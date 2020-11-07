---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: f2f3c3799ff16cdcc5f1091f8a66cb531cf46cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877857"
---
# Get-AzEventGridDomain

## SYNOPSIS
이벤트 그리드 도메인의 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 그리드 도메인의 목록을 가져옵니다.

## 구문과

### ResourceGroupNameParameterSet (기본값)
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DomainNameParameterSet
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
Get-AzEventGridDomain cmdlet은 지정 된 이벤트 그리드 도메인의 세부 정보 또는 현재 Azure 구독에 있는 모든 이벤트 그리드 도메인의 목록 중 하나를 가져옵니다.
도메인 이름이 제공 되 면 단일 이벤트 그리드 도메인의 세부 정보가 반환 됩니다.
도메인 이름이 제공 되지 않으면 도메인 목록이 반환 됩니다. 이 목록에 반환 되는 요소 수는 Top 매개 변수를 통해 제어 됩니다. Top 값을 지정 하지 않거나 $null 하는 경우 목록에는 한 번에 반환 된 모든 도메인 항목이 포함 됩니다. 그렇지 않으면 Top은 목록에 반환 될 최대 요소 수를 나타냅니다.
계속 사용할 수 있는 도메인이 더 있으면 다음 호출에서 도메인의 다음 페이지를 가져오기 위해 NextLink의 값을 사용 해야 합니다.
마지막으로, ODataQuery 매개 변수를 사용 하 여 검색 결과에 대 한 필터링을 수행 합니다. 필터링 쿼리는 Name 속성에만 사용 하 여 OData 구문을 따릅니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.

## 예제의

### 예제 1

\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1의 세부 정보를 가져옵니다 \` \` .

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### 예제 2

\` \` \` \` ResourceId 옵션을 사용 하 여 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 도메인 Domain1의 세부 정보를 가져옵니다.

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### 예제 3

페이지 매김을 사용 하지 않고 리소스 그룹 MyResourceGroupName의 모든 이벤트 그리드 도메인 나열 \` \` (모든 도메인이 하나의 샷에 반환 됨)

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### 예제 4

\` \` 한 번에 10 개의 도메인을 쿼리 하 $odataFilter를 만족 하는 이벤트 그리드 도메인 (있는 경우)을 리소스 그룹 MyResourceGroupName에 나열 합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다. 도메인의 다음 페이지를 가져오기 위해 사용자는 Get-AzEventGridDomain를 다시 호출 하 고 결과를 사용 하는 것으로 예상 됩니다. 이전 통화에서 얻은 NextLink. 호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### 예제 5

페이지 매김을 사용 하지 않고 Azure 구독에 모든 이벤트 그리드 도메인 나열 (모든 도메인이 한 번에 반환 됨)

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### 예제 6

Azure 구독에서 한 번에 20 개의 도메인을 쿼리 하는 $odataFilter를 만족 하는 이벤트 그리드 도메인 (있는 경우)을 나열 합니다. 더 많은 결과를 사용할 수 있는 경우 $result. NextLink는 $null 되지 않습니다. 도메인의 다음 페이지를 가져오기 위해 사용자는 Get-AzEventGridDomain를 다시 호출 하 고 결과를 사용 하는 것으로 예상 됩니다. 이전 통화에서 얻은 NextLink. 호출자가 결과를 중지 해야 합니다. NextLink는 $null 됩니다.

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
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

### -이름
EventGrid 도메인 이름입니다.

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextLink
가져올 리소스의 다음 페이지에 대 한 링크입니다.
이 값은 추가 리소스를 계속 쿼리할 수 있는 첫 번째 Get-AzEventGrid cmdlet 호출을 사용 하 여 가져옵니다.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery
목록 결과를 필터링 하는 데 사용 되는 OData 쿼리입니다.
현재는 이름 속성 에서만 필터링이 허용 됩니다. 지원 되는 작업에는 CONTAINS, eq (동등), ne (같지 않음), AND, OR 등이 포함 됩니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
이벤트 그리드 도메인을 나타내는 리소스 식별자입니다.

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

### -위쪽
얻을 수 있는 최대 리소스 수입니다.
유효한 값은 1 ~ 100입니다.
Top 값이 지정 되 고 더 많은 결과를 사용할 수 있는 경우 결과에는 NextLink에서 쿼리할 다음 페이지에 대 한 링크가 포함 됩니다.
Top 값을 지정 하지 않으면 전체 리소스 목록이 한 번에 반환 됩니다.

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### OmainListInstance Microsoft.Azure.Commands.EventGrid.Models.PSD

## 상속자

## 관련 링크
