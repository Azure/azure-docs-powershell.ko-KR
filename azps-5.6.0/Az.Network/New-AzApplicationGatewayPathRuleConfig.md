---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b343ecbabd66f32be30f4aff1b0a44c7ddf186d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985852"
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
이 cmdlet에서 만든 규칙은 URL 경로 맵 구성 설정 컬렉션에 추가한 다음 게이트웨이에 할당할 수 있습니다.
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

이러한 명령은 새 애플리케이션 게이트웨이 경로 규칙을 만든 다음 **Add-AzApplicationGatewayUrlPathpConfig** cmdlet을 사용하여 해당 규칙을 애플리케이션 게이트웨이에 할당합니다.
이렇게 하여 첫 번째 명령은 게이트웨이 ContosoApplicationGateway에 대한 개체 참조를 만듭니다.
이 개체 참조는 이라는 변수에 $Gateway.
다음 두 명령은 백던드 주소 풀 및 백end HTTP 설정 개체를 만듭니다. 경로 규칙 개체를 만들기 위해 이러한 개체($AddressPool 및 $HttpSettings)가 필요합니다.
네 번째 명령은 경로 규칙 개체를 만들고 이라는 변수에 $PathRuleConfig.
다섯 번째 명령은 **Add-AzApplicationGatewayUrlPathMapConfig를** 사용하여 구성 설정 및 해당 설정에 포함된 새 경로 규칙을 ContosoApplicationGateway에 추가합니다.

### 예제 2
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

이 명령은 이름과 함께 경로 규칙을 만듭니다. "/base"로 경로, BackendAddressPool을 $AddressPool BackendAddressPool, $firewallPolicy BackendHttpSettings를 $HttpSettings.ngs 및 ContosoApplicationGateway에 대한 해당 설정에 포함된 새 경로 규칙으로 경로 규칙을 만듭니다.

## 매개 변수

### -BackendAddressPool
게이트웨이 경로 규칙 구성 설정에 추가할 백드 주소 풀 설정의 컬렉션에 대한 개체 참조를 지정합니다.
이와 유사한 New-AzApplicationGatewayBackendAddressPool cmdlet 및 구문을 사용하여 이 개체 참조를 만들 수 있습니다. `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
이전 명령은 주소 풀에 두 개의 IP 주소(192.16.1.1 및 192.168.1.2)를 추가합니다.
IP 주소는 따옴표로 묶고 콤마를 사용하여 구분됩니다.
그러면 결과 변수인 $AddressPool *DefaultBackendAddressPool* 매개 변수의 매개 변수 값으로 사용할 수 있습니다.
백던드 주소 풀은 백end 서버의 IP 주소를 나타내고 있습니다.
이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소일 수 있습니다.
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
주소 풀 아이디는 Get-AzApplicationGatewayBackendAddressPool cmdlet을 사용하여 반환할 수 있습니다.
ID가 있는 후 *DefaultBackendAddressPool 매개 변수 대신 DefaultBackendAddressPool* 매개 변수를 사용할 *수* 있습니다.
예: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" 백end 주소 풀은 백end 서버의 IP 주소를 나타내고 있습니다.
이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소일 수 있습니다.

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
이와 유사한 New-AzApplicationGatewayBackendHttpSettings cmdlet 및 구문을 사용하여 이 개체 참조를 만들 수 있습니다. $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" 결과 변수, $HttpSettings *기본BackendAddressPool* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다. -DefaultBackendHttpSettings $HttpSettings 백end HTTP 설정은 백end 풀에 대한 포트, 프로토콜 및 쿠키 기반 연결성과 같은 속성을 구성합니다.
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
게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백END HTTP 설정 컬렉션의 ID를 지정합니다.
HTTP 설정 아이디는 Get-AzApplicationGatewayBackendHttpSettings cmdlet을 사용하여 반환할 수 있습니다.
ID가 있는 후 *DefaultBackendHttpSettings 매개 변수 대신 DefaultBackendHttpSettings 매개* 변수를 사용할 *수* 있습니다.
예: -DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" 백end HTTP 설정은 포트, 프로토콜, 백end 풀에 대한 쿠키 기반의 에피니티를 제공합니다.
이 매개 변수를 사용하는 경우 동일한 명령에서 *DefaultBackendHttpSettings* 매개 변수를 사용할 수 없습니다.

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
최상위 방화벽 정책에 대한 개체 참조를 지정합니다. 개체 참조는 cmdlet을 사용하여 New-AzApplicationGatewayWebApplicationFirewallPolicy 수 있습니다.
$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" 위의 명령줄을 사용하여 만든 방화벽 정책을 경로 규칙 수준에서 참조할 수 있습니다. 위의 명령은 기본 정책 설정 및 관리되는 규칙을 만들 것입니다.
사용자는 기본 값 대신 각각 New-AzApplicationGatewayFirewallPolicySettings 사용하여 PolicySettings, ManagedRules를 New-AzApplicationGatewayFirewallPolicySettings New-AzApplicationGatewayFirewallPolicyManagedRules 있습니다.

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
방화벽 정책 신분은 cmdlet을 사용하여 Get-AzApplicationGatewayWebApplicationFirewallPolicy 수 있습니다. ID가 있는 후 FirewallPolicy 매개 변수 대신 *FirewallPolicyId* 매개 변수를 *사용할 수* 있습니다.
예를 들어 -FirewallPolicyId "/subscriptions/<구독-id>/resourceGroups/<리소스 그룹 id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "

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
이 cmdlet이 만드는 경로 규칙 구성의 이름을 지정합니다.

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

### -리디렉션 구성
애플리케이션 게이트웨이 리디렉션 구성

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

### -리디렉션ConfigurationId
애플리케이션 게이트웨이 리디렉션 구성의 ID

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
애플리케이션 게이트웨이 RewriteRuleSet의 ID

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

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


