---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 3ccce01d969f6d6601d4db7383aab505923a7063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985777"
---
# New-AzFirewallNetworkRuleCollection

## SYNOPSIS
Azure 방화벽 네트워크 규칙 컬렉션을 만듭니다.

## 구문

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzFirewallNetworkRuleCollection** cmdlet은 방화벽 네트워크 규칙 컬렉션을 만듭니다.

## 예제

### 예제 1: 두 규칙이 있는 네트워크 컬렉션 만들기
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

이 예제에서는 두 규칙 중 하나에 일치하는 모든 트래픽을 허용하는 컬렉션을 만듭니다.
첫 번째 규칙은 모든 UDP 트래픽에 대한 규칙입니다.
두 번째 규칙은 10.0.0.0.0에서 60.1.5.0:4040까지의 TCP 트래픽에 대한 규칙입니다.
우선 순위가 높은 다른 네트워크 규칙 컬렉션(더 작은 수)이 있는 경우, $rule 1 또는 $rule 2에서 식별된 트래픽과 일치하는 경우 우선 순위가 높은 규칙 컬렉션의 작업이 대신 적용됩니다. 

### 예제 2: 규칙 컬렉션에 규칙 추가
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

이 예제에서는 하나의 규칙으로 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체의 AddRule 메서드를 사용하여 규칙 컬렉션에 두 번째 규칙을 추가합니다. 주어진 규칙 컬렉션의 각 규칙 이름에는 고유한 이름이 있어야 합니다.

### 예제 3: 규칙 컬렉션에서 규칙 사용
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

이 예제에서는 하나의 규칙이 있는 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 GetRuleByName 메서드를 호출하여 이름으로 규칙을 얻습니다. GetRuleByName 메서드의 규칙 이름은 대소문자에 대해 알 수 없습니다.

### 예제 4: 규칙 컬렉션에서 규칙 제거
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

이 예제에서는 두 규칙이 있는 새 네트워크 규칙 컬렉션을 만든 다음 규칙 컬렉션 개체에서 RemoveRuleByName 메서드를 호출하여 규칙 컬렉션에서 첫 번째 규칙을 제거합니다. RemoveRuleByName 메서드의 규칙 이름은 대소문자와 무관합니다.

## 매개 변수

### -ActionType
이 규칙의 트래픽 일치 조건에 대해 수행될 작업을 지정합니다. 수락된 작업은 "허용" 또는 "거부"입니다.

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
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
이 네트워크 규칙 컬렉션의 이름을 지정합니다. 이름은 모든 네트워크 규칙 컬렉션에서 고유해야 합니다.

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

### -Priority
이 규칙 컬렉션의 우선 순위를 지정합니다. 우선 순위는 100에서 65000 사이의 숫자입니다. 숫자가 작을수록 우선 순위가 높습니다.

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

### -Rule
이 컬렉션에서 그룹화할 규칙 목록을 지정합니다.

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
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection

## 참고 사항

## 관련 링크

[New-AzFirewallNetworkRule](./New-AzFirewallNetworkRule.md)

[New-AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)
