---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226457"
---
# <span data-ttu-id="059fc-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="059fc-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="059fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059fc-102">SYNOPSIS</span></span>
<span data-ttu-id="059fc-103">지정 된 구독 및 리소스 그룹에서 지정한 이름을 가진 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="059fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="059fc-104">SYNTAX</span></span>

### <span data-ttu-id="059fc-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="059fc-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="059fc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="059fc-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="059fc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="059fc-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="059fc-108">목록</span><span class="sxs-lookup"><span data-stu-id="059fc-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="059fc-109">설명은</span><span class="sxs-lookup"><span data-stu-id="059fc-109">DESCRIPTION</span></span>
<span data-ttu-id="059fc-110">지정 된 구독 및 리소스 그룹에서 지정한 이름을 가진 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="059fc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="059fc-111">EXAMPLES</span></span>

### <span data-ttu-id="059fc-112">예제 1: 시계열 insights 환경 가져오기</span><span class="sxs-lookup"><span data-stu-id="059fc-112">Example 1: Get a time series insights environment</span></span>
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

<span data-ttu-id="059fc-113">이 명령은 시계열 insights 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="059fc-114">예제 2: 모든 시계열 insights 환경 나열</span><span class="sxs-lookup"><span data-stu-id="059fc-114">Example 2: List all time series insights environments</span></span>
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

<span data-ttu-id="059fc-115">이 명령은 리소스 그룹의 모든 시계열 insights 환경을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="059fc-116">예제 3: 개체 별로 시계열 insights 환경 가져오기</span><span class="sxs-lookup"><span data-stu-id="059fc-116">Example 3: Get a time series insights environment by object</span></span>
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

<span data-ttu-id="059fc-117">이 명령은 시계열 insights 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="059fc-118">변수</span><span class="sxs-lookup"><span data-stu-id="059fc-118">PARAMETERS</span></span>

### <span data-ttu-id="059fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059fc-119">-DefaultProfile</span></span>
<span data-ttu-id="059fc-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="059fc-121">-확장</span><span class="sxs-lookup"><span data-stu-id="059fc-121">-Expand</span></span>
<span data-ttu-id="059fc-122">$Expand = status 설정에는 시계열 Insights 서비스에 환경에 대 한 내부 서비스의 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

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

### <span data-ttu-id="059fc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="059fc-123">-InputObject</span></span>
<span data-ttu-id="059fc-124">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="059fc-125">-이름</span><span class="sxs-lookup"><span data-stu-id="059fc-125">-Name</span></span>
<span data-ttu-id="059fc-126">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="059fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="059fc-128">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="059fc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="059fc-129">-SubscriptionId</span></span>
<span data-ttu-id="059fc-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="059fc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059fc-131">CommonParameters</span></span>
<span data-ttu-id="059fc-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059fc-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="059fc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059fc-134">입력</span><span class="sxs-lookup"><span data-stu-id="059fc-134">INPUTS</span></span>

### <span data-ttu-id="059fc-135">ITimeSeriesInsightsIdentity (Microsoft. PowerShell. i m m)</span><span class="sxs-lookup"><span data-stu-id="059fc-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="059fc-136">출력</span><span class="sxs-lookup"><span data-stu-id="059fc-136">OUTPUTS</span></span>

### <span data-ttu-id="059fc-137">Api20200515. a PowerShell. a i i. a i m.</span><span class="sxs-lookup"><span data-stu-id="059fc-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="059fc-138">상속자</span><span class="sxs-lookup"><span data-stu-id="059fc-138">NOTES</span></span>

<span data-ttu-id="059fc-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="059fc-139">ALIASES</span></span>

<span data-ttu-id="059fc-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="059fc-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="059fc-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="059fc-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="059fc-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="059fc-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="059fc-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="059fc-144">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="059fc-145">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="059fc-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="059fc-146">`[EventSourceName <String>]`: 지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="059fc-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="059fc-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="059fc-148">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="059fc-149">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="059fc-150">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="059fc-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="059fc-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="059fc-151">RELATED LINKS</span></span>

