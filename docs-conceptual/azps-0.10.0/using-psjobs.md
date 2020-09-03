---
title: PowerShell 작업에서 Azure PowerShell cmdlet 실행
description: -AsJob 및 Start-Job을 사용하여 Azure PowerShell cmdlet을 병렬 또는 백그라운드 작업으로 실행하는 방법에 대해 알아보세요.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5d9028c0a433149c8f6cc346651bb8bf875bb42a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243160"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="f3ab2-103">PowerShell 작업에서 Azure PowerShell cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f3ab2-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="f3ab2-104">Azure PowerShell은 Azure Cloud에 연결하고 응답을 기다리는 방법에 따라 달라지므로 대부분의 cmdlet은 클라우드에서 응답을 받을 때까지 PowerShell 세션을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="f3ab2-105">Powershell 작업을 사용하면 백그라운드에서 cmdlet을 실행하거나 단일 PowerShell 세션 내에서 Azure의 여러 작업을 한 번에 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="f3ab2-106">이 문서는 Azure PowerShell cmdlet을 PowerShell 작업으로 실행하고 완료 여부를 확인하는 방법에 대한 간략한 개요입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="f3ab2-107">Azure PowerShell에서 명령을 실행하려면 [Azure 컨텍스트 및 로그인 자격 증명](context-persistence.md)에서 자세히 설명된 Azure PowerShell 컨텍스트를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="f3ab2-108">PowerShell 작업에 대한 자세한 내용은 [PowerShell 작업 정보](/powershell/module/microsoft.powershell.core/about/about_jobs)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="f3ab2-109">PowerShell 작업을 사용하는 Azure 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f3ab2-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="f3ab2-110">PowerShell 작업은 연결된 PowerShell 세션 없이 별도의 프로세스로서 실행되므로 Azure 자격 증명을 공유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="f3ab2-111">자격 증명은 다음 메서드 중 하나를 사용하여 Azure 컨텍스트 개체로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="f3ab2-112">자동 컨텍스트 지속성.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-112">Automatic context persistence.</span></span> <span data-ttu-id="f3ab2-113">컨텍스트 지속성은 기본적으로 사용되며 여러 세션에서 로그인 정보를 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="f3ab2-114">컨텍스트 지속성을 사용하면 현재 Azure 컨텍스트가 새 프로세스에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="f3ab2-115">Azure PowerShell cmdlet과 함께 `-AzContext` 매개 변수를 사용하여 Azure 컨텍스트 개체를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="f3ab2-116">컨텍스트 지속성을 사용하지 않는 경우 `-AzContext` 인수가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="f3ab2-117">일부 Azure PowerShell cmdlet에서 제공하는 `-AsJob` 스위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f3ab2-118">이 스위치는 현재 활성 Azure 컨텍스트를 사용하여 cmdlet을 PowerShell 작업으로 자동 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="f3ab2-119">cmdlet이 `-AsJob`을 지원하는지 확인하려면 해당 참조 설명서를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="f3ab2-120">`-AsJob` 스위치는 컨텍스트 자동 저장을 사용하도록 설정하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="f3ab2-121">[Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet을 사용하여 실행 중인 작업의 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="f3ab2-122">지금까지 작업에서 출력을 가져오려면 [Receive-Job ](/powershell/module/microsoft.powershell.core/receive-job) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="f3ab2-123">Azure에서 원격으로 작업 진행 상황을 확인하려면 작업에서 수정 중인 리소스 형식과 연결된 `Get-` cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ab2-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="f3ab2-124">참고 항목</span><span class="sxs-lookup"><span data-stu-id="f3ab2-124">See Also</span></span>

* [<span data-ttu-id="f3ab2-125">Azure PowerShell 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f3ab2-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="f3ab2-126">PowerShell 작업 정보</span><span class="sxs-lookup"><span data-stu-id="f3ab2-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="f3ab2-127">Get-Job 참조</span><span class="sxs-lookup"><span data-stu-id="f3ab2-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="f3ab2-128">Receive-Job 참조</span><span class="sxs-lookup"><span data-stu-id="f3ab2-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
