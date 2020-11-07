---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 1456afca27b6a5993fa014b738c415af5db98c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703449"
---
# Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration

## SYNOPSIS
응용 프로그램 게이트웨이의 WAF 구성을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet은 응용 프로그램 게이트웨이의 waf (웹 응용 프로그램 방화벽) 구성을 가져옵니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이 웹 응용 프로그램 방화벽 구성 가져오기
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGW 변수에 저장 합니다.
두 번째 명령은 $AppGW에서 응용 프로그램 게이트웨이의 방화벽 구성을 가져온 다음 $FirewallConfig에 저장 합니다.

## 변수

### -ApplicationGateway
응용 프로그램 게이트웨이 개체를 지정 합니다.
Get-AzureRmApplicationGateway cmdlet을 사용 하 여 응용 프로그램 게이트웨이 개체를 가져올 수 있습니다.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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

### Microsoft. * PSApplicationGateway
매개 변수: ApplicationGateway (ByValue)

## 출력

### PSApplicationGatewayWebApplicationFirewallConfiguration에 대 한.

## 상속자

## 관련 링크

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[새로운 AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


