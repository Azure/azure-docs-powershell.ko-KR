---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217907"
---
# <span data-ttu-id="9aa9e-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="9aa9e-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="9aa9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aa9e-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa9e-103">지정 된 환경에서 지정한 이름을 가진 참조 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="9aa9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9aa9e-104">SYNTAX</span></span>

### <span data-ttu-id="9aa9e-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9aa9e-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9aa9e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="9aa9e-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9aa9e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9aa9e-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9aa9e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9aa9e-108">DESCRIPTION</span></span>
<span data-ttu-id="9aa9e-109">지정 된 환경에서 지정한 이름을 가진 참조 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="9aa9e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9aa9e-110">EXAMPLES</span></span>

### <span data-ttu-id="9aa9e-111">예제 1: 지정 된 환경에 따라 모든 참조 데이터 집합 나열</span><span class="sxs-lookup"><span data-stu-id="9aa9e-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="9aa9e-112">이 명령은 지정 된 환경에 따라 모든 참조 데이터 집합을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="9aa9e-113">예제 2: 이름으로 지정 된 참조 데이터 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="9aa9e-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="9aa9e-114">이 명령은 지정 된 참조 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="9aa9e-115">예제 3: 개체를 기준으로 지정 된 참조 데이터 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="9aa9e-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="9aa9e-116">이 명령은 지정 된 참조 데이터 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="9aa9e-117">변수</span><span class="sxs-lookup"><span data-stu-id="9aa9e-117">PARAMETERS</span></span>

### <span data-ttu-id="9aa9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa9e-118">-DefaultProfile</span></span>
<span data-ttu-id="9aa9e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aa9e-120">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="9aa9e-120">-EnvironmentName</span></span>
<span data-ttu-id="9aa9e-121">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="9aa9e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aa9e-122">-InputObject</span></span>
<span data-ttu-id="9aa9e-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9aa9e-124">-이름</span><span class="sxs-lookup"><span data-stu-id="9aa9e-124">-Name</span></span>
<span data-ttu-id="9aa9e-125">지정 된 환경과 연결 된 시계열 Insights 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="9aa9e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aa9e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9aa9e-127">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="9aa9e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9aa9e-128">-SubscriptionId</span></span>
<span data-ttu-id="9aa9e-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9aa9e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa9e-130">CommonParameters</span></span>
<span data-ttu-id="9aa9e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa9e-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa9e-133">입력</span><span class="sxs-lookup"><span data-stu-id="9aa9e-133">INPUTS</span></span>

### <span data-ttu-id="9aa9e-134">ITimeSeriesInsightsIdentity (Microsoft. PowerShell. i m m)</span><span class="sxs-lookup"><span data-stu-id="9aa9e-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="9aa9e-135">출력</span><span class="sxs-lookup"><span data-stu-id="9aa9e-135">OUTPUTS</span></span>

### <span data-ttu-id="9aa9e-136">Api20200515. IReferenceDataSetResource를 호출 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="9aa9e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9aa9e-137">NOTES</span></span>

<span data-ttu-id="9aa9e-138">별칭과</span><span class="sxs-lookup"><span data-stu-id="9aa9e-138">ALIASES</span></span>

<span data-ttu-id="9aa9e-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9aa9e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9aa9e-140">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9aa9e-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9aa9e-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9aa9e-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9aa9e-143">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="9aa9e-144">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="9aa9e-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="9aa9e-145">`[EventSourceName <String>]`: 지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="9aa9e-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="9aa9e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9aa9e-147">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="9aa9e-148">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="9aa9e-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa9e-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="9aa9e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9aa9e-150">RELATED LINKS</span></span>

