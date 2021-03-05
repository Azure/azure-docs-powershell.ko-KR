---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 367e54036d7665cf59ebcc6f1a10b3060b97580d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991018"
---
# Remove-AzApplicationGatewayPrivateLinkConfiguration

## SYNOPSIS
애플리케이션 게이트웨이에서 privateLink 구성을 제거합니다.

## 구문

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에서 privateLink 구성을 제거합니다.

## 예제

### 예제 1: 애플리케이션 게이트웨이 PrivateLink 구성 제거
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $AppGw 변수에 저장합니다.
두 번째 명령은 에 저장된 애플리케이션 게이트웨이에서 privateLinkConfig01이라는 privateLink 구성을 $AppGw.

## 매개 변수

### -ApplicationGateway
ApplicationGateway

```yaml
Type: PSApplicationGateway
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
애플리케이션 게이트웨이 privateLink 구성의 이름

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## 출력

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## 참고 사항

## 관련 링크

[New-AzApplicationGatewayPrivateLinkConfiguration](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[Add-AzApplicationGatewayPrivateLinkConfiguration](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[Get-AzApplicationGatewayPrivateLinkConfiguration](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[Set-AzApplicationGatewayPrivateLinkConfiguration](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)