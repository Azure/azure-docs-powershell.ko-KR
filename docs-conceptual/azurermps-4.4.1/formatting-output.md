---
title: 쿼리 결과 서식 지정 | Microsoft Docs
description: Azure에서 리소스에 대한 쿼리 및 결과 형식을 지정하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: a76ceee5ae1172630d74afd3c671031592d78a8b
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386768"
---
# <a name="formatting-query-results"></a><span data-ttu-id="030eb-103">쿼리 결과 서식 지정</span><span class="sxs-lookup"><span data-stu-id="030eb-103">Formatting query results</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="030eb-104">기본적으로 각 PowerShell cmdlet은 미리 정의된 출력의 서식을 지정하여 쉽게 읽을 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="030eb-105">또한 PowerShell은 출력을 조정하거나 cmdlet 출력을 다음 cmdlet을 가진 다른 형식으로 변환할 수 있는 유연성을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="030eb-106">서식 지정</span><span class="sxs-lookup"><span data-stu-id="030eb-106">Formatting</span></span>      | <span data-ttu-id="030eb-107">변환</span><span class="sxs-lookup"><span data-stu-id="030eb-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="030eb-108">서식 지정 예제</span><span class="sxs-lookup"><span data-stu-id="030eb-108">Formatting examples</span></span>

<span data-ttu-id="030eb-109">이 예제에서는 기본 구독에 있는 Azure VM의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="030eb-110">Get-AzureRmVM 명령은 출력을 기본적으로 테이블 형식으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="030eb-111">반환되는 열을 제한하려는 경우 `Format-Table` cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="030eb-112">다음 예제에서는 가상 머신의 동일한 목록을 가져오지만 VM의 이름, 리소스 그룹 및 VM의 위치에 대한 출력을 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="030eb-113">`-Autosize` 매개 변수는 데이터의 크기에 따라 열 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="030eb-114">선호하는 목록 형식에서 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="030eb-115">다음 예제에서는 `Format-List` cmdlet을 사용하여 이를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell-interactive
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

## <a name="converting-to-other-data-types"></a><span data-ttu-id="030eb-116">다른 데이터 형식으로 변환</span><span class="sxs-lookup"><span data-stu-id="030eb-116">Converting to other data types</span></span>

<span data-ttu-id="030eb-117">또한 PowerShell은 사용할 수 있는 여러 출력 형식을 제공하여 요구 사항을 충족합니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="030eb-118">다음 예제에서는 `Select-Object` cmdlet을 사용하여 구독에서 가상 머신의 특성을 가져오고, 출력을 CSV 형식으로 변환하여 데이터베이스 또는 스프레드시트로 쉽게 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="030eb-119">출력을 JSON 형식으로 변환할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="030eb-120">다음 예제에서는 VM의 동일한 목록을 만들지만 출력 형식을 JSON으로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="030eb-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell-interactive
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
