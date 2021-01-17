---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337826"
---
# Get-AzApplicationGatewayWebApplicationFirewallConfiguration

## SYNOPSIS
애플리케이션 게이트웨이의 WAF 구성을 얻습니다.

## 구문

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 애플리케이션 게이트웨이의 WAF(웹 애플리케이션 방화벽) 구성을 얻습니다.

## 예제

### 예제 1: 애플리케이션 게이트웨이 웹 애플리케이션 방화벽 구성을 얻게 됩니다.
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

첫 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이를 구한 다음, 애플리케이션 $AppGW 저장합니다.
두 번째 명령은 애플리케이션 게이트웨이의 방화벽 구성을 $AppGW 다음, 애플리케이션 게이트웨이에 $FirewallConfig.

## PARAMETERS

### -ApplicationGateway
애플리케이션 게이트웨이 개체를 지정합니다.
애플리케이션 게이트웨이 개체를 Get-AzApplicationGateway cmdlet을 사용할 수 있습니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration

## 참고 사항

## 관련 링크

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[New-AzApplicationGatewayWebApplicationFirewallConfiguration](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[Set-AzApplicationGatewayWebApplicationFirewallConfiguration](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


