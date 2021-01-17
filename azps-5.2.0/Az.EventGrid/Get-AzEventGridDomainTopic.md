---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346773"
---
# Get-AzEventGridDomainTopic

## SYNOPSIS
Event Grid 도메인 토픽의 세부 정보를 얻거나 현재 Azure 구독의 특정 Event Grid 도메인 아래에 있는 모든 Event Grid 도메인 토픽 목록을 얻습니다.

## 구문

### DomainTopicNameParameterSet(기본값)
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdDomainTopicParameterSet
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Get-AzEventGridDomainTopic cmdlet은 지정된 Event Grid 도메인 토픽의 세부 정보 또는 현재 Azure 구독의 특정 도메인에 있는 모든 Event Grid 도메인 토픽 목록을 얻습니다.
도메인 토픽 이름이 제공된 경우 단일 Event Grid 도메인 토픽의 세부 정보가 반환됩니다.
도메인 토픽 이름이 제공되지 않으면 지정된 도메인 이름의 도메인 토픽 목록이 반환됩니다. 이 목록에 반환되는 요소 수는 Top 매개 변수에 의해 제어됩니다. 상위 값이 지정되지 않은 경우 $null 모든 도메인 토픽 항목이 목록에 포함되어 있습니다. 그렇지 않으면 맨 위가 목록에 반환될 최대 요소 수를 나타냅니다.
더 많은 도메인 토픽을 계속 사용할 수 있는 경우 다음 호출에서 NextLink의 값을 사용하여 도메인 토픽의 다음 페이지를 얻습니다.
마지막으로 ODataQuery 매개 변수는 검색 결과에 대한 필터링을 수행하는 데 사용됩니다. 필터링 쿼리는 Name 속성만 사용하는 OData 구문을 따르게 됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.

## 예제

### 예제 1

리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Event Grid 도메인 Domain1에서 Event Grid 도메인 토픽 DomainTopic1의 세부 정보를 \` 얻습니다.

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### 예제 2

ResourceId 옵션을 사용하여 리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Event Grid 도메인 Domain1에서 Event Grid 도메인 토픽 DomainTopic1의 \` 세부 정보를 얻습니다.

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### 예제 3

Event Grid 도메인 도메인 1 아래에 있는 모든 Event Grid 도메인 토픽을 나열합니다( 단번에 모든 결과가 반환되는 경우) \` \` \` MyResourceGroupName 리소스 그룹에서 MyResourceGroupName을 \` 나열합니다.

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### 예제 4

ResourceId 옵션을 사용하여 Event Grid 도메인 도메인 1에 있는 모든 Event Grid 도메인 토픽을 \` \` 나열합니다. \` \`

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### 예제 5

리소스 그룹 \` \` \` MyResourceGroupName의 domain Domain1 아래에 한 $odataFilter 쿼리 10개 도메인 토픽을 충족하는 Event Grid 도메인 토픽(있는 경우)을 \` 나열합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null. 도메인 토픽의 다음 페이지를 얻기 위해 사용자는 다시 호출하여 결과를 Get-AzEventGridDomainTopic 합니다. 이전 호출에서 얻은 NextLink입니다. 호출자는 결과 시 중지해야 합니다. NextLink가 $null.

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -DomainName
EventGrid 도메인 이름입니다.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
EventGrid 도메인 토픽 이름입니다.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

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
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Event Grid 도메인 또는 Grid 도메인 토픽을 나타내는 리소스 식별자입니다.

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
목록 결과를 필터링하는 데 사용되는 OData 쿼리입니다. 필터링은 현재 Name 속성에서만 허용됩니다. 지원되는 작업에는 CONTAINS, eq(같음), ne(같지 않은 경우), AND, OR 및 NOT이 포함됩니다.

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
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

### System.Int32

## 출력

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance

## 참고 사항

## 관련 링크
