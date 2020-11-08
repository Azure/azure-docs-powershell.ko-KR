---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215475"
---
# Get-AzEventGridDomainTopic

## SYNOPSIS
이벤트 그리드 도메인 항목의 세부 정보를 가져오거나 현재 Azure 구독의 특정 이벤트 그리드 도메인 아래에 있는 모든 이벤트 그리드 도메인 항목의 목록을 가져옵니다.

## 구문과

### DomainTopicNameParameterSet (기본값)
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

## 설명은
Get-AzEventGridDomainTopic cmdlet은 지정 된 이벤트 그리드 도메인 항목에 대 한 세부 정보 또는 현재 Azure 구독에서 특정 도메인에 있는 모든 이벤트 그리드 도메인 항목의 목록 중 하나를 가져옵니다.
도메인 주제 이름을 제공 하는 경우 단일 이벤트 그리드 도메인 항목의 세부 정보가 반환 됩니다.
도메인 항목 이름이 제공 되지 않으면 지정 된 도메인 이름 아래에 있는 도메인 항목 목록이 반환 됩니다. 이 목록에 반환 되는 요소 수는 Top 매개 변수를 통해 제어 됩니다. Top 값을 지정 하지 않거나 $null 하는 경우 목록에 모든 도메인 항목 항목이 포함 됩니다. 그렇지 않으면 Top은 목록에 반환 될 최대 요소 수를 나타냅니다.
더 많은 도메인 항목을 계속 사용할 수 있는 경우 다음에 도메인 항목의 다음 페이지를 가져오기 위해 다음 호출에서 NextLink의 값을 사용 해야 합니다.
마지막으로, ODataQuery 매개 변수를 사용 하 여 검색 결과에 대 한 필터링을 수행 합니다. 필터링 쿼리는 Name 속성에만 사용 하 여 OData 구문을 따릅니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.

## 예제의

### 예제 1

\` \` \` \` 리소스 그룹 MyResourceGroupName의 이벤트 그리드 도메인 Domain1 아래 DomainTopic1 \` 이벤트 그리드 도메인 항목의 세부 정보를 가져옵니다 \` .

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

\` \` \` \` \` \` ResourceId 옵션을 사용 하 여 리소스 그룹 MyResourceGroupName의 이벤트 그리드 도메인 Domain1 아래 DomainTopic1 이벤트 그리드 도메인 항목의 세부 정보를 가져옵니다.

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

페이지 매김을 사용 하지 않고 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1의 모든 이벤트 눈금 도메인 항목을 나열 \` \` \` \` 합니다 (모든 결과가 단일 샷에 반환 됨).

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

\`페이지 매김을 사용 하지 않는 리소스 그룹 MyResourceGroupName의 이벤트 그리드 도메인 Domain1에서 모든 이벤트 그리드 도메인 항목 나열 \` \` \` (모든 결과가 단일 샷에 반환 됨) ResourceId 옵션

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

\` \` \` \` 한 번에 10 개의 도메인 항목을 쿼리 하 $odataFilter를 충족 하는 리소스 그룹 MyResourceGroupName의 도메인 Domain1에서 이벤트 눈금 도메인 항목 (있는 경우)을 나열 합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다. 도메인 항목의 다음 페이지를 가져오기 위해 사용자는 Get-AzEventGridDomainTopic 다시 호출 하 고 결과를 사용 합니다. 이전 통화에서 얻은 NextLink. 호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.

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

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -이름
EventGrid 도메인 주제 이름입니다.

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
가져올 리소스의 다음 페이지에 대 한 링크입니다. 이 값은 추가 리소스를 계속 쿼리할 수 있는 첫 번째 Get-AzEventGrid cmdlet 호출을 사용 하 여 가져옵니다.

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
목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다. 현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.

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
이벤트 그리드 도메인 또는 그리드 도메인 항목을 나타내는 리소스 식별자입니다.

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

### -위쪽
목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다. 현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### 시스템. i i.

## 출력

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance

## 상속자

## 관련 링크
