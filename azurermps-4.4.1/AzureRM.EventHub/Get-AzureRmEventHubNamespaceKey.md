---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537252"
---
# Get-AzureRmEventHubNamespaceKey

## SYNOPSIS
지정 된 이벤트 허브 네임 스페이스 권한 부여 규칙의 권한 부여 규칙에 대 한 기본, 보조 connectionstrings 및 키의 세부 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## 설명은
Get-AzureRmEventHubNamespaceKey cmdlet은 지정 된 이벤트 허브 네임 스페이스에서 지정한 권한 부여 규칙의 기본 및 보조 connectionstrings 및 키 세부 정보를 반환 합니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

\` \` \` \` 리소스 그룹 MyResourceGroupName의 이벤트 허브 네임 스페이스 MyNamespaceName에서 권한 \` 부여 규칙 MyAuthRuleName에 대 한 기본, 보조 connectionstrings 및 키의 세부 정보를 가져옵니다 \` .

## 변수

### -AuthorizationRuleName
이벤트 허브 네임 스페이스에 대 한 권한 부여 규칙의 이름입니다.

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

## 입력

### System. 문자열

## 출력

### ListKeysAttributes (.).

## 상속자

## 관련 링크

