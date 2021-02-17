---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184244"
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
**Resize-AzVirtualNetworkGateway** cmdlet을 사용하면 가상 네트워크 게이트웨이에 대한 SKU(주식 유지 단위)를 변경할 수 있습니다.
SKUS는 허용되는 최대 IP 터널 수 및 같은 것을 포함하여 게이트웨이의 기능을 파악합니다.
Azure는 Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUS(Small, Medium 및 Large SKUS라고도 합니다)를 지원
각 SKU 유형의 기능에 대한 자세한 내용은 다음을 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 참조하세요.
SKUS는 가격 책정 및 기능도 다릅니다.
자세한 내용은 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 다음을 참조하세요.

## 예제

### 예제 1: 가상 네트워크 게이트웨이의 크기 변경
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

이 예제에서는 ContosoVirtualGateway라는 가상 네트워크 게이트웨이의 크기를 변경합니다.
첫 번째 명령은 ContosoVirtualGateway에 대한 개체 참조를 만듭니다. 이 개체 참조는 $Gateway.
두 번째 명령은 **Resize-AzVirtualNetworkGateway** cmdlet을 사용하여 *GatewaySku* 속성을 Basic으로 설정합니다.

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

### -GatewaySku
새 유형의 게이트웨이 SKU를 지정합니다.
이 매개 변수에 허용되는 값은
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
이 개체 참조는 Get-AzVirtualNetworkGateway 게이트웨이의 이름을 지정하여 만들 수 있습니다.

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

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

## 참고 사항
Basic/Standard/HighPerformance SKUS에서 새 VpnGw1/VpnGw2/VpnGw3 SKUS로는 변경할 수 없습니다. VpnGw1AZ/VpnGw2AZ/VpnGw3AZ 또는 ErGw1AZ/ErGw2AZ/ErGw2AZ/ErGw3AZ에서/VpnGw3AZ로/에 대한 추가적 재조정은 허용되지 않습니다. SKU '시리즈' 내에서만 허용됩니다. 예: VpnGw1AZ는 VpnGw2AZ/VpnGw3AZ에서 또는 VpnGw3AZ에서, ErGw1AZ는 ErGw2AZ/ErGw3AZ에서 또는 그에 대한/ErGw3AZ로 또는 그 범위에서 ErGw1AZ로 또는 그에 대한/ErGw3AZ로 또는 그에 대한/ErGw1AZ로 또는 그에 대한 또는 그에 대한 재조정을 할 수 있습니다. 지침을 https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways 참조하세요.

## 관련 링크

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[New-AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[Remove-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[Reset-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
