---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376804"
---
# Get-AzEventGridSubscription

## SYNOPSIS
이벤트 구독의 세부 정보를 얻거나 현재 Azure 구독의 모든 이벤트 구독 목록을 얻습니다.

## 구문

### EventSubscriptionTopicNameParameterSet(기본값)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
Get-AzEventGridSubscription cmdlet은 지정된 Event Grid 구독의 세부 정보 또는 현재 Azure 구독 또는 리소스 그룹의 모든 Event Grid 구독 목록을 얻습니다.
이벤트 구독 이름이 제공된 경우 단일 Event Grid 구독의 세부 정보가 반환됩니다.
이벤트 구독 이름이 제공되지 않은 경우 모든 이벤트 구독 목록이 반환됩니다. 이 목록에 반환되는 요소 수는 Top 매개 변수에 의해 제어됩니다. 상위 값이 지정되지 않은 경우 $null 모든 이벤트 구독 항목이 목록에 포함되어 있습니다. 그렇지 않으면 맨 위가 목록에 반환될 최대 요소 수를 나타냅니다.
더 많은 이벤트 구독을 계속 사용할 수 있는 경우 다음 호출에서 NextLink의 값을 사용하여 이벤트 구독의 다음 페이지를 얻습니다.
마지막으로 ODataQuery 매개 변수는 검색 결과에 대한 필터링을 수행하는 데 사용됩니다. 필터링 쿼리는 Name 속성만 사용하는 OData 구문을 따르게 됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

리소스 그룹 \` \` \` \` \` MyResourceGroupName에서 Topic1에 대해 만든 이벤트 구독 EventSubscription1의 세부 정보를 \` 얻습니다.

### 예제 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

웹후크 기반 이벤트 구독인 경우 전체 엔드포인트 URL을 포함하여 리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Topic1에 대해 만든 이벤트 구독 EventSubscription1의 세부 정보를 \` 얻습니다.

### 예제 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Pagination 없이 리소스 그룹 \` \` \` MyResourceGroupName에서 Topic1에 대해 만든 모든 이벤트 구독 목록을 \` 얻습니다.

### 예제 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

리소스 그룹 \` \` \` MyResourceGroupName에서 토픽 Topic1에 대해 만든 처음 10개 이벤트 구독(있는 경우)을 $odataFilter \` 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

### 예제 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

리소스 그룹 \` \` \` MyResourceGroupName에 대해 만든 이벤트 구독 EventSubscription1의 세부 정보를 \` 얻습니다.

### 예제 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

현재 선택한 Azure 구독에 대해 만든 이벤트 구독 \` EventSubscription1의 \` 세부 정보를 얻습니다.

### 예제 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Pagination 없이 리소스 그룹 \` MyResourceGroupName에서 만든 모든 전역 이벤트 구독 목록을 \` 얻습니다.

### 예제 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

리소스 그룹 \` MyResourceGroupName에서 만든 처음 5개 이벤트 구독(있는 경우)을 $odataFilter \` 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

### 예제 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

현재 선택한 Azure 구독에서 만든 모든 전역 이벤트 구독의 목록을 페이그인하지 않고 선택합니다.

### 예제 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

현재 선택한 Azure 구독에서 만든 처음 15개 전역 이벤트 구독(있는 경우)을 $odataFilter 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

### 예제 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

지정한 위치 westus2의 리소스 그룹 \` MyResourceGroupName에서 만든 모든 지역별 이벤트 구독 목록을 페이지 인하지 않고 \` \` \` 선택합니다.

### 예제 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

리소스 그룹 \` MyResourceGroupName에서 만든 처음 15개 지역 이벤트 구독(있는 경우)을 지정된 \` 위치 westus2에 나열하여 $odataFilter \` \` 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

### 예제 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

지정한 EventHub 네임스페이스에 대해 만든 모든 이벤트 구독의 목록을 페이그인(pagination) 없이 선택합니다.

### 예제 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

지정된 EventHub 네임스페이스에 대해 생성된 처음 25개 이벤트 구독(있는 경우)을 $odataFilter 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

### 예제 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

지정된 토픽 유형(EventHub 네임스페이스)에 대해 만든 모든 이벤트 구독의 목록을 페이제이션 없이 지정한 위치에 제공합니다.

### 예제 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

지정된 토픽 유형(EventHub 네임스페이스)에 대해 만든 처음 15개 이벤트 구독(있는 경우)을 지정된 $odataFilter 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

### 예제 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

특정 리소스 그룹에 대해 만든 모든 이벤트 구독 목록을 페이게이션하지 않고 선택합니다.

### 예제 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

특정 리소스 그룹에 대해 생성된 처음 100개 이벤트 구독(있는 경우)을 $odataFilter 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 이벤트 구독의 다음 페이지를 얻기 위해 사용자는 이벤트를 다시 호출하고 결과를 Get-AzEventGridSubscription 합니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

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

### -DomainInputObject
EventGrid 도메인 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainName
EventGrid 도메인 이름입니다.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
EventGrid 도메인 토픽 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
EventGrid 도메인 토픽 이름입니다.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
이벤트 구독의 이름

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
이벤트 구독 대상의 전체 엔드포인트 URL을 포함합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid 토픽 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
위치

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
얻을 리소스의 다음 페이지에 대한 링크입니다. 이 값은 더 많은 리소스를 계속 Get-AzEventGrid 수 있는 경우 첫 번째 Get-AzEventGrid cmdlet 호출을 통해 얻습니다.

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
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
이벤트 구독이 만들어진 리소스의 식별자입니다.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다. 필터링은 현재 Name 속성에서만 허용됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
EventGrid 토픽 이름입니다.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType 이름

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
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

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## 출력

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## 참고 사항

## 관련 링크
