---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881446"
---
# Get-AzureRmExpressRouteServiceProvider

## SYNOPSIS
Express 경로 목록 서비스 공급자 및 해당 특성을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmExpressRouteServiceProvider** Cmdlet은 express 경로 기반 서비스 공급자 및 해당 특성 목록을 검색 합니다. 특성에는 위치 및 대역폭 옵션이 있습니다.

## 예제의

### 예제 1: "실리콘 계곡"의 위치를 사용 하 여 서비스 공급자 목록 가져오기
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### PSExpressRouteServiceProvider에 대 한.

## 상속자

## 관련 링크

[Get-AzureRmExpressRouteCircuitARPTable](Get-AzureRmExpressRouteCircuitARPTable.md)

[Get-AzureRmExpressRouteCircuitRouteTable](Get-AzureRmExpressRouteCircuitRouteTable.md)

[Get-AzureRmExpressRouteCircuitRouteTableSummary](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[Get-AzureRmExpressRouteCircuitStats](Get-AzureRmExpressRouteCircuitStats.md)
