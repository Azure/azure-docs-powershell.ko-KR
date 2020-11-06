---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537235"
---
# Remove-AzureRmEventHubAuthorizationRule

## SYNOPSIS
지정 된 이벤트 허브 권한 부여 규칙을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### NamespaceAuthorizationRuleSet (기본값)
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### EventhubAuthorizationRuleSet
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## 설명은
Remove-AzureRmEventHubAuthorizationRule cmdlet은 지정 된 이벤트 허브에서 지정한 권한 부여 규칙을 제거 하 고 삭제 합니다.

## 예제의

### 예제 1
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### 예제 2
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

\` \` 이벤트 허브 MyEventHubName에서 권한 부여 규칙 MyAuthRuleName를 제거 합니다 \` \` .

## 변수

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventHub
EventHub 이름.

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
확인 메시지를 표시 하지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
AuthorizationRule 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
네임 스페이스 이름입니다.

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
{{Fill PassThru 설명}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## 입력

### System. 문자열

## 출력

### 시스템 부울

## 상속자

## 관련 링크

