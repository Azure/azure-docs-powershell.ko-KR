---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 151b8a431183727dbfaec242705421ba775b0b99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011152"
---
# <span data-ttu-id="e9bf6-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="e9bf6-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="e9bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bf6-103">지정된 구독 및 리소스 그룹에 지정된 이름으로 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="e9bf6-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9bf6-104">SYNTAX</span></span>

### <span data-ttu-id="e9bf6-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="e9bf6-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9bf6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e9bf6-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e9bf6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e9bf6-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e9bf6-108">목록</span><span class="sxs-lookup"><span data-stu-id="e9bf6-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e9bf6-109">설명</span><span class="sxs-lookup"><span data-stu-id="e9bf6-109">DESCRIPTION</span></span>
<span data-ttu-id="e9bf6-110">지정된 구독 및 리소스 그룹에 지정된 이름으로 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="e9bf6-111">예제</span><span class="sxs-lookup"><span data-stu-id="e9bf6-111">EXAMPLES</span></span>

### <span data-ttu-id="e9bf6-112">예제 1: 타임 시리즈 인사이트 환경 얻기</span><span class="sxs-lookup"><span data-stu-id="e9bf6-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="e9bf6-113">이 명령은 타임 시리즈 인사이트 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="e9bf6-114">예제 2: 모든 시간 계열 인사이트 환경 나열</span><span class="sxs-lookup"><span data-stu-id="e9bf6-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="e9bf6-115">이 명령은 리소스 그룹의 모든 시간 계열 인사이트 환경을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="e9bf6-116">예제 3: 개체에 따라 타임 시리즈 인사이트 환경 제공</span><span class="sxs-lookup"><span data-stu-id="e9bf6-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="e9bf6-117">이 명령은 타임 시리즈 인사이트 환경을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="e9bf6-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e9bf6-118">PARAMETERS</span></span>

### <span data-ttu-id="e9bf6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bf6-119">-DefaultProfile</span></span>
<span data-ttu-id="e9bf6-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9bf6-121">-확장</span><span class="sxs-lookup"><span data-stu-id="e9bf6-121">-Expand</span></span>
<span data-ttu-id="e9bf6-122">$expand=status를 설정하면 Time Series Insights 서비스의 환경 내부 서비스의 상태가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9bf6-123">-InputObject</span></span>
<span data-ttu-id="e9bf6-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e9bf6-125">-Name</span></span>
<span data-ttu-id="e9bf6-126">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9bf6-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9bf6-128">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-128">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9bf6-129">-SubscriptionId</span></span>
<span data-ttu-id="e9bf6-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bf6-131">CommonParameters</span></span>
<span data-ttu-id="e9bf6-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bf6-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9bf6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bf6-134">입력</span><span class="sxs-lookup"><span data-stu-id="e9bf6-134">INPUTS</span></span>

### <span data-ttu-id="e9bf6-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e9bf6-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e9bf6-136">출력</span><span class="sxs-lookup"><span data-stu-id="e9bf6-136">OUTPUTS</span></span>

### <span data-ttu-id="e9bf6-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="e9bf6-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="e9bf6-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9bf6-138">NOTES</span></span>

<span data-ttu-id="e9bf6-139">별칭</span><span class="sxs-lookup"><span data-stu-id="e9bf6-139">ALIASES</span></span>

<span data-ttu-id="e9bf6-140">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e9bf6-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e9bf6-141">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e9bf6-142">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e9bf6-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e9bf6-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e9bf6-144">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e9bf6-145">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="e9bf6-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e9bf6-146">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e9bf6-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e9bf6-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e9bf6-148">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e9bf6-149">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e9bf6-150">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e9bf6-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e9bf6-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9bf6-151">RELATED LINKS</span></span>

