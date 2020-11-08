---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043933"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
기존 가상 네트워크 게이트웨이의 크기를 조정 합니다.

## 구문과

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**크기 조정-AzVirtualNetworkGateway** cmdlet을 사용 하 여 가상 네트워크 게이트웨이의 SKU (stock 보관 단위)를 변경할 수 있습니다.
Sku는 처리량, 허용 되는 최대 IP 터널 수 등의 게이트웨이 기능을 결정 합니다.
Azure는 Basic, Standard, 고성능, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ Sku (간혹 소형, 중형, 대형 Sku 라고도 함)를 지원 합니다.
각 SKU 유형의 기능에 대 한 자세한 내용은을 참조 https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ 하세요.
Sku는 가격 및 기능에 차이가 있다는 점에 유의 하세요.
자세한 내용은을 참조 https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ 하세요.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이의 크기 변경
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

이 예제에서는 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이의 크기를 변경 합니다.
첫 번째 명령은 ContosoVirtualGateway에 대 한 개체 참조를 만듭니다. 이 개체 참조는 $Gateway 라는 변수에 저장 됩니다.
그런 다음 두 번째 명령은 **AzVirtualNetworkGateway** cmdlet을 사용 하 여 하이 *속성을* Basic으로 설정 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -게이트웨이 Sku
게이트웨이 SKU의 새로운 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 기본적
- 표준이
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
크기를 조정할 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.
Get-AzVirtualNetworkGateway를 사용 하 고 게이트웨이의 이름을 지정 하 여이 개체 참조를 만들 수 있습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSVirtualNetworkGateway에 대 한.

### System. 문자열

## 출력

### PSVirtualNetworkGateway에 대 한.

## 상속자
기본/표준/HighPerformance Sku에서 new VpnGw1/VpnGw2/VpnGw3 Sku로 크기를 조정할 수 없습니다. VpnGw1AZ/VpnGw2AZ/VpnGw3AZ 또는 ErGw1AZ/ErGw2AZ/ErGw3AZ에는 추가 크기 조정이 허용 되지 않습니다. 크기 조정에는 SKU ' 계열 '에만 사용할 수 있습니다. 예를 들어 VpnGw1AZ에서 VpnGw2AZ/VpnGw3AZ로 크기를 조정 하거나 ErGw1AZ에서 ErGw2AZ/ErGw3AZ로 크기를 조정할 수 있습니다. https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways지침은을 참조 하세요.

## 관련 링크

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[새로운 AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[제거-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[다시 설정-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
