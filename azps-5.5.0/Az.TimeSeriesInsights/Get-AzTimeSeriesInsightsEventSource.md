---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198324"
---
# <span data-ttu-id="b0b01-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="b0b01-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="b0b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b01-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b01-103">지정된 환경에서 지정된 이름의 이벤트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="b0b01-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0b01-104">SYNTAX</span></span>

### <span data-ttu-id="b0b01-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="b0b01-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0b01-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b0b01-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0b01-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0b01-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0b01-108">설명</span><span class="sxs-lookup"><span data-stu-id="b0b01-108">DESCRIPTION</span></span>
<span data-ttu-id="b0b01-109">지정된 환경에서 지정된 이름의 이벤트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="b0b01-110">예제</span><span class="sxs-lookup"><span data-stu-id="b0b01-110">EXAMPLES</span></span>

### <span data-ttu-id="b0b01-111">예제 1: 지정된 환경의 모든 이벤트 원본 나열</span><span class="sxs-lookup"><span data-stu-id="b0b01-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="b0b01-112">이 명령은 지정된 환경의 모든 이벤트 원본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="b0b01-113">예제 2: 이름에 따라 지정된 이벤트 원본을 얻게</span><span class="sxs-lookup"><span data-stu-id="b0b01-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="b0b01-114">이 명령은 특정 이벤트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="b0b01-115">예제 3: 개체에 따라 지정된 이벤트 원본을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="b0b01-116">이 명령은 특정 이벤트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="b0b01-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b01-117">PARAMETERS</span></span>

### <span data-ttu-id="b0b01-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b01-118">-DefaultProfile</span></span>
<span data-ttu-id="b0b01-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b01-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b0b01-120">-EnvironmentName</span></span>
<span data-ttu-id="b0b01-121">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="b0b01-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b01-122">-InputObject</span></span>
<span data-ttu-id="b0b01-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b0b01-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b0b01-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b01-124">-Name</span></span>
<span data-ttu-id="b0b01-125">지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b01-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b01-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0b01-127">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="b0b01-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0b01-128">-SubscriptionId</span></span>
<span data-ttu-id="b0b01-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b01-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b01-130">CommonParameters</span></span>
<span data-ttu-id="b0b01-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b01-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0b01-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b01-133">입력</span><span class="sxs-lookup"><span data-stu-id="b0b01-133">INPUTS</span></span>

### <span data-ttu-id="b0b01-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="b0b01-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="b0b01-135">출력</span><span class="sxs-lookup"><span data-stu-id="b0b01-135">OUTPUTS</span></span>

### <span data-ttu-id="b0b01-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="b0b01-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="b0b01-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0b01-137">NOTES</span></span>

<span data-ttu-id="b0b01-138">별칭</span><span class="sxs-lookup"><span data-stu-id="b0b01-138">ALIASES</span></span>

<span data-ttu-id="b0b01-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b0b01-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0b01-140">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0b01-141">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0b01-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0b01-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0b01-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0b01-143">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="b0b01-144">`[EnvironmentName <String>]`: 환경의 이름</span><span class="sxs-lookup"><span data-stu-id="b0b01-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="b0b01-145">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="b0b01-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b0b01-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0b01-147">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="b0b01-148">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="b0b01-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b01-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b0b01-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0b01-150">RELATED LINKS</span></span>

