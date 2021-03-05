---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: d3f774b078c1069fc5a2c2690996837f17a4c187
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994098"
---
# Get-AzApplicationGatewayPrivateLinkConfiguration

## SYNOPSIS
애플리케이션 게이트웨이의 개인 링크 구성을 얻습니다.

## 구문

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 애플리케이션 게이트웨이의 개인 링크 구성을 얻습니다.

## 예제

### 예제 1 : 지정된 개인 링크 구성을 다운로드합니다.
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.
두 번째 명령은 $AppGw privateLinkConfig01이라는 개인 링크 구성을 $PrivateLinkConfiguration 변수에 저장합니다.

### 예제 2 : 개인 링크 구성 목록 다운로드
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.
두 번째 명령은 $AppGw 모든 개인 링크 구성을 $PrivateLinkConfigurations 변수에 저장합니다.

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration

## 참고 사항

## 관련 링크

[New-AzApplicationGatewayPrivateLinkConfiguration](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[Add-AzApplicationGatewayPrivateLinkConfiguration](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[Remove-AzApplicationGatewayPrivateLinkConfiguration](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[Set-AzApplicationGatewayPrivateLinkConfiguration](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)