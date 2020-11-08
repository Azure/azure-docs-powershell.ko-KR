---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216736"
---
# Set-AzNetworkSecurityRuleConfig

## SYNOPSIS
네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 업데이트 합니다.

## 구문과

### SetByResource (기본값)
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

## 설명은
**Set-AzNetworkSecurityRuleConfig** cmdlet은 네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 업데이트 합니다.

## 예제의

### 예제 1: 네트워크 보안 규칙에서 access 구성 변경
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

첫 번째 명령은 NSG-프런트 엔드 라는 네트워크 보안 그룹을 가져온 다음 변수 $nsg에 저장 합니다.
두 번째 명령은 파이프라인 연산자를 사용 하 여 $nsg의 보안 그룹을 Get-AzNetworkSecurityRuleConfig에 전달 하 고,이는 rdp-rule 라는 보안 규칙 구성을 가져옵니다.
세 번째 명령은 rdp 규칙의 액세스 구성을 Deny로 변경 합니다.

### 예제 2

네트워크 보안 그룹에 대 한 네트워크 보안 규칙 구성을 업데이트 합니다. 생성

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## 변수

### -Access
네트워크 트래픽의 허용 또는 거부 여부를 지정 합니다. 이 매개 변수에 허용 되는 값은 허용 및 거부입니다.

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

### -설명
규칙 구성에 대 한 설명을 지정 합니다.
최대 크기는 140 자입니다.

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
대상 주소 접두사를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 클래스 없는 도메인간 라우팅 (CIDR) 주소 
- 대상 IP 주소 범위 
- 모든 IP 주소와 일치 하는 와일드 카드 문자 (*) VirtualNetwork, AzureLoadBalancer, Internet 등의 태그를 사용할 수 있습니다.

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
규칙의 대상으로 설정 된 응용 프로그램 보안 그룹 ' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.

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
규칙의 대상으로 설정 된 응용 프로그램 보안 그룹 ' DestinationAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.

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
대상 포트 또는 범위를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 정수 
- 0에서 65535 사이의 정수 범위
- 모든 포트에 일치 하는 와일드 카드 문자 (*)

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

### 방향
들어오는 트래픽 또는 나가는 트래픽에 대해 규칙이 평가 되는지 여부를 지정 합니다.
이 매개 변수에 허용 되는 값은 인바운드와 아웃 바운드입니다.

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

### -이름
이 cmdlet이 설정 하는 네트워크 보안 규칙 구성의 이름을 지정 합니다.

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
설정할 네트워크 보안 규칙 구성을 포함 하는 **Networksecuritygroup** 개체를 지정 합니다.

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

### -우선 순위
규칙 구성의 우선 순위를 지정 합니다.
이 매개 변수에 허용 되는 값은 100에서 4096 사이의 정수입니다.
우선 순위 번호는 컬렉션의 각 규칙에 대해 고유 해야 합니다.
우선 순위 번호가 낮을수록 규칙의 우선 순위가 높습니다.

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

### -프로토콜
규칙 구성이 적용 되는 네트워크 프로토콜을 지정 합니다.
이 매개 변수에 허용 되는 값은:--Tcp
- Udp
- 둘 다 일치 하는 와일드 카드 문자 (*)

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
원본 주소 접두사를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- CIDR
- 원본 IP 범위
- 모든 IP 주소와 일치 하는 와일드 카드 문자 (*) VirtualNetwork, AzureLoadBalancer, Internet 등의 태그도 사용할 수도 있습니다.

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
규칙의 원본으로 설정 된 응용 프로그램 보안 그룹 ' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.

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
규칙의 원본으로 설정 된 응용 프로그램 보안 그룹 ' SourceAddressPrefix ' 매개 변수와 함께 사용할 수 없습니다.

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
원본 포트 또는 범위를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 정수
- 0에서 65535 사이의 정수 범위
- 모든 포트에 일치 하는 와일드 카드 문자 (*)

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. 네트워크 모델. PSNetworkSecurityGroup

## 출력

### Microsoft. 네트워크 모델. PSNetworkSecurityGroup

## 상속자

## 관련 링크

[추가-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[새로운 AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[제거-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


