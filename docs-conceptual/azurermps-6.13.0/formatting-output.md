---
title: Azure PowerShell cmdlet 출력 형식 지정
description: Azure powershell cmdlet 출력의 형식을 지정 하는 방법.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 059b00194de2e9369f7c8e39d22049035bd7b814
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83388043"
---
# <a name="format-azurepowershell-cmdlet-output"></a>Azure PowerShell cmdlet 출력 형식 지정

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

기본적으로 각 Azure PowerShell cmdlet은 미리 정의된 출력의 형식을 지정하여 쉽게 읽을 수 있도록 합니다.  또한 PowerShell은 출력을 조정하거나 cmdlet 출력을 다음 cmdlet을 가진 다른 형식으로 변환할 수 있는 유연성을 제공합니다.

| 서식 지정      | 변환       |
|-----------------|------------------|
| [Format-Custom](/powershell/module/microsoft.powershell.utility/format-custom) | [ConvertTo-Csv](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [Format-List](/powershell/module/microsoft.powershell.utility/format-list)   | [ConvertTo-Html](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [Format-Table](/powershell/module/microsoft.powershell.utility/format-table)  | [ConvertTo-Json](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [Format-Wide](/powershell/module/microsoft.powershell.utility/format-wide)   | [ConvertTo-Xml](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a>형식 지정 예제

이 예제에서는 기본 구독에 있는 Azure VM의 목록을 가져옵니다.  `Get-AzureRmVM` 명령은 출력을 기본적으로 테이블 형식으로 지정합니다.

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

반환되는 열을 제한하려는 경우 `Format-Table` cmdlet을 사용할 수 있습니다. 다음 예제에서는 가상 머신의 동일한 목록을 가져오지만 VM의 이름, 리소스 그룹 및 VM의 위치에 대한 출력을 제한합니다.  `-Autosize` 매개 변수는 데이터의 크기에 따라 열 크기를 지정합니다.

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

또한 출력을 목록으로 나타낼 수 있습니다. 다음 예제에서는 `Format-List` cmdlet을 사용하여 이를 보여 줍니다.

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

## <a name="convert-to-other-data-types"></a>다른 데이터 형식으로 변환

PowerShell은 또한 명령 출력을 여러 데이터 형식으로 변환할 수도 있습니다. 다음 예제에서는 `Select-Object` cmdlet을 사용하여 구독에서 가상 머신의 특성을 가져오고, 출력을 CSV 형식으로 변환하여 데이터베이스 또는 스프레드시트로 쉽게 가져옵니다.

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

출력을 JSON 형식으로 변환할 수도 있습니다.  다음 예제에서는 VM의 동일한 목록을 만들지만 출력 형식을 JSON으로 변경합니다.

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
