---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1fef5f018791fba9369ce7ab18a4b0c3a2440cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950827"
---
# <span data-ttu-id="99c76-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="99c76-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="99c76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c76-102">SYNOPSIS</span></span>
<span data-ttu-id="99c76-103">지정된 환경에서 지정된 이름으로 참조 데이터 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="99c76-104">구문</span><span class="sxs-lookup"><span data-stu-id="99c76-104">SYNTAX</span></span>

### <span data-ttu-id="99c76-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="99c76-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99c76-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="99c76-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="99c76-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99c76-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="99c76-108">설명</span><span class="sxs-lookup"><span data-stu-id="99c76-108">DESCRIPTION</span></span>
<span data-ttu-id="99c76-109">지정된 환경에서 지정된 이름으로 참조 데이터 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="99c76-110">예제</span><span class="sxs-lookup"><span data-stu-id="99c76-110">EXAMPLES</span></span>

### <span data-ttu-id="99c76-111">예제 1: 지정된 환경 아래에 모든 참조 데이터 집합 나열</span><span class="sxs-lookup"><span data-stu-id="99c76-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="99c76-112">이 명령은 지정된 환경 아래에 있는 모든 참조 데이터 집합을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="99c76-113">예제 2: 이름에 따라 지정된 참조 데이터 집합을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="99c76-114">이 명령은 지정된 참조 데이터 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="99c76-115">예제 3: 개체에 따라 지정된 참조 데이터 집합을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="99c76-116">이 명령은 지정된 참조 데이터 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="99c76-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="99c76-117">PARAMETERS</span></span>

### <span data-ttu-id="99c76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c76-118">-DefaultProfile</span></span>
<span data-ttu-id="99c76-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99c76-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="99c76-120">-EnvironmentName</span></span>
<span data-ttu-id="99c76-121">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="99c76-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99c76-122">-InputObject</span></span>
<span data-ttu-id="99c76-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="99c76-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99c76-124">-Name</span><span class="sxs-lookup"><span data-stu-id="99c76-124">-Name</span></span>
<span data-ttu-id="99c76-125">지정된 환경과 연결된 Time Series Insights 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99c76-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c76-126">-ResourceGroupName</span></span>
<span data-ttu-id="99c76-127">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="99c76-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99c76-128">-SubscriptionId</span></span>
<span data-ttu-id="99c76-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="99c76-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c76-130">CommonParameters</span></span>
<span data-ttu-id="99c76-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c76-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99c76-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c76-133">입력</span><span class="sxs-lookup"><span data-stu-id="99c76-133">INPUTS</span></span>

### <span data-ttu-id="99c76-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="99c76-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="99c76-135">출력</span><span class="sxs-lookup"><span data-stu-id="99c76-135">OUTPUTS</span></span>

### <span data-ttu-id="99c76-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="99c76-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="99c76-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99c76-137">NOTES</span></span>

<span data-ttu-id="99c76-138">별칭</span><span class="sxs-lookup"><span data-stu-id="99c76-138">ALIASES</span></span>

<span data-ttu-id="99c76-139">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="99c76-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99c76-140">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99c76-141">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99c76-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99c76-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="99c76-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99c76-143">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="99c76-144">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="99c76-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="99c76-145">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="99c76-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="99c76-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99c76-147">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="99c76-148">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="99c76-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="99c76-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="99c76-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99c76-150">RELATED LINKS</span></span>

