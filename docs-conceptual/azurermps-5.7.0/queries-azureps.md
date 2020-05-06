---
title: Azure PowerShell cmdlet 쿼리 결과
description: Azure에서 리소스에 대한 쿼리 및 결과 형식을 지정하는 방법입니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: dae1db158f940587d81a3fe47dfad8524f136d56
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534661"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Azure PowerShell cmdlet 쿼리 결과

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

기본 제공 cmdlet을 사용하여 PowerShell에서 쿼리를 완료할 수 있습니다. PowerShell에서 cmdlet은 **_동사-명사_** 형태로 이름을 지정합니다. **_Get_** 동사를 사용하는 cmdlet은 cmdlet 쿼리입니다. cmdlet 명사는 cmdlet 동사가 역할을 담당하는 Azure 리소스의 종류입니다.

## <a name="select-simple-properties"></a>단순 속성 선택

Azure PowerShell에는 각 cmdlet에 대해 정의된 기본 형식이 있습니다. 각 리소스 형식의 가장 일반적인 속성은 자동으로 테이블 또는 목록 형식으로 표시됩니다. 출력의 서식을 지정하는 방법에 대한 자세한 내용은 [쿼리 결과 서식 지정](formatting-output.md)을 참조하세요.

`Get-AzureRmVM` cmdlet을 사용하여 계정에서 VM 목록을 쿼리합니다.

```azurepowershell-interactive
Get-AzureRmVM
```

기본 출력의 서식은 자동으로 테이블로 지정됩니다.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

`Select-Object` cmdlet을 사용하여 흥미로운 특정 속성을 선택할 수 있습니다.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>복잡한 중첩 속성 선택

선택하려는 속성이 JSON 출력에서 깊숙이 중첩된 경우 해당 중첩 속성의 전체 경로를 제공해야 합니다. 다음 예제에서는 `Get-AzureRmVM` cmdlet에서 VM 이름 및 OS 형식을 선택하는 방법을 보여 줍니다.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>Where-Object cmdlet으로 결과 필터링

`Where-Object` cmdlet을 사용하면 속성 값에 기반하여 결과를 필터링할 수 있습니다. 다음 예제에서 필터는 해당 이름에 "RGD"라는 텍스트가 포함된 VM만 선택합니다.

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

다음 예제의 결과는 vmSize 'Standard_DS1_V2'가 포함된 VM을 반환합니다.

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
