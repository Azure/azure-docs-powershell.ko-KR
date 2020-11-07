---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
ms.openlocfilehash: 95865de8e99ad09a755329b742f69ebe1e935d72
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880389"
---
# New-AzureRmApplicationGatewayPathRuleConfig

## SYNOPSIS
응용 프로그램 게이트웨이 경로 규칙을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### SetByResourceId
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**새 AzureRmApplicationGatewayPathRuleConfig** cmdlet은 응용 프로그램 게이트웨이 경로 규칙을 만듭니다.
이 cmdlet에서 만든 규칙을 URL 경로 맵 구성 설정 컬렉션에 추가 하 고 게이트웨이에 할당할 수 있습니다.

경로 맵 구성 설정은 응용 프로그램 게이트웨이 부하 분산에 사용 됩니다.

## 예제의

### 예제 1
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

이러한 명령은 새 응용 프로그램 게이트웨이 경로 규칙을 만든 다음 **추가-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet을 사용 하 여 해당 규칙을 응용 프로그램 게이트웨이에 할당 합니다.
이렇게 하려면 첫 번째 명령은 게이트웨이 ContosoApplicationGateway에 대 한 개체 참조를 만듭니다.
이 개체 참조는 $Gateway 라는 변수에 저장 됩니다.

다음 두 명령은 백 엔드 주소 풀 및 백 엔드 HTTP 설정 개체를 만듭니다. 경로 규칙 개체를 만들기 위해서는 이러한 개체 (변수 $AddressPool 및 $HttpSettings에 저장)가 필요 합니다.

네 번째 명령은 path 규칙 개체를 만들고 $PathRuleConfig 라는 변수에 저장 됩니다.

다섯 번째 명령은 **AzureRmApplicationGatewayUrlPathMapConfig 추가** 를 사용 하 여 구성 설정 및 해당 설정에 포함 된 새 경로 규칙을 ContosoApplicationGateway에 추가 합니다.

## 변수

### -BackendAddressPool
게이트웨이 경로 규칙 구성 설정에 추가할 백 엔드 주소 풀 설정 컬렉션에 대 한 개체 참조를 지정 합니다.
다음과 같은 New-AzureRmApplicationGatewayBackendAddressPool cmdlet 및 구문을 사용 하 여이 개체 참조를 만들 수 있습니다.

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

앞의 명령은 두 개의 IP 주소 (192.16.1.1 및 192.168.1.2)를 주소 풀에 추가 합니다.
IP 주소는 인용 부호로 묶여 있고 쉼표로 구분 됩니다.

결과 변수인 $AddressPool는 *DefaultBackendAddressPool* 매개 변수의 매개 변수 값으로 사용할 수 있습니다.

백 엔드 주소 풀은 백 엔드 서버의 IP 주소를 나타냅니다.
이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소 여야 합니다.
이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 없습니다.

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백엔드 주소 풀의 ID를 지정 합니다.
주소 풀 Id는 Get-AzureRmApplicationGatewayBackendAddressPool cmdlet을 사용 하 여 반환할 수 있습니다.
ID를 설정한 후에는 *DefaultBackendAddressPool* 매개 변수 대신 *DefaultBackendAddressPoolId* 매개 변수를 사용할 수 있습니다.
예를 들면 다음과 같습니다.

-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"

백 엔드 주소 풀은 백 엔드 서버의 IP 주소를 나타냅니다.
이러한 IP 주소는 가상 네트워크 서브넷에 속하거나 공용 IP 주소 여야 합니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettings
게이트웨이 경로 규칙 구성 설정에 추가할 백 엔드 HTTP 설정 컬렉션에 대 한 개체 참조를 지정 합니다.
다음과 같은 New-AzureRmApplicationGatewayBackendHttpSettings cmdlet 및 구문을 사용 하 여이 개체 참조를 만들 수 있습니다.

$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-포트 80-프로토콜 "Http"-CookieBasedAffinity "Disabled"

그런 다음 *DefaultBackendAddressPool* 매개 변수에 대 한 매개 변수 값으로 결과 변수 $HttpSettings를 사용할 수 있습니다.

-DefaultBackendHttpSettings $HttpSettings

백 엔드 HTTP 설정은 포트, 프로토콜 및 백 엔드 풀에 대 한 쿠키 기반 선호도와 같은 속성을 구성 합니다.
이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendHttpSettingsId* 매개 변수를 사용할 수 없습니다.

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
게이트웨이 경로 규칙 구성 설정에 추가할 수 있는 기존 백 엔드 HTTP 설정 컬렉션의 ID를 지정 합니다.
HTTP 설정 Id는 Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet을 사용 하 여 반환할 수 있습니다.
ID를 설정한 후에는 *DefaultBackendHttpSettings* 매개 변수 대신 *DefaultBackendHttpSettingsId* 매개 변수를 사용할 수 있습니다.
예를 들면 다음과 같습니다.

-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"

백 엔드 HTTP 설정은 포트, 프로토콜 및 백 엔드 풀에 대 한 쿠키 기반 선호도와 같은 속성을 구성 합니다.
이 매개 변수를 사용 하는 경우 동일한 명령에서 *DefaultBackendHttpSettings* 매개 변수를 사용할 수 없습니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
이 cmdlet이 만드는 경로 규칙 구성의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -경로
하나 이상의 응용 프로그램 게이트웨이 경로 규칙을 지정 합니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.

```yaml
Type: String
Parameter Sets: SetByResourceId
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

###  
**New-AzureRmApplicationGatewayPathRuleConfig** 는 파이프라인 입력을 허용 하지 않습니다.

## 출력

###  
AzureRmApplicationGatewayPathRuleConfig- **PSApplicationGatewayPathRule** 개체의 새 인스턴스를 만듭니다 **(새)** .

## 상속자

## 관련 링크

[추가-AzureRmApplicationGatewayUrlPathMapConfig](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Get-AzureRmApplicationGatewayUrlPathMapConfig](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[새로운 AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[새로운 AzureRmApplicationGatewayBackendHttpSettings](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[새로운 AzureRmApplicationGatewayPathRuleConfig](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[새로운 AzureRmApplicationGatewayUrlPathMapConfig](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[제거-AzureRmApplicationGatewayUrlPathMapConfig](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Set-AzureRmApplicationGatewayUrlPathMapConfig](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


