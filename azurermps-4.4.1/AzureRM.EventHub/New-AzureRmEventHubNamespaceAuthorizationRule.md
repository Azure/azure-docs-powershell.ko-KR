---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: dc384ca6056ef13d5517241d550bacddf2e7d0d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537244"
---
# New-AzureRmEventHubNamespaceAuthorizationRule

## SYNOPSIS
지정 된 네임 스페이스에 대 한 새 권한 부여 규칙을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String> [-Rights] <String[]> [-WhatIf] [-Confirm]
```

## 설명은
New-AzureRmEventHubNamespaceAuthorizationRule cmdlet은 지정 된 이벤트 허브 네임 스페이스에 대 한 새 권한 부여 규칙을 만듭니다.

## 예제의

### 예제 1
```
PS C:\> New-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

\` \` \` \` 리소스 그룹 MyResourceGroupName에서 이벤트 허브 네임 스페이스 MyNamespaceName에 대 한 수신 대기 및 보내기 권한을 사용 하 여 \` MyAuthRuleName \` 권한 부여 규칙을 만듭니다.

## 변수

### -AuthorizationRuleName
권한 부여 규칙 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -권한
권한 (예: @ ("수신", "보내기", "관리")

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

## 입력

### System. 문자열

## 출력

### Microsoft. *. a. a.

## 상속자

## 관련 링크

