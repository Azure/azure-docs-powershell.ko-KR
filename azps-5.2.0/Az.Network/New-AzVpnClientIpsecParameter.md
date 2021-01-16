---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: f57c3d4711fe0c05e79f0d7dbeca897475f78421
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327557"
---
# New-AzVpnClientIpsecParameter

## SYNOPSIS
이 명령을 사용하면 사용자가 IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup과 같은 하나 또는 모든 값을 지정하여 Vpn ipsec 매개 변수 개체를 만들어 기존 VPN 게이트웨이에 설정할 수 있습니다.

## 구문

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
이 명령을 사용하면 사용자가 IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup과 같은 하나 또는 모든 값을 지정하여 Vpn ipsec 매개 변수 개체를 만들어 기존 VPN 게이트웨이에 설정할 수 있습니다.

## 예제

### 예제 1
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

New-AzVpnClientIpsecParameter cmdlet은 사용자가 ResourceGroup의 기존 가상 네트워크 게이트웨이에 대해 설정할 수 있는 전달된 하나 또는 모든 매개 변수 값을 사용하는 vpn ipsec 매개 변수 개체를 만드는 데 사용됩니다.
이 생성한 VpnClientIPsecParameters 개체는 Set-AzVpnClientIpsecParameter 예제와 같이 가상 네트워크 게이트웨이에서 지정된 Vpn ipsec 사용자 지정 정책을 설정하는 Set-AzVpnClientIpsecParameter 명령으로 전달됩니다. 이 명령은 설정된 매개 변수를 표시하는 VpnClientIPsecParameters의 개체를 반환합니다.

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

### -DhGroup
IKE 1단계에서 초기 SA에 사용되는 VpnClient DH 그룹입니다.

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
VpnClient IKE 암호화 알고리즘(IKE 2단계)

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
VpnClient IKE 무결성 알고리즘(IKE 2단계)

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

### -IpsecEncryption
VpnClient IPSec 암호화 알고리즘(IKE 1단계)

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

### -IpsecIntegrity
VpnClient IPSec 무결성 알고리즘(IKE 1단계)

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
새 자식 SA에 대한 IKE 2단계에서 사용되는 VpnClient PFS 그룹

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
VpnClient IPSec 보안 연결(빠른 모드 또는 2단계 SA라고도 하는) 페이로드 크기(KB)

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
VpnClient IPSec 보안 연결(빠른 모드 또는 2단계 SA라고도 하는) 수명(초)

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

## 참고 사항

## 관련 링크

[Get-AzVpnClientIpsecParameter](./Get-AzVpnClientIpsecParameter.md)

[Remove-AzVpnClientIpsecParameter](./Remove-AzVpnClientIpsecParameter.md)

[Set-AzVpnClientIpsecParameter](./Set-AzVpnClientIpsecParameter.md)
