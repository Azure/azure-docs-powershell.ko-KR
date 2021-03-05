---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 3ef56e9c554b7efbd762b4b373806aad649e0449
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987448"
---
# <span data-ttu-id="e3863-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e3863-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="e3863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3863-102">SYNOPSIS</span></span>
<span data-ttu-id="e3863-103">지정된 구독, 리소스 그룹 및 환경에서 지정된 이름으로 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="e3863-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3863-104">SYNTAX</span></span>

### <span data-ttu-id="e3863-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e3863-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e3863-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e3863-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3863-107">설명</span><span class="sxs-lookup"><span data-stu-id="e3863-107">DESCRIPTION</span></span>
<span data-ttu-id="e3863-108">지정된 구독, 리소스 그룹 및 환경에서 지정된 이름으로 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="e3863-109">예제</span><span class="sxs-lookup"><span data-stu-id="e3863-109">EXAMPLES</span></span>

### <span data-ttu-id="e3863-110">예제 1: 이름에 따라 지정된 액세스 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="e3863-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e3863-111">이 명령은 지정된 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="e3863-112">예제 2: 개체에 따라 지정된 액세스 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="e3863-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e3863-113">이 명령은 지정된 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="e3863-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3863-114">PARAMETERS</span></span>

### <span data-ttu-id="e3863-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3863-115">-DefaultProfile</span></span>
<span data-ttu-id="e3863-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3863-117">-Description</span><span class="sxs-lookup"><span data-stu-id="e3863-117">-Description</span></span>
<span data-ttu-id="e3863-118">액세스 정책에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-118">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3863-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e3863-119">-EnvironmentName</span></span>
<span data-ttu-id="e3863-120">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e3863-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3863-121">-InputObject</span></span>
<span data-ttu-id="e3863-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e3863-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3863-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e3863-123">-Name</span></span>
<span data-ttu-id="e3863-124">지정된 환경과 연결된 Time Series Insights 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3863-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3863-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3863-126">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e3863-127">-역할</span><span class="sxs-lookup"><span data-stu-id="e3863-127">-Role</span></span>
<span data-ttu-id="e3863-128">주체가 환경에 할당된 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3863-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3863-129">-SubscriptionId</span></span>
<span data-ttu-id="e3863-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e3863-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e3863-131">-Confirm</span></span>
<span data-ttu-id="e3863-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3863-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3863-133">-WhatIf</span></span>
<span data-ttu-id="e3863-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3863-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3863-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3863-136">CommonParameters</span></span>
<span data-ttu-id="e3863-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3863-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3863-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3863-139">입력</span><span class="sxs-lookup"><span data-stu-id="e3863-139">INPUTS</span></span>

### <span data-ttu-id="e3863-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e3863-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e3863-141">출력</span><span class="sxs-lookup"><span data-stu-id="e3863-141">OUTPUTS</span></span>

### <span data-ttu-id="e3863-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="e3863-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="e3863-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3863-143">NOTES</span></span>

<span data-ttu-id="e3863-144">별칭</span><span class="sxs-lookup"><span data-stu-id="e3863-144">ALIASES</span></span>

<span data-ttu-id="e3863-145">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e3863-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3863-146">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3863-147">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3863-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3863-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3863-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3863-149">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e3863-150">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="e3863-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e3863-151">`[EventSourceName <String>]`: 지정된 환경과 연결된 Time Series Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e3863-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e3863-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3863-153">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e3863-154">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e3863-155">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3863-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e3863-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3863-156">RELATED LINKS</span></span>

