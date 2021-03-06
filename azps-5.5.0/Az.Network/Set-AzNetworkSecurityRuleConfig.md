---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202451"
---
# Set-AzNetworkSecurityRuleConfig

## SYNOPSIS
네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다.

## 구문

### SetByResource(기본값)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Set-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다.

## 예제

### 예제 1: 네트워크 보안 규칙에서 액세스 구성 변경
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

첫 번째 명령은 NSG-FrontEnd라는 네트워크 보안 그룹을 인용한 다음, NSG-FrontEnd의 변수에 $nsg.
두 번째 명령은 파이프라인 연산자를 사용하여 rdp-rule이라는 보안 규칙 구성을 $nsg Get-AzNetworkSecurityRuleConfig에 보안 그룹을 전달합니다.
세 번째 명령은 rdp-rule의 액세스 구성을 거부로 변경합니다.

### 예제 2

네트워크 보안 그룹에 대한 네트워크 보안 규칙 구성을 업데이트합니다. (자동Generated)

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## PARAMETERS

### -Access
네트워크 트래픽을 허용하거나 거부할지 여부를 지정합니다. 이 매개 변수에 허용되는 값은 허용 및 거부입니다.

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
규칙 구성에 대한 설명을 지정합니다.
최대 크기는 140자입니다.

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
들어오는 트래픽 또는 외출 트래픽에 대해 규칙이 평가될지 여부를 지정합니다.
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
이 cmdlet이 설정하는 네트워크 보안 규칙 구성의 이름을 지정합니다.

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
설정할 네트워크 보안 규칙 구성을 포함하는 **NetworkSecurityGroup** 개체를 지정합니다.

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
이 매개 변수에 허용되는 값은 --Tcp입니다.
- Udp
- 둘 다 일치할 와일드카드 문자(*)입니다.

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
- IP 주소와 일치하는 와일드카드 문자(*)를 VirtualNetwork, AzureLoadBalancer 및 인터넷과 같은 태그를 사용할 수도 있습니다.

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
규칙에 대한 원본으로 설정된 애플리케이션 보안 그룹입니다. 'SourceAddressPrefix' 매개 변수와 함께 사용할 수 없습니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## 출력

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## 참고 사항

## 관련 링크

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


