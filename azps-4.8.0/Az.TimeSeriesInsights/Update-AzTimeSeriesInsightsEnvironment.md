---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212471"
---
# <span data-ttu-id="f5947-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="f5947-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="f5947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5947-102">SYNOPSIS</span></span>
<span data-ttu-id="f5947-103">지정 된 구독 및 리소스 그룹에서 지정한 이름으로 환경을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f5947-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5947-104">SYNTAX</span></span>

### <span data-ttu-id="f5947-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5947-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f5947-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f5947-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5947-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f5947-107">DESCRIPTION</span></span>
<span data-ttu-id="f5947-108">지정 된 구독 및 리소스 그룹에서 지정한 이름으로 환경을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f5947-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f5947-109">EXAMPLES</span></span>

### <span data-ttu-id="f5947-110">예제 1: Gen1 시계열 insights 환경 업데이트</span><span class="sxs-lookup"><span data-stu-id="f5947-110">Example 1: Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="f5947-111">이 명령은 Gen1 시계열 insights 환경을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="f5947-112">예제 2: Gen1 시계열 insights 환경 업데이트</span><span class="sxs-lookup"><span data-stu-id="f5947-112">Example 2:  Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="f5947-113">이 명령은 Gen1 시계열 insights 환경을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="f5947-114">변수</span><span class="sxs-lookup"><span data-stu-id="f5947-114">PARAMETERS</span></span>

### <span data-ttu-id="f5947-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5947-115">-AsJob</span></span>
<span data-ttu-id="f5947-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="f5947-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f5947-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5947-117">-DefaultProfile</span></span>
<span data-ttu-id="f5947-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5947-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5947-119">-InputObject</span></span>
<span data-ttu-id="f5947-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f5947-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f5947-121">-Name</span></span>
<span data-ttu-id="f5947-122">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f5947-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f5947-123">-NoWait</span></span>
<span data-ttu-id="f5947-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="f5947-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f5947-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5947-125">-ResourceGroupName</span></span>
<span data-ttu-id="f5947-126">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f5947-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5947-127">-SubscriptionId</span></span>
<span data-ttu-id="f5947-128">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f5947-129">태그</span><span class="sxs-lookup"><span data-stu-id="f5947-129">-Tag</span></span>
<span data-ttu-id="f5947-130">환경에 대 한 추가 속성의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="f5947-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f5947-131">-Confirm</span></span>
<span data-ttu-id="f5947-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5947-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5947-133">-WhatIf</span></span>
<span data-ttu-id="f5947-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5947-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5947-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5947-136">CommonParameters</span></span>
<span data-ttu-id="f5947-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5947-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5947-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5947-139">입력</span><span class="sxs-lookup"><span data-stu-id="f5947-139">INPUTS</span></span>

### <span data-ttu-id="f5947-140">ITimeSeriesInsightsIdentity (Microsoft. PowerShell. i m m)</span><span class="sxs-lookup"><span data-stu-id="f5947-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f5947-141">출력</span><span class="sxs-lookup"><span data-stu-id="f5947-141">OUTPUTS</span></span>

### <span data-ttu-id="f5947-142">Api20200515. a PowerShell. a i i. a i m.</span><span class="sxs-lookup"><span data-stu-id="f5947-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="f5947-143">상속자</span><span class="sxs-lookup"><span data-stu-id="f5947-143">NOTES</span></span>

<span data-ttu-id="f5947-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="f5947-144">ALIASES</span></span>

<span data-ttu-id="f5947-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f5947-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5947-146">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5947-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5947-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5947-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f5947-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5947-149">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f5947-150">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="f5947-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f5947-151">`[EventSourceName <String>]`: 지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f5947-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="f5947-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5947-153">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f5947-154">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f5947-155">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f5947-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f5947-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5947-156">RELATED LINKS</span></span>

