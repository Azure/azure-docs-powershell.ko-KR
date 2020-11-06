---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 204d70753d3a4ae80e05dfff90d4a5b50b47ab58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536596"
---
# Get-AzureRmExpressRouteCircuitPeeringConfig

## SYNOPSIS
Express 경로 회로 피어 링 구성을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmExpressRouteCircuitPeeringConfig** Cmdlet은 express 경로 회로에 대 한 피어 링 관계의 구성을 검색 합니다.

## 예제의

### 예제 1: Express 경로 회로에 대 한 피어 링 구성 표시
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

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

### -ExpressRouteCircuit
피어 링 구성을 포함 하는 Express 경로 회로 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
검색할 피어 링 구성의 이름입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSExpressRouteCircuit에 대 한.
매개 변수: ExpressRouteCircuit (ByValue)

## 출력

### PSPeering에 대 한.

## 상속자

## 관련 링크

[추가-AzureRmExpressRouteCircuitPeeringConfig](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[새로운 AzureRmExpressRouteCircuitPeeringConfig](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[제거-AzureRmExpressRouteCircuitPeeringConfig](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[Set-AzureRmExpressRouteCircuit](Set-AzureRmExpressRouteCircuit.md)
