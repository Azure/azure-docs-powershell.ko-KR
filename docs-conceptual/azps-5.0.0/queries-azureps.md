---
title: Azure PowerShell cmdlet 쿼리 결과
description: Azure에서 리소스에 대한 쿼리 및 결과 형식을 지정하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 71de99fec7de36cf8cc0fe3e8840fb55cedc5db7
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409961"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="061ae-103">Azure PowerShell 쿼리 출력</span><span class="sxs-lookup"><span data-stu-id="061ae-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="061ae-104">각 Azure PowerShell cmdlet의 결과는 Azure PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="061ae-105">명시적 `Get-` 작업이 아닌 cmdlet도 생성되거나 수정된 리소스에 대한 정보를 제공하기 위해 검사할 수 있는 값을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="061ae-106">대부분의 cmdlet은 단일 개체를 반환하지만 일부는 반복되어야 하는 배열을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="061ae-107">대부분의 경우 Azure PowerShell의 출력을 [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet(약식 `select`)을 사용하여 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="061ae-108">출력은 [Where-object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), 또는 별칭인 `where`을 사용하여 필터링할 수 있습니다</span><span class="sxs-lookup"><span data-stu-id="061ae-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="061ae-109">단순 속성 선택</span><span class="sxs-lookup"><span data-stu-id="061ae-109">Select simple properties</span></span>

<span data-ttu-id="061ae-110">기본 테이블 형식에서, Azure PowerShell cmdlet은 사용 가능한 속성을 모두 표시하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="061ae-111">[Format-list](/powershell/module/microsoft.powershell.utility/format-list) cmdlet 또는 `Select-Object *`로 출력을 파이핑하여 전체 속성을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="061ae-112">관심있는 속성의 이름을 알게되면 `Select-Object`와 같은 속성 이름을 사용하여 직접 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="061ae-113">`Select-Object`를 사용한 출력은 항상 요청된 형식을 표시하도록 서식 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="061ae-114">쿼리 결과를 cmdlet 결과의 일부로 사용하는 방법에 대한 자세한 내용은 [Azure PowerShell cmdlet 출력 형식](formatting-output.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="061ae-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="061ae-115">중첩 속성 선택</span><span class="sxs-lookup"><span data-stu-id="061ae-115">Select nested properties</span></span>

<span data-ttu-id="061ae-116">Azure PowerShell cmdlet 출력의 일부 속성은 `Get-AzVM` 출력의 `StorageProfile` 속성과 같은 중첩된 개체를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="061ae-117">중첩 된 속성에서 값을 가져오려면, `Select-Object`에 대한 사전 인수의 일부로 검사할 값의 전체 경로 및 표시 이름을 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="061ae-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="061ae-118">각 사전 인수는 개체의 한 속성을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="061ae-119">추출할 속성은 식의 일부여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="061ae-120">결과 필터링</span><span class="sxs-lookup"><span data-stu-id="061ae-120">Filter results</span></span> 

<span data-ttu-id="061ae-121">`Where-Object` cmdlet을 사용하면 중첩 속성을 포함하여 속성 값에 기반하여 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="061ae-122">다음 예제는 `Where-Object`를 사용하여 리소스 그룹에서 Linux VM을 찾는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="061ae-123">`Select-Object`, `Where-Object`의 결과를 각각으로 파이프할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="061ae-124">성능 향상을 위해, `Where-Object` 작업을 `Select-Object` 전에 두는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="061ae-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```
