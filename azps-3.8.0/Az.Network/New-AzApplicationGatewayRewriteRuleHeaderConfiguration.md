---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044783"
---
# New-AzApplicationGatewayRewriteRuleHeaderConfiguration

## SYNOPSIS
응용 프로그램 게이트웨이에 대 한 재작성 규칙 헤더 구성을 만듭니다.

## 구문과

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzApplicationGatewayRewriteRuleHeaderConfiguration Cmdlet은** Azure application gateway에 대해 설정 된 재작성 규칙 작업을 만듭니다.

## 예제의

### 예제 1
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

이 명령은 재작성 규칙 헤더 구성을 만들고, 결과를 $hc 이라는 변수에 저장 합니다.

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

### -인원 Ername
다시 쓸 헤더의 이름입니다.

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

### -HeaderValue
지정 된 헤더 이름에 대 한 집합에 대 한 헤더 값입니다.
이를 생략 하면 헤더가 삭제 됩니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### Microsoft. 네트워크. Psapplication의 Header구성

## 상속자

## 관련 링크

[추가-AzApplicationGatewayRewriteRuleSet](./Add-AzApplicationGatewayRewriteRuleSet.md)

[Get-AzApplicationGatewayRewriteRuleSet](./Get-AzApplicationGatewayRewriteRuleSet.md)

[새로운 AzApplicationGatewayRewriteRuleSet](./New-AzApplicationGatewayRewriteRuleSet.md)

[제거-AzApplicationGatewayRewriteRuleSet](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[Set-AzApplicationGatewayRewriteRuleSet](./Set-AzApplicationGatewayRewriteRuleSet.md)

[새로운 AzApplicationGatewayRewriteRule](./New-AzApplicationGatewayRewriteRule.md)

[새로운 AzApplicationGatewayRewriteRuleActionSet](./New-AzApplicationGatewayRewriteRuleActionSet.md)
