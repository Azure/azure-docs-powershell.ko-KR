---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531973"
---
# Set-AzureRmVirtualNetworkGateway

## SYNOPSIS
가상 네트워크 게이트웨이를 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 기본값 (기본값)
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RadiusServerConfiguration
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVirtualNetworkGateway** cmdlet은 가상 네트워크 게이트웨이를 업데이트 합니다.

## 예제의

### 예제 1: 목표 상태 설정 가상 네트워크 게이트웨이
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져와 $Gateway 이라는 변수에 저장 하 고 두 번째 명령은 변수 $Gateway에 저장 된 가상 네트워크 게이트웨이의 목표 상태를 설정 합니다.
또한이 명령은 ASN을 1337로 설정 합니다.

### 예제 2: 목표 상태 설정 가상 네트워크 게이트웨이
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

첫 번째 명령은 리소스 그룹 ResourceGroup001에 속한 Gateway01 이라는 가상 네트워크 게이트웨이를 가져오고, 두 번째 명령은 지정 된 ipsec 매개 변수로 Vpn ipsec 정책 개체를 만드는 $Gateway 명명 된 변수에 저장 합니다.
세 번째 명령은 변수 $Gateway에 저장 된 가상 네트워크 게이트웨이의 목표 상태를 설정 합니다.
또한이 명령은 가상 네트워크 게이트웨이의 $vpnclientipsecpolicy 개체에 지정 된 사용자 지정 vpn ipsec 정책을 설정 합니다.

## 변수

### -AsJob
백그라운드에서 cmdlet 실행

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Asn
IPsec 터널 내에서 BGP (Border Gateway Protocol) 세션을 설정 하는 데 사용 되는 가상 ASN (네트워크 게이트웨이 익명 시스템 번호)을 지정 합니다.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DisableActiveActiveFeature
활성 활성 기능을 사용 하지 않도록 설정 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableActiveActiveFeature
활성 활성 기능을 사용 하도록 설정 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -게이트웨이 Defaultsite
강제 터널링에 사용할 기본 사이트를 지정 합니다.
기본 사이트를 지정 하면 게이트웨이의 VPN (가상 사설망)에 있는 모든 인터넷 트래픽이 해당 사이트로 라우팅됩니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -게이트웨이 Sku
가상 네트워크 게이트웨이의 SKU (stock 보관 단위)를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 기본적
- 표준이
- HighPerformance
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

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PeerWeight
이 가상 네트워크 게이트웨이에서 BGP를 통해 얻은 경로에 추가 된 가중치를 지정 합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusServerAddress
P2S 외부 Radius 서버 주소입니다.

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusServerSecret
P2S 외부 Radius 서버 비밀.

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
수정이 해제 되는 가상 네트워크 게이트웨이 개체를 지정 합니다.
Get-AzureRmVirtualNetworkGateway cmdlet을 사용 하 여 가상 네트워크 게이트웨이 개체를 가져올 수 있습니다.

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

### -VpnClientAddressPool
이 cmdlet이 VPN 클라이언트 IP 주소를 할당 하는 데 사용 하는 주소 공간을 지정 합니다.
이는 가상 네트워크 또는 온-프레미스 범위와 중복 되어서는 안 됩니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientIpsecPolicy
P2S VPN 클라이언트 터널링 프로토콜에 대 한 IPSec 정책 목록입니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientProtocol
P2S VPN 클라이언트 터널링 프로토콜 목록

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRevokedCertificates
해지 된 VPN 클라이언트 인증서 목록을 지정 합니다.
이들 중 하 나와 일치 하는 인증서를 제시 하는 VPN 클라이언트는 제거 됩니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRootCertificates
VPN 클라이언트 인증에 사용할 VPN 클라이언트 루트 인증서의 목록을 지정 합니다.
VPN 클라이언트를 연결 하는 것은 이러한 루트 인증서 중 하나에서 생성 된 인증서를 제공 해야 합니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSVirtualNetworkGateway에 대 한.
매개 변수: VirtualNetworkGateway (ByValue)

### System. 문자열

### Microsoft. 네트워크. PSLocalNetworkGateway

### System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]

### System.webserver. List ' 1 [[PSVpnClientRootCertificate, Microsoft azure. 6.4.1.0,. *. *. *. e l e = 중립, PublicKeyToken = null]]

### System.webserver. List ' 1 [[PSVpnClientRevokedCertificate, Microsoft azure. 6.4.1.0,. *. *. *. e l e = 중립, PublicKeyToken = null]]

### System.webserver. List ' 1 [[PSIpsecPolicy, Microsoft azure. 6.4.1.0,. *. *. *. e l e = 중립, PublicKeyToken = null]]

### 시스템. UInt32

### 시스템. i i.

### System.webserver

## 출력

### PSVirtualNetworkGateway에 대 한.

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹

## 관련 링크

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[새로운 AzureRmVirtualNetworkGateway](./New-AzureRmVirtualNetworkGateway.md)

[제거-AzureRmVirtualNetworkGateway](./Remove-AzureRmVirtualNetworkGateway.md)

[다시 설정-AzureRmVirtualNetworkGateway](./Reset-AzureRmVirtualNetworkGateway.md)

[크기 조정-AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)


