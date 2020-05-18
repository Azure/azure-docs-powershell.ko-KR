---
title: PowerShell 작업을 사용하여 병렬로 cmdlet 실행
description: -AsJob 매개 변수를 사용하여 병렬로 cmdlet을 실행하는 방법입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: beb7f0a89d2e254b348b79daf4f8d3bfdc562de5
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534203"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="63082-103">PowerShell 작업을 사용하여 병렬로 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="63082-103">Running cmdlets in parallel using PowerShell jobs</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="63082-104">PowerShell에서는 [PowerShell 작업](/powershell/module/microsoft.powershell.core/about/about_jobs)을 통해 비동기 작업을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="63082-105">Azure PowerShell은 Azure에 대한 네트워크 호출 만들기 및 대기에 크게 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="63082-106">일부 경우에는 비차단 호출을 수행해야 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63082-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="63082-107">이러한 요구를 해결하기 위해 Azure PowerShell은 최고 수준의 [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) 지원을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="63082-108">컨텍스트 지속성 및 PSJob</span><span class="sxs-lookup"><span data-stu-id="63082-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="63082-109">PSJob은 개별 프로세스로 실행되므로 Azure 연결을 공유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="63082-110">`Connect-AzureRmAccount`로 Azure 계정에 로그인한 후 작업에 컨텍스트를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-110">After signing in to your Azure account with `Connect-AzureRmAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="63082-111">그러나 컨텍스트가 `Enable-AzureRmContextAutosave`로 자동 저장되도록 선택한 경우 컨텍스트는 작성한 모든 작업과 자동으로 공유됩니다.</span><span class="sxs-lookup"><span data-stu-id="63082-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="63082-112">`-AsJob`을 포함한 자동 작업</span><span class="sxs-lookup"><span data-stu-id="63082-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="63082-113">편의를 위해 Azure PowerShell에서는 장기 실행 cmdlet에 `-AsJob` 스위치를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="63082-114">`-AsJob` 스위치를 사용하면 PSJob을 보다 쉽게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63082-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="63082-115">`Get-Job` 및 `Get-AzureRmVM`을 사용하여 작업 및 진행률을 언제든지 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63082-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzureRmVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="63082-116">작업이 완료되면 `Receive-Job`으로 작업 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63082-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="63082-117">`Receive-Job`은 `-AsJob` 플래그가 없는 것처럼 cmdlet으로부터 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="63082-118">예를 들어 `Do-Action -AsJob`의 `Receive-Job` 결과는 `Do-Action`의 결과와 같은 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="63082-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="63082-119">예제 시나리오</span><span class="sxs-lookup"><span data-stu-id="63082-119">Example Scenarios</span></span>

<span data-ttu-id="63082-120">한 번에 여러 VM을 만들기:</span><span class="sxs-lookup"><span data-stu-id="63082-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

<span data-ttu-id="63082-121">이 예제에서 `Wait-Job` cmdlet을 사용하면 작업이 실행되는 동안 스크립트가 일시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="63082-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="63082-122">스크립트는 모든 작업이 완료되면 실행을 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="63082-123">여러 작업이 병렬로 실행되고 스크립트가 완료될 때까지 기다린 후 작업을 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="63082-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
