---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: bfa6e32ce51022cf208e40238bfe10b3fafe8933
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869821"
---
# New-AzVpnClientIpsecPolicy

## SYNOPSIS
사용자는이 명령을 사용 하 여 VPN 게이트웨이에서 설정 되는 Ipsec ipsec 정책 개체를 만들어 (IkeEncryption Encryption, Ipsec Integrity,, IkeIntegrity, DhGroup, PfsGroup 등의 값을 하나 또는 모두 지정할 수 있습니다. 이 명령은 output 개체를 사용 하 여 새/기존 게이트웨이 모두에 대 한 vpn ipsec 정책을 설정 합니다.

## 구문과

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
사용자는이 명령을 사용 하 여 VPN 게이트웨이에서 설정 되는 Ipsec ipsec 정책 개체를 만들어 (IkeEncryption Encryption, Ipsec Integrity,, IkeIntegrity, DhGroup, PfsGroup 등의 값을 하나 또는 모두 지정할 수 있습니다. 이 명령은 output 개체를 사용 하 여 새/기존 게이트웨이 모두에 대 한 vpn ipsec 정책을 설정 합니다.

## 예제의

### Vpn ipsec 정책 개체 정의:
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

이 cmdlet은 전달 된 하나 또는 모든 매개 변수를 사용 하 여 vpn ipsec 정책 개체를 생성 하는 데 사용 됩니다. VpnClientIpsecPolicy 명령: p r o m a t:에 New-AzVirtualNetworkGateway (새 VPN 게이트웨이 만들기)/Set-AzVirtualNetworkGateway (기존 VPN 게이트웨이 업데이트) ResourceGroup의 리소스 수:

### Vpn 사용자 지정 ipsec 정책 설정을 사용 하 여 새 가상 네트워크 게이트웨이 만들기:
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

이 cmdlet은 생성 후 가상 네트워크 게이트웨이 개체를 반환 합니다. 

### 기존 가상 네트워크 게이트웨이에서 vpn 사용자 지정 ipsec 정책 설정:
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

이 cmdlet은 vpn 사용자 지정 ipsec 정책을 설정한 후 가상 네트워크 게이트웨이 개체를 반환 합니다.

### Vpn 사용자 지정 정책이 올바르게 설정 되어 있는지 확인 하려면 가상 네트워크 게이트웨이를 가져옵니다.
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

이 cmdlet은 가상 네트워크 게이트웨이 개체를 반환 합니다.

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

### -DhGroup
초기 SA에 대 한 IKE 단계 1에 사용 되는 VpnClient DH 그룹

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeEncryption
VpnClient IKE 암호화 알고리즘 (IKE 단계 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
VpnClient IKE 무결성 알고리즘 (IKE 단계 2)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -암호 암호화
VpnClient IPSec 암호화 알고리즘 (IKE 단계 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -계층 무결성
VpnClient IPSec 무결성 알고리즘 (IKE 단계 1)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
새 자식 SA에 대 한 IKE 단계 2에 사용 되는 VpnClient PFS 그룹

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
VpnClient IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 페이로드 크기 (KB)

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
VpnClient IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 수명이 초 단위입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### PSIpsecPolicy에 대 한.

## 상속자

## 관련 링크
