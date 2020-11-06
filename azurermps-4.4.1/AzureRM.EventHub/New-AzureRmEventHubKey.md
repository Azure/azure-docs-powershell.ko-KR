---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537243"
---
# New-AzureRmEventHubKey

## SYNOPSIS
지정 된 이벤트 허브 권한 부여 규칙에 대 한 새 기본 또는 보조 키를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### NamespaceAuthorizationRuleSet (기본값)
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### EventhubAuthorizationRuleSet
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## 설명은
New-AzureRmEventHubKey cmdlet은 지정 된 이벤트 허브 권한 부여 규칙에 대 한 기본 또는 보조 SAS 키를 다시 생성 합니다.

## 예제의

### 예제 1.1
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

권한 부여 규칙 MyAuthRuleName에 대 한 기본 키를 다시 생성 \` \` 합니다.

### 예제 1.2
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

권한 부여 규칙 MyAuthRuleName에 대 한 기본 키를 다시 생성 \` \` 합니다.

### 예제 2.1
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### 예제 2.2
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

권한 부여 규칙 MyAuthRuleName에 대 한 보조 키를 다시 생성 \` \` 합니다.

## 변수

### -RegenerateKey
다시 생성 하는 키: \` PrimaryKey \` 또는 \` secondarykey \` 입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

