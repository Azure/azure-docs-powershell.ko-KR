---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 842b48e1645bb141650c2a53dc86bbb5e79acb80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969200"
---
# Get-AzEventHubAuthorizationRule

## SYNOPSIS
권한 부여 규칙의 세부 정보를 얻거나 권한 부여 규칙 목록을 얻습니다.

## 구문

### NamespaceAuthorizationRuleSet(기본값)
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventhubAuthorizationRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasAuthoRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Get-AzEventHubAuthorizationRule cmdlet은 권한 부여 규칙의 세부 정보 또는 지정된 Event Hub에 대한 모든 권한 부여 규칙 목록을 얻습니다.
권한 부여 규칙의 이름이 제공된 경우 해당 단일 권한 부여 규칙의 세부 정보가 반환됩니다.
권한 부여 규칙의 이름이 제공되지 않으면 지정된 Event Hub에 대한 모든 권한 부여 규칙 목록이 반환됩니다.
(재해 복구) 별칭 이름이 제공된 경우 구성된 별칭에 대한 네임스페이스의 권한 부여 규칙에 대한 세부 정보가 반환됩니다.

## 예제

### 예제 1: 네임스페이스에 대한 AuthorizationRule
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

네임스페이스 \` \` \` MyNamespaceName에서 MyAuthRuleName 권한 부여 규칙을 \` 얻습니다.

### 예제 2: 네임스페이스에 대한 AuthorizationRules
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

\`네임스페이스 MyNamespaceName의 모든 권한 부여 규칙 목록을 \` 얻습니다.

### 예제 3: EventHub용 AuthorizationRule
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

네임스페이스 MyNamespaceName의 범위가 지정되는 Event \` \` Hub \` MyEventHubName에서 \` \` MyAuthRuleName \` 권한 부여 규칙을 얻습니다.

### 예제 4: EventHub용 AuthorizationRules
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

네임스페이스 \` \` \` MyNamespaceName의 범위가 지정되는 Event Hub MyEventHubName에서 목록 권한 부여 규칙을 \` 얻습니다.

### 예제 5: 별칭에 대한 AuthorizationRule(GeoRecovery 구성)
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

네임스페이스 \` \` \` MyNamespaceName에서 MyAuthRuleName 권한 부여 규칙을 \` 얻습니다.

### 예제 6: 별칭에 대한 AuthorizationRules(GeoRecovery 구성)
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

네임스페이스 \` \` \` MyNamespaceName에서 MyAuthRuleName의 모든 권한 부여 규칙 목록을 을 \` 니다.

## 매개 변수

### -AliasName
별칭 이름

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Eventhub
Eventhub 이름

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
AuthorizationRule 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -네임스페이스
네임스페이스 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes

## 참고 사항

## 관련 링크
