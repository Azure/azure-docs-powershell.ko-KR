---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192025"
---
# Add-AzNetworkSecurityRuleConfig

## SYNOPSIS
네트워크 보안 그룹에 네트워크 보안 규칙 구성을 추가합니다.

## 구문

### SetByResource(기본값)
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Add-AzNetworkSecurityRuleConfig** cmdlet은 Azure 네트워크 보안 그룹에 네트워크 보안 규칙 구성을 추가합니다.

## 예제

### 1: 네트워크 보안 그룹 추가
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

첫 번째 명령은 리소스 그룹 "rg1"에서 "nsg1"이라는 Azure 네트워크 보안 그룹을 검색합니다. 두 번째 명령은 포트 3389의 인터넷에서 검색된 네트워크 보안 그룹 개체로 트래픽을 허용하는 "rdp-rule"이라는 네트워크 보안 규칙을 추가합니다. 수정된 Azure 네트워크 보안 그룹을 유지 관리합니다.

### 2: 애플리케이션 보안 그룹을 통해 새 보안 규칙 추가
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

먼저 두 개의 새 애플리케이션 보안 그룹을 생성합니다. 그런 다음 리소스 그룹 "rg1"에서 "nsg1"이라는 Azure 네트워크 보안 그룹을 검색합니다. "rdp-rule"이라는 네트워크 보안 규칙을 추가합니다. 규칙은 애플리케이션 보안 그룹 "srcAsg"의 모든 IP 구성에서 포트 3389의 "destAsg"의 모든 IP 구성으로 트래픽을 허용합니다. 규칙을 추가한 후 수정된 Azure 네트워크 보안 그룹을 유지하게 됩니다.

## PARAMETERS

### -Access
네트워크 트래픽이 허용되거나 거부될지 여부를 지정합니다.
이 매개 변수에 허용되는 값은 허용 및 거부입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Description
네트워크 보안 규칙 구성에 대한 설명을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
대상 주소의 주소를 지정합니다.
이 매개 변수에 허용되는 값은
- CIDR(CIDR(Classless Interdomain Routing)) 주소
- 대상 IP 주소 범위
- IP 주소와 일치하는 와일드카드 문자(*)는 VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수 있습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
규칙에 대한 대상으로 설정된 애플리케이션 보안 그룹입니다. 'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
규칙에 대한 대상으로 설정된 애플리케이션 보안 그룹입니다. 'DestinationAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
대상 포트 또는 범위를 지정합니다.
이 매개 변수에 허용되는 값은
- 정수
- 0에서 65535 사이의 정수 범위
- 모든 포트와 일치하는 와일드카드 문자(*)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Direction
들어오는 트래픽 또는 외출 트래픽에서 규칙이 평가될지 여부를 지정합니다.
이 매개 변수에 허용되는 값은 인바운드 및 아웃바운드입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
네트워크 보안 규칙 구성의 이름을 지정합니다.

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

### -NetworkSecurityGroup
**NetworkSecurityGroup 개체를 지정합니다.**
이 cmdlet은 이 매개 변수가 지정하는 개체에 네트워크 보안 규칙 구성을 추가합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Priority
규칙 구성의 우선 순위를 지정합니다.
이 매개 변수에 허용되는 값은 100에서 4096 사이의 정수입니다.
우선 순위 번호는 컬렉션의 각 규칙에 대해 고유해야 합니다.
우선 순위 번호가 낮을수록 규칙의 우선 순위가 높아야 합니다.

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

### -Protocol
규칙 구성이 적용되는 네트워크 프로토콜을 지정합니다.
이 매개 변수에 허용되는 값은
- Tcp
- Udp
- 둘 다 일치할 와일드카드 문자(*)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
원본 주소의 주소를 지정합니다.
이 매개 변수에 허용되는 값은
- A CIDR
- 원본 IP 범위
- 모든 IP 주소와 일치하는 와일드카드 문자(*)입니다.
VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수도 있습니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
규칙의 원본으로 설정된 애플리케이션 보안 그룹입니다. 'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
규칙의 원본으로 설정된 애플리케이션 보안 그룹입니다. 'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
원본 포트 또는 범위를 지정합니다.
이 값은 0에서 65535 사이의 범위로 정수로 표현되거나 모든 원본 포트와 일치하기 위해 와일드카드 문자(*)로 표현됩니다.

```yaml
Type: System.String[]
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

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## 출력

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## 참고 사항

## 관련 링크

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


