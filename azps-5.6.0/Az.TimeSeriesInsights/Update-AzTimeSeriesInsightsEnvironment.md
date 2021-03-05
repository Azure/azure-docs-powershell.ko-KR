---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 86e143455f287bef8bff4b391f7f40aa01fba99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987434"
---
# <span data-ttu-id="64f7d-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="64f7d-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="64f7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="64f7d-103">지정된 구독 및 리소스 그룹에 지정된 이름으로 환경을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="64f7d-104">구문</span><span class="sxs-lookup"><span data-stu-id="64f7d-104">SYNTAX</span></span>

### <span data-ttu-id="64f7d-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="64f7d-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64f7d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="64f7d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64f7d-107">설명</span><span class="sxs-lookup"><span data-stu-id="64f7d-107">DESCRIPTION</span></span>
<span data-ttu-id="64f7d-108">지정된 구독 및 리소스 그룹에 지정된 이름으로 환경을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="64f7d-109">예제</span><span class="sxs-lookup"><span data-stu-id="64f7d-109">EXAMPLES</span></span>

### <span data-ttu-id="64f7d-110">예제 1: Gen1 타임 시리즈 인사이트 환경 업데이트</span><span class="sxs-lookup"><span data-stu-id="64f7d-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="64f7d-111">이 명령은 Gen1 타임 시리즈 인사이트 환경을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="64f7d-112">예제 2: Gen1 타임 시리즈 인사이트 환경 업데이트</span><span class="sxs-lookup"><span data-stu-id="64f7d-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="64f7d-113">이 명령은 Gen1 타임 시리즈 인사이트 환경을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="64f7d-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="64f7d-114">PARAMETERS</span></span>

### <span data-ttu-id="64f7d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64f7d-115">-AsJob</span></span>
<span data-ttu-id="64f7d-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="64f7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f7d-117">-DefaultProfile</span></span>
<span data-ttu-id="64f7d-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f7d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64f7d-119">-InputObject</span></span>
<span data-ttu-id="64f7d-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="64f7d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64f7d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="64f7d-121">-Name</span></span>
<span data-ttu-id="64f7d-122">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f7d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64f7d-123">-NoWait</span></span>
<span data-ttu-id="64f7d-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="64f7d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64f7d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f7d-125">-ResourceGroupName</span></span>
<span data-ttu-id="64f7d-126">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f7d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64f7d-127">-SubscriptionId</span></span>
<span data-ttu-id="64f7d-128">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f7d-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="64f7d-129">-Tag</span></span>
<span data-ttu-id="64f7d-130">환경에 대한 추가 속성의 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-130">Key-value pairs of additional properties for the environment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f7d-131">-확인</span><span class="sxs-lookup"><span data-stu-id="64f7d-131">-Confirm</span></span>
<span data-ttu-id="64f7d-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64f7d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f7d-133">-WhatIf</span></span>
<span data-ttu-id="64f7d-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64f7d-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64f7d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f7d-136">CommonParameters</span></span>
<span data-ttu-id="64f7d-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f7d-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64f7d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f7d-139">입력</span><span class="sxs-lookup"><span data-stu-id="64f7d-139">INPUTS</span></span>

### <span data-ttu-id="64f7d-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="64f7d-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="64f7d-141">출력</span><span class="sxs-lookup"><span data-stu-id="64f7d-141">OUTPUTS</span></span>

### <span data-ttu-id="64f7d-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="64f7d-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="64f7d-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64f7d-143">NOTES</span></span>

<span data-ttu-id="64f7d-144">별칭</span><span class="sxs-lookup"><span data-stu-id="64f7d-144">ALIASES</span></span>

<span data-ttu-id="64f7d-145">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="64f7d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64f7d-146">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64f7d-147">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64f7d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64f7d-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="64f7d-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64f7d-149">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="64f7d-150">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="64f7d-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="64f7d-151">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="64f7d-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="64f7d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64f7d-153">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="64f7d-154">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="64f7d-155">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="64f7d-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="64f7d-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64f7d-156">RELATED LINKS</span></span>

