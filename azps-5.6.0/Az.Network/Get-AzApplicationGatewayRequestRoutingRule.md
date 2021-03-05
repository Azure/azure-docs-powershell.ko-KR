---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 04c7ef7dd041ce26802f23117edab79353816283
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994079"
---
# Get-AzApplicationGatewayRequestRoutingRule

## SYNOPSIS
애플리케이션 게이트웨이의 요청 라우팅 규칙을 얻습니다.

## 구문

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzApplicationGatewayRequestRoutingRule** cmdlet은 애플리케이션 게이트웨이의 요청 라우팅 규칙을 얻습니다.

## 예제

### 예제 1: 특정 요청 라우팅 규칙 사용
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 결과를 $AppGW.
두 번째 명령은 애플리케이션 게이트웨이에서 Rule01이라는 요청 라우팅 규칙을 $AppGW.

### 예제 2: 요청 라우팅 규칙 목록 얻기
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 결과를 $AppGW.
두 번째 명령은 응용 프로그램 게이트웨이라는 변수에 저장된 Application Gateway에서 요청 라우팅 규칙 목록을 $AppGW.

## 매개 변수

### -ApplicationGateway
요청 라우팅 규칙을 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
이 cmdlet이 도착하는 요청 라우팅 규칙의 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule

## 참고 사항

## 관련 링크

[Add-AzApplicationGatewayRequestRoutingRule](./Add-AzApplicationGatewayRequestRoutingRule.md)

[New-AzApplicationGatewayRequestRoutingRule](./New-AzApplicationGatewayRequestRoutingRule.md)

[Remove-AzApplicationGatewayRequestRoutingRule](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[Set-AzApplicationGatewayRequestRoutingRule](./Set-AzApplicationGatewayRequestRoutingRule.md)


