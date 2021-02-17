---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207549"
---
# <span data-ttu-id="8fbd2-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="8fbd2-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="8fbd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fbd2-102">SYNOPSIS</span></span>
<span data-ttu-id="8fbd2-103">지정된 구독, 리소스 그룹 및 환경에서 지정된 이름으로 참조 데이터 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="8fbd2-104">구문</span><span class="sxs-lookup"><span data-stu-id="8fbd2-104">SYNTAX</span></span>

### <span data-ttu-id="8fbd2-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="8fbd2-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8fbd2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8fbd2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8fbd2-107">설명</span><span class="sxs-lookup"><span data-stu-id="8fbd2-107">DESCRIPTION</span></span>
<span data-ttu-id="8fbd2-108">지정된 구독, 리소스 그룹 및 환경에서 지정된 이름으로 참조 데이터 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="8fbd2-109">예제</span><span class="sxs-lookup"><span data-stu-id="8fbd2-109">EXAMPLES</span></span>

### <span data-ttu-id="8fbd2-110">예제 1: 이름에 따라 지정된 참조 데이터 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="8fbd2-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8fbd2-111">이 명령은 지정된 참조 데이터 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="8fbd2-112">예제 2: 개체에 의해 지정된 참조 데이터 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="8fbd2-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="8fbd2-113">이 명령은 지정된 참조 데이터 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="8fbd2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fbd2-114">PARAMETERS</span></span>

### <span data-ttu-id="8fbd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fbd2-115">-DefaultProfile</span></span>
<span data-ttu-id="8fbd2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fbd2-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="8fbd2-117">-EnvironmentName</span></span>
<span data-ttu-id="8fbd2-118">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="8fbd2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fbd2-119">-InputObject</span></span>
<span data-ttu-id="8fbd2-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8fbd2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8fbd2-121">-Name</span></span>
<span data-ttu-id="8fbd2-122">지정된 환경과 연결된 Time Series Insights 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="8fbd2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fbd2-123">-ResourceGroupName</span></span>
<span data-ttu-id="8fbd2-124">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="8fbd2-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fbd2-125">-SubscriptionId</span></span>
<span data-ttu-id="8fbd2-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8fbd2-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="8fbd2-127">-Tag</span></span>
<span data-ttu-id="8fbd2-128">참조 데이터 집합에 대한 추가 속성의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="8fbd2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fbd2-129">-Confirm</span></span>
<span data-ttu-id="8fbd2-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fbd2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fbd2-131">-WhatIf</span></span>
<span data-ttu-id="8fbd2-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8fbd2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fbd2-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fbd2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fbd2-134">CommonParameters</span></span>
<span data-ttu-id="8fbd2-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fbd2-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fbd2-137">입력</span><span class="sxs-lookup"><span data-stu-id="8fbd2-137">INPUTS</span></span>

### <span data-ttu-id="8fbd2-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="8fbd2-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="8fbd2-139">출력</span><span class="sxs-lookup"><span data-stu-id="8fbd2-139">OUTPUTS</span></span>

### <span data-ttu-id="8fbd2-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="8fbd2-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="8fbd2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8fbd2-141">NOTES</span></span>

<span data-ttu-id="8fbd2-142">별칭</span><span class="sxs-lookup"><span data-stu-id="8fbd2-142">ALIASES</span></span>

<span data-ttu-id="8fbd2-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8fbd2-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8fbd2-144">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8fbd2-145">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8fbd2-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8fbd2-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8fbd2-147">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="8fbd2-148">`[EnvironmentName <String>]`: 환경의 이름</span><span class="sxs-lookup"><span data-stu-id="8fbd2-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="8fbd2-149">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="8fbd2-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8fbd2-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8fbd2-151">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="8fbd2-152">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="8fbd2-153">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbd2-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="8fbd2-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fbd2-154">RELATED LINKS</span></span>

