---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876624"
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
Azure는 기본, 표준, 고성능, VpnGw1, VpnGw2 및 VpnGw3 Sku (간혹 소형, 중형, 대형 Sku 라고도 함)를 지원 합니다.
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

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
Type: PSVirtualNetworkGateway
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

###  
이 cmdlet은 **PSVirtualNetworkGateway** 개체의 파이프라인 인스턴스를 허용 합니다.

## 출력

###  
이 cmdlet은 **PSVirtualNetworkGateway** 개체의 기존 인스턴스를 수정 합니다.

## 상속자
기본/표준/HighPerformance Sku에서 new VpnGw1/VpnGw2/VpnGw3 Sku로 크기를 조정할 수 없습니다. https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways지침은을 참조 하세요.

## 관련 링크

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


