---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711574"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## SYNOPSIS
Eventubs 네임 스페이스 권한 부여 규칙의 세부 정보를 가져오거나 권한 부여 규칙의 목록을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## 설명은
Get-AzureRmEventHubNamespaceAuthorizationRule cmdlet은 지정 된 이벤트 허브 네임 스페이스 권한 부여 규칙 또는 네임 스페이스 권한 부여 규칙 목록에 대 한 세부 정보를 가져옵니다.
권한 부여 규칙 이름을 제공 하는 경우 단일 인증 규칙의 세부 정보가 반환 됩니다.
권한 부여 규칙 이름을 제공 하지 않으면 네임 스페이스의 모든 권한 부여 규칙 목록이 반환 됩니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 이벤트 허브 네임 스페이스 MyNamespaceName에 있는 \` 권한 부여 규칙 MyAuthRuleName를 반환 합니다 \` .

### 예제 2
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 이벤트 허브 네임 스페이스 MyNamespaceName에서 \` 기본 권한 부여 규칙 RootManageSharedAccessKey를 반환 합니다 \` .

### 예제 3
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

\` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 이벤트 허브 네임 스페이스 MyNamespaceName의 모든 권한 부여 규칙을 반환 합니다 \` \` .

## 변수

### -AuthorizationRuleName
이벤트 허브 네임 스페이스 권한 부여 규칙 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
이벤트 허브 네임 스페이스 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

## 입력

### System. 문자열

## 출력

### System.webserver. List ' 1 [[Microsoft Azure.]. a n [[0.0.1.0]. SharedAccessAuthorizationRuleAttributes, Microsoft Azure. 명령. EventHub, Version =, Culture = 중립, PublicKeyToken = null]]

## 상속자

## 관련 링크

