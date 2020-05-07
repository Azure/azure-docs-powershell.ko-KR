---
title: Azure PowerShell cmdlet 출력 형식 지정
description: Azure powershell cmdlet 출력의 형식을 지정 하는 방법.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 6a35024e1bac819fa9b69174195e5245361cb7cc
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534994"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="4af8e-103">Azure PowerShell cmdlet 출력 형식 지정</span><span class="sxs-lookup"><span data-stu-id="4af8e-103">Format AzurePowerShell cmdlet output</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="4af8e-104">기본적으로 각 Azure PowerShell cmdlet은 미리 정의된 출력의 형식을 지정하여 쉽게 읽을 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="4af8e-105">또한 PowerShell은 출력을 조정하거나 cmdlet 출력을 다음 cmdlet을 가진 다른 형식으로 변환할 수 있는 유연성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="4af8e-106">서식 지정</span><span class="sxs-lookup"><span data-stu-id="4af8e-106">Formatting</span></span>      | <span data-ttu-id="4af8e-107">변환</span><span class="sxs-lookup"><span data-stu-id="4af8e-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="4af8e-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="4af8e-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="4af8e-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="4af8e-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="4af8e-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="4af8e-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="4af8e-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="4af8e-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="4af8e-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="4af8e-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="4af8e-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="4af8e-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="4af8e-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="4af8e-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="4af8e-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="4af8e-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="4af8e-116">형식 지정 예제</span><span class="sxs-lookup"><span data-stu-id="4af8e-116">Format examples</span></span>

<span data-ttu-id="4af8e-117">이 예제에서는 기본 구독에 있는 Azure VM의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-117">In this example, we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="4af8e-118">`Get-AzureRmVM` 명령은 출력을 기본적으로 테이블 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="4af8e-119">반환되는 열을 제한하려는 경우 `Format-Table` cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="4af8e-120">다음 예제에서는 가상 머신의 동일한 목록을 가져오지만 VM의 이름, 리소스 그룹 및 VM의 위치에 대한 출력을 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-120">In the following example, we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="4af8e-121">`-Autosize` 매개 변수는 데이터의 크기에 따라 열 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="4af8e-122">또한 출력을 목록으로 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="4af8e-123">다음 예제에서는 `Format-List` cmdlet을 사용하여 이를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="4af8e-124">다른 데이터 형식으로 변환</span><span class="sxs-lookup"><span data-stu-id="4af8e-124">Convert to other data types</span></span>

<span data-ttu-id="4af8e-125">PowerShell은 또한 명령 출력을 여러 데이터 형식으로 변환할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="4af8e-126">다음 예제에서는 `Select-Object` cmdlet을 사용하여 구독에서 가상 머신의 특성을 가져오고, 출력을 CSV 형식으로 변환하여 데이터베이스 또는 스프레드시트로 쉽게 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-126">In the following example, the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="4af8e-127">출력을 JSON 형식으로 변환할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="4af8e-128">다음 예제에서는 VM의 동일한 목록을 만들지만 출력 형식을 JSON으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="4af8e-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
