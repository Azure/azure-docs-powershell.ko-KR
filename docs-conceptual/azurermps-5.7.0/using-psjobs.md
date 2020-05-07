---
title: PowerShell 작업을 사용하여 병렬로 cmdlet 실행
description: -AsJob 매개 변수를 사용하여 병렬로 cmdlet을 실행하는 방법입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: d2ffd6cc4c5e70c53ab60b1280384faac9b45867
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534719"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="d3b15-103">PowerShell 작업을 사용하여 병렬로 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d3b15-103">Running cmdlets in parallel using PowerShell jobs</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="d3b15-104">PowerShell에서는 [PowerShell 작업](/powershell/module/microsoft.powershell.core/about/about_jobs)을 통해 비동기 작업을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="d3b15-105">Azure PowerShell은 Azure에 대한 네트워크 호출 만들기 및 대기에 크게 의존합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="d3b15-106">개발자는 스크립트에서 Azure에 대해 여러 개의 비중단 호출을 시도하거나 현재 세션을 차단하지 않고 REPL에서 Azure 리소스를 만들고자 하는 경우가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="d3b15-107">이러한 요구를 해결하기 위해 Azure PowerShell에는 최고 수준의 [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) 지원을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="d3b15-108">컨텍스트 지속성 및 PSJob</span><span class="sxs-lookup"><span data-stu-id="d3b15-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="d3b15-109">PSJob은 별도의 프로세스로 실행되므로 Azure 연결에 대한 정보를 작성한 작업과 적절하게 공유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="d3b15-110">`Connect-AzureRmAccount`로 Azure 계정을 PowerShell 세션에 연결하면 컨텍스트를 작업에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-110">Upon connecting your Azure account to your PowerShell session with `Connect-AzureRmAccount`, you can pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="d3b15-111">그러나 컨텍스트가 `Enable-AzureRmContextAutosave`로 자동 저장되도록 선택한 경우 컨텍스트는 작성한 모든 작업과 자동으로 공유됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="d3b15-112">`-AsJob`을 포함한 자동 작업</span><span class="sxs-lookup"><span data-stu-id="d3b15-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="d3b15-113">편의를 위해 Azure PowerShell에서는 장기 실행 cmdlet에 `-AsJob` 스위치를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="d3b15-114">`-AsJob` 스위치를 사용하면 PSJob을 보다 쉽게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="d3b15-115">`Get-Job` 및 `Get-AzureRmVM`을 사용하여 작업 및 진행률을 언제든지 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

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

<span data-ttu-id="d3b15-116">이후에 완료되면, `Receive-Job`으로 작업 결과를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="d3b15-117">`Receive-Job`은 `-AsJob` 플래그가 없는 것처럼 cmdlet으로부터 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="d3b15-118">예를 들어 `Receive-Job`의 `Do-Action -AsJob` 결과는 `Do-Action`의 결과와 같은 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

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

## <a name="example-scenarios"></a><span data-ttu-id="d3b15-119">예제 시나리오</span><span class="sxs-lookup"><span data-stu-id="d3b15-119">Example Scenarios</span></span>

<span data-ttu-id="d3b15-120">한 번에 여러 VM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-120">Create multiple VMs at once.</span></span>

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

<span data-ttu-id="d3b15-121">이 예제에서 `Wait-Job` cmdlet을 사용하면 작업이 실행되는 동안 스크립트가 일시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="d3b15-122">스크립트는 모든 작업이 완료되면 실행을 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="d3b15-123">이렇게 하면 여러 작업을 병렬로 실행한 다음 완료될 때까지 기다렸다가 계속 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3b15-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

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
