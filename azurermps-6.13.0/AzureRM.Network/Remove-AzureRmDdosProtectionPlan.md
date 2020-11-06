---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 87110fe779e128e8ef5d5d6de0504ec9fdca1b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537539"
---
# Remove-AzureRmDdosProtectionPlan

## SYNOPSIS
DDoS 보호 계획을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Remove-AzureRmDdosProtectionPlan cmdlet은 DDoS protection 계획을 제거 합니다.

## 예제의

### 예제 1: 빈 DDoS 보호 계획 제거
```
D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

이 경우 지정 된 대로 DDoS protection 계획을 제거 합니다.

### 예제 2: 가상 네트워크와 연결 된 DDoS protection 계획 제거
```
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzureRmVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

DDoS 보호 계획은 가상 네트워크와 연결 되어 있는 경우 삭제할 수 없습니다. 따라서 첫 번째 단계는 두 개체의 연관을 해제 하는 것입니다. 여기서는 계획과 연결 된 가상 네트워크의 업데이트 버전을 **DdosProtectionPlan** 속성을 빈 값으로 설정 하 고 플래그 **EnableDdosProtection** (이 플래그는 계획 없이는 true 일 수 없습니다).
그런 다음 지역 변수를 **Set-AzureRmVirtualNetwork** 에 파이핑 하 여 새 상태를 유지 합니다. 이 시점에서 계획이 더 이상 가상 네트워크에 연결 되어 있지 않습니다.
이 계획이 계획에 연결 된 마지막 DDoS 경우 Remove-AzureRmDdosProtectionPlan 명령을 사용 하 여 보호 계획을 제거할 수 있습니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
제거할 DDoS 보호 계획의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
제거할 DDoS protection 계획의 리소스 그룹을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### 시스템 부울

## 상속자

## 관련 링크

[새로운 AzureRmDdosProtectionPlan](./New-AzureRmDdosProtectionPlan.md)

[Get-AzureRmDdosProtectionPlan](./Get-AzureRmDdosProtectionPlan.md)

[새로운 AzureRmVirtualNetwork](./New-AzureRmVirtualNetwork.md)

[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)

[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
