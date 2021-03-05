---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: ddf0f6687550e544aa22efbce772c0751a7b810e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006000"
---
# Remove-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
가상 네트워크 게이트웨이에서 기본 사이트를 제거합니다.

## 구문

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet은 가상 네트워크 게이트웨이에서 강제 터널링 기본 사이트를 제거합니다.
강제 터널링은 Azure 가상 머신에서 인터넷 바인딩 트래픽을 프레미스 네트워크로 리디렉션하는 방법을 제공합니다. 이렇게 하면 트래픽을 발매하기 전에 트래픽을 검사하고 감사할 수 있습니다.
강제 터널링은 VPN(가상 사설망) 터널을 사용하여 수행됩니다. 이 터널에는 모든 Azure 인터넷 바인딩 트래픽이 리디렉션되는 로컬 게이트웨이인 기본 사이트가 필요합니다.
**Remove-AzVirtualNetworkGatewayDefaultSite는** 게이트웨이에 할당된 기본 사이트를 제거합니다.
이렇게 하면 게이트웨이를 강제 터널링에 Set-AzVirtualNetworkGatewayDefaultSite 전에 새 기본 사이트를 할당하기 위해 새 사이트를 사용해야 합니다.

## 예제

### 예제 1: 가상 네트워크 게이트웨이에 할당된 기본 사이트 제거
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

이 예제에서는 ContosoVirtualGateway라는 가상 네트워크 게이트웨이에 현재 할당된 기본 사이트를 제거합니다.
첫 번째 명령은 **Get-AzVirtualNetworkGateway를 사용하여** 게이트웨이에 대한 개체 참조를 만듭니다. 이 개체 참조는 이라는 변수에 $Gateway.
그런 다음 두 번째 명령은 **Remove-AzVirtualNetworkGatewayDefaultSite를 사용하여** 해당 게이트웨이에 할당된 기본 사이트를 제거합니다.

## 매개 변수

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

### -VirtualNetworkGateway
제거할 기본 사이트를 포함하는 가상 네트워크 게이트웨이에 대한 개체 참조를 지정합니다.
가상 네트워크 게이트웨이에 대한 개체 참조를 Get-AzVirtualNetworkGateway 게이트웨이 이름을 지정할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## 참고 사항

## 관련 링크

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayDefaultSite](./Set-AzVirtualNetworkGatewayDefaultSite.md)


