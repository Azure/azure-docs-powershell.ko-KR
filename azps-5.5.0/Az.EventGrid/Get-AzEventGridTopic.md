---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194428"
---
# Get-AzEventGridTopic

## SYNOPSIS
Event Grid 항목의 세부 정보를 얻거나 현재 Azure 구독의 모든 Event Grid 토픽 목록을 얻습니다.

## 구문

### ResourceGroupNameParameterSet(기본값)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Get-AzEventGridTopic cmdlet은 지정된 Event Grid 토픽의 세부 정보 또는 현재 Azure 구독의 모든 Event Grid 토픽 목록을 얻습니다.
토픽 이름이 제공된 경우 단일 Event Grid 토픽의 세부 정보가 반환됩니다.
토픽 이름이 제공되지 않은 경우 토픽 목록이 반환됩니다. 이 목록에 반환되는 요소 수는 Top 매개 변수에 의해 제어됩니다. 상위 값이 지정되지 않은 경우 또는 $null 목록에 모든 토픽 항목이 포함되어 있습니다. 그렇지 않으면 맨 위가 목록에 반환될 최대 요소 수를 나타냅니다.
더 많은 토픽을 계속 사용할 수 있는 경우 다음 호출에서 NextLink의 값을 사용하여 항목의 다음 페이지를 얻습니다.
마지막으로 ODataQuery 매개 변수는 검색 결과에 대한 필터링을 수행하는 데 사용됩니다. 필터링 쿼리는 Name 속성만 사용하는 OData 구문을 따르게 됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

리소스 그룹 \` \` \` MyResourceGroupName의 Event Grid 항목 Topic1에 대한 세부 정보를 \` 얻습니다.

### 예제 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

리소스 그룹 \` \` \` MyResourceGroupName의 Event Grid 항목 Topic1에 대한 세부 정보를 \` 얻습니다.

### 예제 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

리소스 그룹 \` MyResourceGroupName의 모든 Event Grid 토픽을 페이지인하지 않고 \` 나열합니다.

### 예제 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

리소스 그룹 \` MyResourceGroupName의 처음 10개 Event Grid 토픽(있는 경우)을 $odataFilter \` 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 토픽의 다음 페이지를 얻기 위해 사용자는 다시 호출해야 Get-AzEventGridTopic 결과를 사용할 수 있습니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

### 예제 5
```powershell
PS C:\> Get-AzEventGridTopic
```

구독의 모든 Event Grid 토픽을 페이제이션 없이 나열합니다.

### 예제 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

구독에서 이벤트 쿼리를 충족하는 처음 10개 Event Grid 토픽(있는 경우)$odataFilter 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 토픽의 다음 페이지를 얻기 위해 사용자는 다시 호출해야 Get-AzEventGridTopic 결과를 사용할 수 있습니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -Name
EventGrid 토픽 이름입니다.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
얻을 리소스의 다음 페이지에 대한 링크입니다. 이 값은 더 많은 리소스를 계속 Get-AzEventGrid 경우 첫 번째 Get-AzEventGrid cmdlet 호출을 통해 얻습니다.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다. 필터링은 현재 Name 속성에서만 허용됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Event Grid 토픽을 나타내는 리소스 식별자입니다.

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

### -Top
얻을 최대 리소스 수입니다. 유효한 값은 1에서 100 사이입니다. 상위 값이 지정되어 더 많은 결과를 계속 사용할 수 있는 경우 결과에 NextLink에서 검색할 다음 페이지에 대한 링크가 포함되어 있습니다. 상위 값을 지정하지 않으면 리소스의 전체 목록이 한에 반환됩니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## 출력

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## 참고 사항

## 관련 링크
