---
title: Azure 리소스에 대한 쿼리 및 결과 서식 지정 | Microsoft Docs
description: Azure에서 리소스에 대한 쿼리 및 결과 형식을 지정하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 23cc0d13e9ecb17bef04cedc8a0f395a04e89390
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386479"
---
# <a name="querying-for-azure-resources"></a>Azure 리소스에 대한 쿼리

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

기본 제공 cmdlet을 사용하여 PowerShell에서 쿼리를 완료할 수 있습니다. PowerShell에서 cmdlet은 **_동사-명사_** 형태로 이름을 지정합니다. **_Get_** 동사를 사용하는 cmdlet은 cmdlet 쿼리입니다. cmdlet 명사는 cmdlet 동사가 역할을 담당하는 Azure 리소스의 종류입니다.

## <a name="selecting-simple-properties"></a>단순 속성 선택

Azure PowerShell에는 각 cmdlet에 대해 정의된 기본 형식이 있습니다. 각 리소스 형식의 가장 일반적인 속성은 자동으로 테이블 또는 목록 형식으로 표시됩니다. 출력의 서식을 지정하는 방법에 대한 자세한 내용은 [쿼리 결과 서식 지정](formatting-output.md)을 참조하세요.

`Get-AzureRmVM` cmdlet을 사용하여 계정에서 VM 목록을 쿼리합니다.

```powershell-interactive
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

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>복잡한 중첩 속성 선택

선택하려는 속성이 JSON 출력에서 깊숙이 중첩된 경우 해당 중첩 속성의 전체 경로를 제공해야 합니다. 다음 예제에서는 `Get-AzureRmVM` cmdlet에서 VM 이름 및 OS 형식을 선택하는 방법을 보여 줍니다.

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>장소-개체 cmdlet을 사용하는 결과 필터링

`Where-Object` cmdlet을 사용하면 속성 값에 기반하여 결과를 필터링할 수 있습니다. 다음 예제에서 필터는 해당 이름에 "RGD"라는 텍스트가 포함된 VM만 선택합니다.

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

다음 예제의 결과는 vmSize 'Standard_DS1_V2'가 포함된 VM을 반환합니다.

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
