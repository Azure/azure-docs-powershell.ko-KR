---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 66e32c19001586972cb408e61397545fb1c25d44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696498"
---
# Get-AzEventHubAuthorizationRule

## SYNOPSIS
권한 부여 규칙의 세부 정보를 가져오거나 권한 부여 규칙 목록을 가져옵니다.

## 구문과

### NamespaceAuthorizationRuleSet (기본값)
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

## 설명은
Get-AzEventHubAuthorizationRule cmdlet은 권한 부여 규칙의 세부 정보나 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙의 목록을 가져옵니다.
권한 부여 규칙의 이름을 제공 하는 경우 해당 단일 인증 규칙의 세부 정보가 반환 됩니다.
권한 부여 규칙의 이름을 제공 하지 않으면 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙 목록이 반환 됩니다.
(재해 복구) 별칭 이름이 제공 되 면 별칭에 대 한 네임 스페이스의 권한 부여 규칙에 대 한 세부 정보가 반환 됩니다.

## 예제의

### 예제 1.0-네임 스페이스에 대 한 AuthorizationRule
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

\` \` 네임 스페이스 MyNamespaceName에서 MyAuthRuleName 권한 부여 규칙을 가져옵니다 \` \` .

### 예제 1.1-네임 스페이스에 대 한 AuthorizationRules
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

네임 스페이스 MyNamespaceName의 모든 권한 부여 규칙 목록을 가져옵니다 \` \` .

### 예제 2.0-EventHub에 대 한 AuthorizationRule
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

\` \` \` \` 네임 스페이스 MyNamespaceName로 범위가 지정 된 이벤트 허브 MyEventHubName에서 \` 권한 부여 규칙 MyAuthRuleName를 가져옵니다 \` .

### 예제 2.1-EventHub에 대 한 AuthorizationRules
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

\` \` MyNamespaceName 네임 스페이스의 범위를 지정 하는 이벤트 허브 MyEventHubName의 목록 인증 규칙을 가져옵니다 \` \` .

### 예제 3.0-별칭에 대 한 AuthorizationRule (GeoRecovery 구성)
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

\` \` 네임 스페이스 MyNamespaceName에서 MyAuthRuleName 권한 부여 규칙을 가져옵니다 \` \` .

### 예제 3.1-별칭에 대 한 AuthorizationRules (GeoRecovery 구성)
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

\` \` 네임 스페이스 MyNamespaceName의 모든 권한 부여 규칙 MyAuthRuleName 목록을 가져옵니다 \` \` .

## 변수

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

### -이름
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

### -Namespace
네임 스페이스 이름

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. ' EventHub. ' PSSharedAccessAuthorizationRuleAttributes

## 상속자

## 관련 링크
