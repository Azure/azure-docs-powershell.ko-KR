---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 4b2b8f2694377845af92db5809230a423f83d594
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700731"
---
# Add-AzApplicationGatewayRewriteRuleSet

## SYNOPSIS
응용 프로그램 게이트웨이에 다시 쓰기 규칙 집합을 추가 합니다.

## 구문과

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzApplicationGatewayRewriteRuleSet** cmdlet은 응용 프로그램 게이트웨이에 다시 작성 규칙 집합을 추가 합니다.

## 예제의

### 예제 1
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.
두 번째 명령은 응용 프로그램 게이트웨이에 다시 작성 규칙 집합을 추가 합니다.

## 변수

### -ApplicationGateway
ApplicationGateway

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
RewriteRuleSet의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRule
재작성 규칙 목록

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. * PSApplicationGateway

## 출력

### Microsoft. * PSApplicationGateway

## 상속자

## 관련 링크

[Get-AzApplicationGatewayRewriteRuleSet](./Get-AzApplicationGatewayRewriteRuleSet.md)

[새로운 AzApplicationGatewayRewriteRuleSet](./New-AzApplicationGatewayRewriteRuleSet.md)

[제거-AzApplicationGatewayRewriteRuleSet](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[Set-AzApplicationGatewayRewriteRuleSet](./Set-AzApplicationGatewayRewriteRuleSet.md)

[새로운 AzApplicationGatewayRewriteRule](./New-AzApplicationGatewayRewriteRule.md)

[새로운 AzApplicationGatewayRewriteRuleActionSet](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[새로운 AzApplicationGatewayRewriteRuleHeaderConfiguration](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
