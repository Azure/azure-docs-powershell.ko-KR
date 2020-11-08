---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 16643ba0060f4f242f8c36ff16737a03aec7507b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043264"
---
# New-AzFirewallNetworkRuleCollection

## SYNOPSIS
네트워크 규칙의 Azure 방화벽 네트워크 컬렉션을 만듭니다.

## 구문과

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzFirewallNetworkRuleCollection** Cmdlet은 방화벽 네트워크 규칙의 컬렉션을 만듭니다.

## 예제의

### 1: 두 가지 규칙을 사용 하 여 네트워크 컬렉션 만들기
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

이 예제에서는 두 규칙 중 하 나와 일치 하는 모든 트래픽을 허용 하는 컬렉션을 만듭니다.
첫 번째 규칙은 모든 UDP 트래픽에 대 한 것입니다.
두 번째 규칙은 10.0.0.0에서 60.1.5.0:4040 TCP 트래픽에 대 한 것입니다.
$Rule 1 또는 $rule 2에서 식별 된 트래픽에만 일치 하는 더 높은 우선 순위의 네트워크 규칙 컬렉션이 있는 경우에는 우선 순위가 높은 규칙 모음의 작업이 대신 적용 됩니다. 

### 2: 규칙 컬렉션에 규칙 추가
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

이 예제에서는 규칙 하나가 포함 된 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에 메서드 AddRule을 사용 하 여 규칙 컬렉션에 두 번째 규칙을 추가 합니다. 지정 된 규칙 컬렉션의 각 규칙 이름은 고유한 이름을 가져야 하 고 대/소문자를 구분 하지 않습니다.

### 3: 규칙 컬렉션에서 규칙 가져오기
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

이 예제에서는 규칙 하나가 포함 된 새 네트워크 규칙 컬렉션을 만든 다음, 규칙 컬렉션 개체의 GetRuleByName 메서드를 호출 하 여 이름을 기준으로 규칙을 가져옵니다. 메서드 GetRuleByName의 규칙 이름은 대/소문자를 구분 하지 않습니다.

### 4: 규칙 컬렉션에서 규칙 제거
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

이 예제에서는 두 개의 규칙이 있는 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체의 메서드 RemoveRuleByName를 호출 하 여 규칙 컬렉션에서 첫 번째 규칙을 제거 합니다. 메서드 RemoveRuleByName의 규칙 이름은 대/소문자를 구분 하지 않습니다.

## 변수

### -ActionType
이 규칙의 트래픽 일치 조건에 대해 수행할 작업을 지정 합니다. 허용 되는 작업은 "허용" 또는 "거부"입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
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

### -이름
이 네트워크 규칙 컬렉션의 이름을 지정 합니다. 이름은 모든 네트워크 규칙 모음에서 고유 해야 합니다.

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

### -우선 순위
이 규칙 컬렉션의 우선 순위를 지정 합니다. Priority는 100과 65000 사이의 숫자입니다. 숫자가 작을수록 우선 순위가 높습니다.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -규칙
이 컬렉션 아래에서 그룹화 할 규칙 목록을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### PSAzureFirewallNetworkRuleCollection에 대 한.

## 상속자

## 관련 링크

[새로운 AzFirewallNetworkRule](./New-AzFirewallNetworkRule.md)

[새로운 AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)
