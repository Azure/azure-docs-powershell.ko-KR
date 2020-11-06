---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: ed2855571ccd3ce10a8a41fd72f5e14fde7bba16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537295"
---
# New-AzureRmEventGridSubscription

## SYNOPSIS
항목, Azure 리소스, Azure 구독 또는 리소스 그룹에 대 한 새 Azure 이벤트 그리드 이벤트 구독을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ResourceGroupNameParameterSet (기본값)
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EventSubscriptionInputObjectSet
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CustomTopicEventSubscriptionParameterSet
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Azure 이벤트 그리드 항목, 지원 되는 Azure 리소스, Azure 구독 또는 리소스 그룹에 대 한 새 이벤트 구독을 만듭니다.
현재 선택 된 Azure 구독에 대 한 이벤트 구독을 만들려면 이벤트 구독 이름과 대상 끝점을 지정 합니다.
리소스 그룹에 대 한 이벤트 구독을 만들려면 이벤트 구독 이름과 대상 끝점 외에도 리소스 그룹 이름을 지정 합니다.
Azure 이벤트 그리드 항목에 대 한 이벤트 구독을 만들려면 항목 이름도 함께 지정 합니다.
지원 되는 Azure 리소스에 대 한 이벤트 구독을 만들려면 리소스의 전체 리소스 ID를 지정 합니다. 지원 되는 형식 목록을 보려면 Get-AzureRmEventGridTopicType cmdlet을 실행 합니다.

## 예제의

### 예제 1
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

\` \` \` \` \` \` Webhook 대상 끝점을 사용 하 여 리소스 그룹 MyResourceGroupName에서 Azure 이벤트 그리드 항목 Topic1에 EventSubscription1 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 . 이 이벤트 구독은 기본 필터를 사용 합니다.

### 예제 2
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

\` \` \` \` Webhook 대상 끝점을 사용 하 여 리소스 그룹 MyResourceGroupName EventSubscription1 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 . 이 이벤트 구독은 기본 필터를 사용 합니다.

### 예제 3
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

\` \` Webhook 대상 끝점을 사용 하 여 현재 선택 된 Azure 구독에 EventSubscription1 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 . 이 이벤트 구독은 기본 필터를 사용 합니다.

### 예제 4
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

\` \` Webhook 대상 끝점을 사용 하 여 현재 선택 된 Azure 구독에 EventSubscription1 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 . 이 이벤트 구독은 이벤트 유형 및 주체의 추가 필터를 지정 하 고 해당 필터와 일치 하는 이벤트만 대상 끝점에 전달 됩니다.

### 예제 5
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

\` \` 지정 된 이벤트 허브가 있는 현재 선택한 Azure 구독에 대 한 EventSubscription1 이벤트의 대상으로 새 이벤트 구독을 만듭니다. 이 이벤트 구독은 기본 필터를 사용 합니다.

### 예제 6
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

\` \` 지정 된 webhhok 대상 끝점을 사용 하 여 EventHub 네임 스페이스에 대 한 새 이벤트 구독을 만듭니다 https://requestb.in/19qlscd1 . 이 이벤트 구독은 기본 필터를 사용 합니다.

## 변수

### -끝점
이벤트 구독 대상 끝점입니다.
이것은 webhook URL 또는 EventHub의 Azure resource ID 일 수 있습니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndpointType
끝점 유형입니다.
이는 webhook 또는 eventhub 일 수 있습니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
이벤트 구독의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludedEventType
포함할 이벤트 유형 목록을 지정 하는 필터입니다. 지정 하지 않으면 모든 이벤트 형식이 포함 됩니다.

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
EventGrid 주제 개체

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -레이블
이벤트 구독에 대 한 레이블

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
주제의 리소스 그룹입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
이벤트 구독을 만들어야 하는 리소스의 식별자입니다.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubjectBeginsWith
지정 된 제목 접두사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.
지정 하지 않으면 모든 제목 접두사가 있는 이벤트가 포함 됩니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이란 Casesensitive
주제 필드가 대/소문자를 구분 하 여 비교 하도록 지정 하는 필터입니다.
지정 하지 않으면 제목은 대/소문자를 구분 하지 않고 비교 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -# Endswith
지정 된 주체 접미사와 일치 하는 이벤트만 포함 되도록 지정 하는 필터입니다.
지정 하지 않으면 모든 주체 접미사가 있는 이벤트가 포함 됩니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
이벤트 구독을 만들어야 하는 주제의 이름입니다.

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열
Microsoft. c c. c c. c c. c c. c c.

## 출력

### Microsoft. PSEventSubscription 표.

## 상속자

## 관련 링크

