---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371323"
---
# New-AzApplicationGatewayPathRuleConfig

## SYNOPSIS
애플리케이션 게이트웨이 경로 규칙을 만듭니다.

## 구문

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzApplicationGatewayPathRuleConfig** cmdlet은 애플리케이션 게이트웨이 경로 규칙을 만듭니다.
이 cmdlet에서 만든 규칙은 URL 경로 맵 구성 설정의 컬렉션에 추가한 다음 게이트웨이에 할당할 수 있습니다.
경로 맵 구성 설정은 애플리케이션 게이트웨이 부하 분산에 사용됩니다.

## 예제

### 예제 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

이러한 명령은 새 애플리케이션 게이트웨이 경로 규칙을 만든 다음 **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet을 사용하여 애플리케이션 게이트웨이에 해당 규칙을 할당합니다.
이를 위해 첫 번째 명령은 ContosoApplicationGateway 게이트웨이에 대한 개체 참조를 만듭니다.
이 개체 참조는 $Gateway.
다음 두 명령은 백end 주소 풀 및 백end HTTP 설정 개체를 만듭니다. 경로 규칙 개체를 만들기 위해 이러한 개체($AddressPool 및 $HttpSettings 변수에 저장)가 필요합니다.
네 번째 명령은 경로 규칙 개체를 만들고 경로 규칙이라는 변수에 $PathRuleConfig.
다섯 번째 명령은 **Add-AzApplicationGatewayUrlPathMapConfig를** 사용하여 구성 설정 및 해당 설정 내에 포함된 새 경로 규칙을 ContosoApplicationGateway에 추가합니다.

### 예제 2
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

이 명령은 "base"로, 경로는 "/base"로, BackendAddressPool은 $AddressPool, BackendHttpSettings는 $HttpSettings, FirewallPolicy는 $firewallPolicy.ngs로, ContosoApplicationGateway에 대한 해당 설정 내에 포함된 새 경로 규칙으로 경로 규칙을 만듭니다.

## PARAMETERS

### -BackendAddressPool
게이트웨이 경로 규칙 구성 설정에 추가할 백end 주소 풀 설정의 컬렉션에 대한 개체 참조를 지정합니다.
이와 유사한 New-AzApplicationGatewayBackendAddressPool cmdlet 및 구문을 사용하여 이 개체 참조를 만들 수 있습니다. `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
이전 명령은 주소 풀에 두 개의 IP 주소(192.16.1.1 및 192.168.1.2)를 추가합니다.
IP 주소는 따옴표로 묶고 콤마를 사용하여 구분됩니다.
그러면 결과 변수인 $AddressPool *DefaultBackendAddressPool* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다.
백end 주소 풀은 백end 서버의 IP 주소를 나타 내는 것입니다.
이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소에 속해야 합니다.
이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 없습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백드 주소 풀의 ID를 지정합니다.
주소 풀은 Get-AzApplicationGatewayBackendAddressPool cmdlet을 사용하여 반환할 수 있습니다.
ID가 있는 후 *DefaultBackendAddressPool 매개 변수 대신 DefaultBackendAddressPoolId* 매개 변수를 사용할 *수* 있습니다.
예: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 백end 주소 풀은 백end 서버의 IP 주소를 나타남
이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소에 속해야 합니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettings
게이트웨이 경로 규칙 구성 설정에 추가할 백end HTTP 설정 컬렉션에 대한 개체 참조를 지정합니다.
New-AzApplicationGatewayBackendHttpSettings cmdlet과 비슷한 구문을 사용하여 이 개체 참조를 만들 수 있습니다. $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" 결과 변수 $HttpSettings *DefaultBackendAddressPool* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다. -DefaultBackendHttpSettings $HttpSettings 백 $HttpSettings HTTP 설정은 백end 풀에 대한 포트, 프로토콜 및 쿠키 기반 속성과 같은 속성을 구성합니다.
이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettingsId* 매개 변수를 사용할 수 없습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백end HTTP 설정 컬렉션의 ID를 지정합니다.
HTTP 설정 IDD는 Get-AzApplicationGatewayBackendHttpSettings 반환할 수 있습니다.
ID가 있는 후 *DefaultBackendHttpSettings 매개 변수 대신 DefaultBackendHttpSettingsId* 매개 변수를 사용할 *수* 있습니다.
예: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 백end HTTP 설정은 포트, 프로토콜 등의 속성을 구성합니다. 백end 풀에 대한 쿠키 기반의 에인티비전을 제공합니다.
이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettings 매개* 변수를 사용할 수 없습니다.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicy
최상위 방화벽 정책에 대한 개체 참조를 지정합니다. 개체 참조는 cmdlet을 사용하여 New-AzApplicationGatewayWebApplicationFirewallPolicy 있습니다.
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" 위의 commandlet을 사용하여 만든 방화벽 정책을 경로 규칙 수준에서 참조할 수 있습니다. 위의 명령은 기본 정책 설정 및 관리 규칙을 만들 것입니다.
사용자는 기본값 대신 각각 정책 및 데이터 형식을 사용하여 PolicySettings, ManagedRules를 New-AzApplicationGatewayFirewallPolicySettings New-AzApplicationGatewayFirewallPolicyManagedRules 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
기존 최상위 웹 애플리케이션 방화벽 리소스의 ID를 지정합니다.
Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet을 사용하여 방화벽 정책 Get-AzApplicationGatewayWebApplicationFirewallPolicy 있습니다. ID가 있는 후 *FirewallPolicy* 매개 변수 대신 *FirewallPolicyId* 매개 변수를 사용할 수 있습니다.
예: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Name
이 cmdlet에서 만드는 경로 규칙 구성의 이름을 지정합니다.

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

### -Paths
하나 이상의 애플리케이션 게이트웨이 경로 규칙을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
Application gateway RedirectConfiguration

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
Application Gateway RedirectConfiguration의 ID

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSet
Application gateway RewriteRuleSet

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSetId
Application Gateway RewriteRuleSet의 ID

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule

## 참고 사항

## 관련 링크

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)

[New-AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


