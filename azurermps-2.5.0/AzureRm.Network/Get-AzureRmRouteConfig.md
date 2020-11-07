---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 907ca017518304a38340e9539aa4e8faf4216d59
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882921"
---
# Get-AzureRmRouteConfig

## SYNOPSIS
경로 테이블에서 경로를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmRouteConfig** Cmdlet은 Azure 경로 테이블에서 경로를 가져옵니다.
이름을 기준으로 경로를 지정할 수 있습니다.

## 예제의

### 예제 1: 경로 테이블 가져오기
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

이 명령은 **AzureRmRouteTable** cmdlet을 사용 하 여 RouteTable01 이라는 경로 테이블을 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 해당 테이블을 현재 cmdlet에 전달 합니다.
현재 cmdlet는 RouteTable01 이라는 경로 테이블에서 Route07 이라는 경로를 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 가져오는 경로의 이름을 지정 합니다.

```yaml
Type: String
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
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSRouteTable
' RouteTable ' 매개 변수는 파이프라인에서 ' PSRouteTable ' 형식의 값을 허용 합니다.

## 출력

### Microsoft. 네트워크 모델. PSRoute

## 상속자

## 관련 링크

[추가-AzureRmRouteConfig](./Add-AzureRmRouteConfig.md)

[Get-AzureRmRouteTable](./Get-AzureRmRouteTable.md)

[새로운 AzureRmRouteConfig](./New-AzureRmRouteConfig.md)

[제거-AzureRmRouteConfig](./Remove-AzureRmRouteConfig.md)

[Set-AzureRmRouteConfig](./Set-AzureRmRouteConfig.md)


