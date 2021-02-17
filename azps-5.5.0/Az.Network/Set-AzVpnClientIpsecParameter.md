---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202416"
---
# Set-AzVpnClientIpsecParameter

## SYNOPSIS
기존 가상 네트워크 게이트웨이에 대한 vpn ipsec 매개 변수를 설정합니다.

## 구문

### ByFactoryName(기본값)
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzVpnClientIpsecParameter** cmdlet은 기존 가상 네트워크 게이트웨이에 대한 vpn ipsec 매개 변수를 설정합니다.
가상 네트워크 게이트웨이가 만들어질 때 게이트웨이에서 기본 vpn ipsec 정책 집합을 설정합니다. 지점 및 사이트간 사용자가 특정 사용자 지정 ipsec 정책을 사용하여 VPN Gateway에 연결하려는 경우 사용자는 먼저 VPN Gateway에서 해당 ipsec 정책을 설정해야 합니다. **Set-AzVpnClientIpsecParameter는** 이를 위해 방법을 제공합니다.

## 예제

### 예제 1: 사용자 지정 vpn ipsec 정책을 기존 가상 네트워크 게이트웨이로 설정합니다.
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

이 예제에서는 ContosoResourceGroup이라는 리소스 그룹에서 ContosoVirtualGateway라는 기존 가상 네트워크 게이트웨이에 사용자 지정 vpn ipsec 정책을 설정합니다.
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

### -InputObject
가상 네트워크 게이트웨이 개체

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Azure 리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
가상 네트워크 게이트웨이 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VpnClientIPsecParameter
Vpn 클라이언트 ipsec 매개 변수입니다. 이 매개 변수 값은 PS 명령 let:New-AzVpnClientIpsecParameter를 사용하여 구성할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters

## 참고 사항

## 관련 링크

[Get-AzVpnClientIpsecParameter](./Get-AzVpnClientIpsecParameter.md)

[New-AzVpnClientIpsecParameter](./New-AzVpnClientIpsecParameter.md)

[Remove-AzVpnClientIpsecParameter](./Remove-AzVpnClientIpsecParameter.md)
