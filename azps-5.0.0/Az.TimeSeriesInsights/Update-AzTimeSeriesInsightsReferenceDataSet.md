---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215152"
---
# <span data-ttu-id="1019b-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="1019b-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="1019b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1019b-102">SYNOPSIS</span></span>
<span data-ttu-id="1019b-103">지정 된 구독, 리소스 그룹 및 환경에서 지정한 이름으로 참조 데이터 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="1019b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1019b-104">SYNTAX</span></span>

### <span data-ttu-id="1019b-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1019b-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1019b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1019b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1019b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1019b-107">DESCRIPTION</span></span>
<span data-ttu-id="1019b-108">지정 된 구독, 리소스 그룹 및 환경에서 지정한 이름으로 참조 데이터 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="1019b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1019b-109">EXAMPLES</span></span>

### <span data-ttu-id="1019b-110">예제 1: 이름으로 지정 된 참조 데이터 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="1019b-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="1019b-111">이 명령은 지정 된 참조 데이터 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="1019b-112">예제 2: 개체에 의해 지정 된 참조 데이터 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="1019b-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="1019b-113">이 명령은 지정 된 참조 데이터 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="1019b-114">변수</span><span class="sxs-lookup"><span data-stu-id="1019b-114">PARAMETERS</span></span>

### <span data-ttu-id="1019b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1019b-115">-DefaultProfile</span></span>
<span data-ttu-id="1019b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1019b-117">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="1019b-117">-EnvironmentName</span></span>
<span data-ttu-id="1019b-118">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="1019b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1019b-119">-InputObject</span></span>
<span data-ttu-id="1019b-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1019b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1019b-121">-Name</span></span>
<span data-ttu-id="1019b-122">지정 된 환경과 연결 된 시계열 Insights 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1019b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1019b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1019b-124">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="1019b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1019b-125">-SubscriptionId</span></span>
<span data-ttu-id="1019b-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1019b-127">태그</span><span class="sxs-lookup"><span data-stu-id="1019b-127">-Tag</span></span>
<span data-ttu-id="1019b-128">참조 데이터 집합에 대 한 추가 속성의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="1019b-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1019b-129">-Confirm</span></span>
<span data-ttu-id="1019b-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1019b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1019b-131">-WhatIf</span></span>
<span data-ttu-id="1019b-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1019b-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1019b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1019b-134">CommonParameters</span></span>
<span data-ttu-id="1019b-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1019b-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1019b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1019b-137">입력</span><span class="sxs-lookup"><span data-stu-id="1019b-137">INPUTS</span></span>

### <span data-ttu-id="1019b-138">ITimeSeriesInsightsIdentity (Microsoft. PowerShell. i m m)</span><span class="sxs-lookup"><span data-stu-id="1019b-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="1019b-139">출력</span><span class="sxs-lookup"><span data-stu-id="1019b-139">OUTPUTS</span></span>

### <span data-ttu-id="1019b-140">Api20200515. IReferenceDataSetResource를 호출 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="1019b-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="1019b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1019b-141">NOTES</span></span>

<span data-ttu-id="1019b-142">별칭과</span><span class="sxs-lookup"><span data-stu-id="1019b-142">ALIASES</span></span>

<span data-ttu-id="1019b-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1019b-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1019b-144">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1019b-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1019b-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1019b-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1019b-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1019b-147">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="1019b-148">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="1019b-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="1019b-149">`[EventSourceName <String>]`: 지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="1019b-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="1019b-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1019b-151">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="1019b-152">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="1019b-153">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1019b-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1019b-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1019b-154">RELATED LINKS</span></span>

