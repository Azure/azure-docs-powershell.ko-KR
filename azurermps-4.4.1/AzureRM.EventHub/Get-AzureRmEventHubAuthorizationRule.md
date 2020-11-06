---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537268"
---
# Get-AzureRmEventHubAuthorizationRule

## SYNOPSIS
권한 부여 규칙의 세부 정보를 가져오거나 권한 부여 규칙 목록을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### NamespaceAuthorizationRuleSet (기본값)
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### EventhubAuthorizationRuleSet
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## 설명은
Get-AzureRmEventHubAuthorizationRule cmdlet은 권한 부여 규칙의 세부 정보나 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙의 목록을 가져옵니다.
권한 부여 규칙의 이름을 제공 하는 경우 해당 단일 인증 규칙의 세부 정보가 반환 됩니다.
권한 부여 규칙의 이름을 제공 하지 않으면 지정 된 이벤트 허브에 대 한 모든 권한 부여 규칙 목록이 반환 됩니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

\` \` \` \` 네임 스페이스 MyNamespaceName로 범위가 지정 된 이벤트 허브 MyEventHubName에서 \` 권한 부여 규칙 MyAuthRuleName를 가져옵니다 \` .

### 예제 2
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

\` \` MyNamespaceName 네임 스페이스의 범위를 지정 하는 이벤트 허브 MyEventHubName의 모든 권한 부여 규칙 목록을 가져옵니다 \` \` .

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

### -Eventhub
Eventhub 이름.

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

### -이름
AuthorizationRule 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
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

## 입력

### System. 문자열

## 출력

### System.webserver. List ' 1 [[Microsoft Azure.]. a n [[0.0.1.0]. SharedAccessAuthorizationRuleAttributes, Microsoft Azure. 명령. EventHub, Version =, Culture = 중립, PublicKeyToken = null]]

## 상속자

## 관련 링크

