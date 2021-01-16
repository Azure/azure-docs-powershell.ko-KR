---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331742"
---
# Set-AzVirtualNetworkGatewayDefaultSite

## SYNOPSIS
가상 네트워크 게이트웨이에 대한 기본 사이트를 설정합니다.

## 구문

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzVirtualNetworkGatewayDefaultSite** cmdlet은 강제 터널링 기본 사이트를 가상 네트워크 게이트웨이에 할당합니다.
강제 터널링은 Azure 가상 머신에서 인터넷에 바인딩된 트래픽을 사용자-프레미스 네트워크로 리디렉션하는 방법을 제공합니다. 이렇게 하면 트래픽을 발매하기 전에 검사하고 감사할 수 있습니다.
강제 터널링은 VPN(가상 사설망) 터널을 사용하여 수행됩니다. 이 터널에는 모든 Azure 인터넷 바인딩 트래픽이 리디렉션되는 로컬 게이트웨이인 기본 사이트가 필요합니다.
**Set-AzVirtualNetworkGatewayDefaultSite는** 게이트웨이에 할당된 기본 사이트를 변경하는 방법을 제공합니다.

## 예제

### 예제 1: 가상 네트워크 게이트웨이에 기본 사이트 할당
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

이 예제에서는 ContosoVirtualGateway라는 가상 네트워크 게이트웨이에 기본 사이트를 할당합니다.
첫 번째 명령은 ContosoLocalGateway라는 로컬 게이트웨이에 대한 개체 참조를 만듭니다.
$LocalGateway 변수에 저장된 이 개체 참조는 기본 사이트로 구성할 게이트웨이를 나타냅니다.
그런 다음 두 번째 명령은 가상 네트워크 게이트웨이에 대한 개체 참조를 만들고 결과를 가상 네트워크 게이트웨이라는 변수에 $VirtualGateway.
세 번째 명령은 **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet을 사용하여 ContosoVirtualGateway에 기본 사이트를 할당합니다.

## PARAMETERS

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

### -GatewayDefaultSite
지정된 가상 네트워크에 대한 기본 사이트로 할당할 로컬 네트워크 게이트웨이에 대한 개체 참조를 지정합니다.
Get-AzLocalNetworkGateway cmdlet을 사용하여 로컬 게이트웨이에 대한 개체 참조를 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
기본 사이트가 할당될 가상 네트워크 게이트웨이에 대한 개체 참조를 지정합니다.
**Get-AzVirtualNetworkGateway를** 사용하고 게이트웨이 이름을 지정하여 가상 네트워크 게이트웨이에 대한 개체 참조를 만들 수 있습니다.
그런 다음 $VirtualGateway *VirtualNetworkGateway* 매개 변수에 대한 매개 변수 값으로 사용할 수 있습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## 참고 사항

## 관련 링크

[Get-AzLocalNetworkGateway](./Get-AzLocalNetworkGateway.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGatewayDefaultSite](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


