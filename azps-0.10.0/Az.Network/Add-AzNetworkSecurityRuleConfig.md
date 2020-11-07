---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: b2b1667a9326a9c25d78639e397146c0dd85dc5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875663"
---
# Add-AzNetworkSecurityRuleConfig

## SYNOPSIS
네트워크 보안 규칙 구성을 네트워크 보안 그룹에 추가 합니다.

## 구문과

### SetByResource (기본값)
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**추가-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 규칙 구성을 Azure 네트워크 보안 그룹에 추가 합니다.

## 예제의

### 1: 네트워크 보안 그룹 추가
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

첫 번째 명령은 리소스 그룹 "rg1"에서 "nsg1" 이라는 Azure 네트워크 보안 그룹을 검색 합니다. 두 번째 명령은 포트 3389의 인터넷에서 검색 된 네트워크 보안 그룹 개체에 트래픽을 허용 하는 "rdp-tcp" 라는 네트워크 보안 규칙을 추가 합니다. 수정 된 Azure 네트워크 보안 그룹을 유지 합니다.

### 1: 응용 프로그램 보안 그룹을 사용 하 여 새 보안 규칙 추가
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

먼저 두 가지 새로운 응용 프로그램 보안 그룹을 만듭니다. 그런 다음 리소스 그룹 "rg1"에서 "nsg1" 이라는 Azure 네트워크 보안 그룹을 검색 합니다. ".rdp-rule" 이라는 네트워크 보안 규칙을 추가 합니다. 이 규칙은 응용 프로그램 보안 그룹 "srcAsg"의 모든 IP 구성에서 포트 3389에 있는 "destAsg"의 모든 IP 구성에 대 한 트래픽을 허용 합니다. 규칙을 추가한 후에는 수정 된 Azure 네트워크 보안 그룹을 유지 합니다.

## 변수

### -Access
네트워크 트래픽의 허용 또는 거부 여부를 지정 합니다.
이 매개 변수에 허용 되는 값은 허용 및 거부입니다.

```yaml
Type: String
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

### -설명
네트워크 보안 규칙 구성에 대 한 설명을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
대상 주소 접두사를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 클래스 없는 도메인간 라우팅 (CIDR) 주소
- 대상 IP 주소 범위
- 모든 IP 주소와 일치 하는 와일드 카드 문자 (*)

VirtualNetwork, AzureLoadBalancer, 인터넷 등의 태그를 사용할 수 있습니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
규칙의 대상으로 설정 된 응용 프로그램 보안 그룹 ' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
규칙의 대상으로 설정 된 응용 프로그램 보안 그룹 ' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
대상 포트 또는 범위를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 정수
- 0에서 65535 사이의 정수 범위
- 모든 포트에 일치 하는 와일드 카드 문자 (*)

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 방향
들어오는 트래픽이나 보내는 트래픽에 대해 규칙이 평가 되는지 여부를 지정 합니다.
이 매개 변수에 허용 되는 값은 인바운드와 아웃 바운드입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
네트워크 보안 규칙 구성의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
**Networksecuritygroup** 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 개체에 네트워크 보안 규칙 구성을 추가 합니다.

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -우선 순위
규칙 구성의 우선 순위를 지정 합니다.
이 매개 변수에 허용 되는 값은 100에서 4096 사이의 정수입니다.

우선 순위 번호는 컬렉션의 각 규칙에 대해 고유 해야 합니다.
우선 순위 번호가 낮을수록 규칙의 우선 순위가 높습니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로토콜
규칙 구성이 적용 되는 네트워크 프로토콜을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- Net.tcp
- Udp
- 와일드 카드 문자 (*)와 일치 하는 항목

```yaml
Type: String
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
원본 주소 접두사를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- CIDR
- 원본 IP 범위
- 모든 IP 주소와 일치 하는 와일드 카드 문자 (*)입니다.

VirtualNetwork, AzureLoadBalancer 및 Internet 등의 태그를 사용할 수도 있습니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
규칙의 원본으로 설정 된 응용 프로그램 보안 그룹 ' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
규칙의 원본으로 설정 된 응용 프로그램 보안 그룹 ' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
원본 포트 또는 범위를 지정 합니다.
이 값은 정수 (0에서 65535 사이의 범위 또는 원본 포트와 일치 하는 와일드 카드 문자 (*))로 표현 됩니다.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSNetworkSecurityGroup
' NetworkSecurityGroup ' 매개 변수는 파이프라인에서 ' PSNetworkSecurityGroup ' 유형의 값을 허용 합니다.

## 출력

### Microsoft. 네트워크 모델. PSNetworkSecurityGroup

## 상속자

## 관련 링크

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[새로운 AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[제거-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


