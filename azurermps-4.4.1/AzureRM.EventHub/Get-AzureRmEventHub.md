---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537272"
---
# Get-AzureRmEventHub

## SYNOPSIS
단일 이벤트 허브의 세부 정보를 가져오거나 이벤트 허브 목록을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## 설명은
Get-AzureRmEventHub cmdlet은 이벤트 허브의 세부 정보 또는 현재 네임 스페이스에 있는 모든 이벤트 허브의 목록 중 하나를 반환 합니다.
이벤트 허브 이름을 제공 하는 경우 단일 이벤트 허브에 대 한 세부 정보가 반환 됩니다.
이벤트 허브 이름을 제공 하지 않으면 지정 된 네임 스페이스에 있는 모든 이벤트 허브 목록이 반환 됩니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

이벤트 허브 MyEventHubName의 세부 정보를 반환 합니다 \` \` .

### 예제 2
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

네임 스페이스 MyNamespaceName의 이벤트 허브 목록을 반환 \` \` 합니다.

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

### -이름
EventHub 이름.

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

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
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## 입력

### System. 문자열

## 출력

### System.webserver. List ' 1 [[Microsoft EventHubAttributes, Microsoft Azure. 0.0.1.0, Version =, Culture = 중립, PublicKeyToken = null]])

## 상속자

## 관련 링크

