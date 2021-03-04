---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4b2963d77d2182821bb4950907ef278950e410f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958155"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
기존 가상 네트워크 게이트웨이의 수를 변경합니다.

## 구문

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Resize-AzVirtualNetworkGateway** cmdlet을 사용하면 가상 네트워크 게이트웨이에 대한 SKU(재고 유지 단위)를 변경할 수 있습니다.
SKUS는 허용되는 최대 IP 터널 수와 같은 데이터와 같은 게이트웨이의 기능을 결정합니다.
Azure는 기본, 표준, 고성능, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUS(중소형 및 대규모 SKUS라고도도 합니다)를 지원합니다.
각 SKU 형식의 기능에 대한 자세한 내용은 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 를 참조하세요.
SKUS는 가격 책정뿐만 아니라 기능도 다르다는 점에 유의합니다.
자세한 내용은 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 를 참조하세요.

## 예제

### 예제 1: 가상 네트워크 게이트웨이의 크기 변경
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

이 예제에서는 ContosoVirtualGateway라는 가상 네트워크 게이트웨이의 크기를 변경합니다.
첫 번째 명령은 ContosoVirtualGateway에 대한 개체 참조를 만듭니다. 이 개체 참조는 이라는 변수에 $Gateway.
그런 다음 두 번째 명령은 **Resize-AzVirtualNetworkGateway** cmdlet을 사용하여 *GatewaySku* 속성을 Basic으로 설정합니다.

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

### -GatewaySku
새 형식의 게이트웨이 SKU를 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 기본
- 표준
- 고성능
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
변경될 가상 네트워크 게이트웨이에 대한 개체 참조를 지정합니다.
이 개체 참조는 Get-AzVirtualNetworkGateway 게이트웨이 이름을 지정하여 만들 수 있습니다.

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

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## 참고 사항
Basic/Standard/HighPerformance SKUS에서 새 VpnGw1/VpnGw2/VpnGw3 SKUS로는 변경할 수 없습니다. VpnGw1AZ/VpnGw2AZ/VpnGw3AZ 또는 ErGw1AZ/ErGw2AZ/ErGw2AZ/ErGw3AZ로의 추가 변경은 허용되지 않습니다. SKU '시리즈' 내에서만 사용할 수 있습니다(예: VpnGw1AZ는 VpnGw2AZ/VpnGw3AZ 및 ErGw1AZ에서 ErGw2AZ/ErGw3AZ로의 재조정할 수 있습니다. 지침을 https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpngateways 참조하세요.

## 관련 링크

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
