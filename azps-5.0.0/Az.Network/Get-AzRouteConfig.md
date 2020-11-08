---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226417"
---
# Get-AzRouteConfig

## SYNOPSIS
경로 테이블에서 경로를 가져옵니다.

## 구문과

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzRouteConfig** Cmdlet은 Azure 경로 테이블에서 경로를 가져옵니다.
이름을 기준으로 경로를 지정할 수 있습니다.

## 예제의

### 예제 1: 경로 테이블 가져오기
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

이 명령은 **AzRouteTable** cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.
현재 cmdlet는 RouteTable01 이라는 경로 테이블에서 Route07 이라는 경로를 가져옵니다.

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

### -이름
이 cmdlet이 가져오는 경로의 이름을 지정 합니다.

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

### -RouteTable
이 cmdlet이 경로를 가져오는 경로 테이블을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### PSRouteTable에 대 한.

## 출력

### Microsoft. 네트워크 모델. PSRoute

## 상속자

## 관련 링크

[추가-AzRouteConfig](./Add-AzRouteConfig.md)

[Get-AzRouteTable](./Get-AzRouteTable.md)

[새로운 AzRouteConfig](./New-AzRouteConfig.md)

[제거-AzRouteConfig](./Remove-AzRouteConfig.md)

[Set-AzRouteConfig](./Set-AzRouteConfig.md)


