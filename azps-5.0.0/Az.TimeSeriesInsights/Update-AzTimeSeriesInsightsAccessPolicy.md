---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215995"
---
# <span data-ttu-id="a57d1-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a57d1-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="a57d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a57d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a57d1-103">지정 된 구독, 리소스 그룹 및 환경에서 지정한 이름으로 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a57d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a57d1-104">SYNTAX</span></span>

### <span data-ttu-id="a57d1-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a57d1-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a57d1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a57d1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a57d1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a57d1-107">DESCRIPTION</span></span>
<span data-ttu-id="a57d1-108">지정 된 구독, 리소스 그룹 및 환경에서 지정한 이름으로 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a57d1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a57d1-109">EXAMPLES</span></span>

### <span data-ttu-id="a57d1-110">예제 1: 이름으로 지정 된 액세스 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="a57d1-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="a57d1-111">이 명령은 지정 된 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="a57d1-112">예제 2: 개체 별로 지정 된 액세스 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="a57d1-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="a57d1-113">이 명령은 지정 된 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="a57d1-114">변수</span><span class="sxs-lookup"><span data-stu-id="a57d1-114">PARAMETERS</span></span>

### <span data-ttu-id="a57d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57d1-115">-DefaultProfile</span></span>
<span data-ttu-id="a57d1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57d1-117">-설명</span><span class="sxs-lookup"><span data-stu-id="a57d1-117">-Description</span></span>
<span data-ttu-id="a57d1-118">액세스 정책에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="a57d1-119">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="a57d1-119">-EnvironmentName</span></span>
<span data-ttu-id="a57d1-120">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a57d1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a57d1-121">-InputObject</span></span>
<span data-ttu-id="a57d1-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a57d1-123">-이름</span><span class="sxs-lookup"><span data-stu-id="a57d1-123">-Name</span></span>
<span data-ttu-id="a57d1-124">지정 된 환경과 연결 된 시계열 Insights 액세스 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="a57d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="a57d1-126">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a57d1-127">-역할</span><span class="sxs-lookup"><span data-stu-id="a57d1-127">-Role</span></span>
<span data-ttu-id="a57d1-128">환경에서 주체가 할당 되는 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-128">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="a57d1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a57d1-129">-SubscriptionId</span></span>
<span data-ttu-id="a57d1-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a57d1-131">-확인</span><span class="sxs-lookup"><span data-stu-id="a57d1-131">-Confirm</span></span>
<span data-ttu-id="a57d1-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57d1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57d1-133">-WhatIf</span></span>
<span data-ttu-id="a57d1-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57d1-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57d1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57d1-136">CommonParameters</span></span>
<span data-ttu-id="a57d1-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57d1-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a57d1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57d1-139">입력</span><span class="sxs-lookup"><span data-stu-id="a57d1-139">INPUTS</span></span>

### <span data-ttu-id="a57d1-140">ITimeSeriesInsightsIdentity (Microsoft. PowerShell. i m m)</span><span class="sxs-lookup"><span data-stu-id="a57d1-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a57d1-141">출력</span><span class="sxs-lookup"><span data-stu-id="a57d1-141">OUTPUTS</span></span>

### <span data-ttu-id="a57d1-142">Api20200515. IAccessPolicyResource에 대 한 정보를 모두 보세요.</span><span class="sxs-lookup"><span data-stu-id="a57d1-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="a57d1-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a57d1-143">NOTES</span></span>

<span data-ttu-id="a57d1-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="a57d1-144">ALIASES</span></span>

<span data-ttu-id="a57d1-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a57d1-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a57d1-146">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a57d1-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a57d1-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a57d1-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a57d1-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a57d1-149">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a57d1-150">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="a57d1-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a57d1-151">`[EventSourceName <String>]`: 지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a57d1-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a57d1-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a57d1-153">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a57d1-154">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a57d1-155">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a57d1-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a57d1-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a57d1-156">RELATED LINKS</span></span>

