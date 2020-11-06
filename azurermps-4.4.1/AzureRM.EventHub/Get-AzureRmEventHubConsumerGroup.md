---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537260"
---
# Get-AzureRmEventHubConsumerGroup

## SYNOPSIS
지정 된 이벤트 허브 소비자 그룹의 세부 정보를 가져오거나 이벤트 허브의 소비자 그룹 목록을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## 설명은
Get-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브 소비자 그룹 또는 지정 된 이벤트 허브의 소비자 그룹 목록에 대 한 세부 정보를 가져옵니다.
소비자 그룹의 이름을 제공 하는 경우 단일 소비자 그룹 세부 정보에 대 한 세부 정보가 반환 됩니다.
소비자 그룹의 이름을 제공 하지 않으면 지정 된 이벤트 허브의 소비자 그룹 목록이 반환 됩니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

\` \` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName에서 \` 소비자 그룹 MyConsumerGroupName를 가져옵니다.

### 예제 2
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName의 소비자 그룹 목록을 가져옵니다 \` .

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

### -EventHub
EventHub 이름.

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
ConsumerGroup 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

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

### System.webserver. List ' 1 [[Microsoft ConsumerGroupAttributes, Microsoft Azure. 0.0.1.0, Version =, Culture = 중립, PublicKeyToken = null]])

## 상속자

## 관련 링크

