---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215980"
---
# Get-AzNetworkVirtualApplianceSku

## SYNOPSIS
재고에 사용 가능한 네트워크 가상 어플라이언스 Sku를 가져오거나 나열 합니다.

## 구문과

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Get-AzNetworkVirtualApplianceSku Microsoft Azure 인벤토리에서 사용할 수 있는 네트워크 가상 어플라이언스 Sku를 가져오거나 나열 합니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

이름별로 sku를 가져옵니다.

### 예제 2
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

모든 사용 가능한 네트워크 가상 어플라이언스 Sku를 나열 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -서 비 Uname
Sku 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### PSNetworkVirtualApplianceSku에 대 한.

## 상속자

## 관련 링크
