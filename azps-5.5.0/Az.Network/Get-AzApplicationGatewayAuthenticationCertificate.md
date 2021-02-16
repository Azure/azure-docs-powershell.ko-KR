---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 00d5d84f3f9895aec42f9728de6eec1bf2ff9b06
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189921"
---
# Get-AzApplicationGatewayAuthenticationCertificate

## SYNOPSIS
애플리케이션 게이트웨이에 대한 인증 인증서를 얻습니다.

## 구문

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzApplicationGatewayAuthenticationCertificate** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 인증 인증서를 얻습니다.

## 예제

### 예제 1: 지정된 인증 인증서를 얻게 됩니다.
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

첫 번째 명령은 appGwName이라는 애플리케이션 게이트웨이를 $appgw 변수에 저장합니다.
두 번째 명령은 cert01이라는 인증 인증서를 사용하여 $cert 변수에 저장합니다.

## PARAMETERS

### -ApplicationGateway
이 cmdlet이 인증 인증서를 받을 애플리케이션 게이트웨이의 이름을 지정합니다.

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

### -Name
이 cmdlet에서 얻을 인증 인증서의 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate

## 참고 사항
* 키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹

## 관련 링크

[Add-AzApplicationGatewayAuthenticationCertificate](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[New-AzApplicationGatewayAuthenticationCertificate](./New-AzApplicationGatewayAuthenticationCertificate.md)

[Remove-AzApplicationGatewayAuthenticationCertificate](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[Set-AzApplicationGatewayAuthenticationCertificate](./Set-AzApplicationGatewayAuthenticationCertificate.md)


