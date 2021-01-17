---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372513"
---
# <span data-ttu-id="ec1b7-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ec1b7-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="ec1b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec1b7-103">리소스에 대한 정책 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="ec1b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec1b7-104">SYNTAX</span></span>

### <span data-ttu-id="ec1b7-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="ec1b7-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec1b7-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="ec1b7-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec1b7-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="ec1b7-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec1b7-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="ec1b7-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec1b7-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="ec1b7-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec1b7-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="ec1b7-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec1b7-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="ec1b7-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec1b7-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="ec1b7-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec1b7-113">설명</span><span class="sxs-lookup"><span data-stu-id="ec1b7-113">DESCRIPTION</span></span>
<span data-ttu-id="ec1b7-114">리소스에 대한 정책 준수 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="ec1b7-115">다양한 범위에서 정책 상태 레코드를Queried할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="ec1b7-116">지정된 시간 간격(기본값-마지막 날)에 따라 최신 정책 상태 또는 모든 정책 상태 전환을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="ec1b7-117">결과를 필터링, 그룹화 및 그룹 집계를 계산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="ec1b7-118">예제</span><span class="sxs-lookup"><span data-stu-id="ec1b7-118">EXAMPLES</span></span>

### <span data-ttu-id="ec1b7-119">예제 1: 현재 구독 범위에서 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="ec1b7-120">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="ec1b7-121">예제 2: 지정된 구독 범위에서 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="ec1b7-122">지정된 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="ec1b7-123">예제 3: 현재 구독 범위의 모든 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="ec1b7-124">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 모든 기록 정책 상태 레코드(최신 포함)를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="ec1b7-125">예제 4: 관리 그룹 범위에서 최신 정책 상태 얻기</span><span class="sxs-lookup"><span data-stu-id="ec1b7-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="ec1b7-126">지정된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="ec1b7-127">예제 5: 현재 구독의 리소스 그룹 범위에서 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="ec1b7-128">지정된 리소스 그룹 내의 모든 리소스(현재 세션 컨텍스트의 구독에서)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="ec1b7-129">예제 6: 지정된 구독의 리소스 그룹 범위에서 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="ec1b7-130">지정된 리소스 그룹 내의 모든 리소스(지정된 구독에서)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="ec1b7-131">예제 7: 리소스에 대한 최신 정책 상태 얻기</span><span class="sxs-lookup"><span data-stu-id="ec1b7-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="ec1b7-132">지정된 리소스에 대한 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="ec1b7-133">예제 8: 현재 구독의 정책 집합 정의에 대한 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ec1b7-134">지정된 정책 집합 정의(현재 세션 컨텍스트의 구독에 존재하는)의 영향을 에 따라 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ec1b7-135">예제 9: 지정된 구독에서 정책 집합 정의에 대한 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ec1b7-136">지정된 정책 집합 정의(지정된 구독에 있는)의 영향을 을(를) 적용하는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ec1b7-137">예제 10: 현재 구독의 정책 정의에 대한 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ec1b7-138">지정된 정책 정의(현재 세션 컨텍스트의 구독에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ec1b7-139">예제 11: 지정된 구독에서 정책 정의에 대한 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="ec1b7-140">지정된 정책 정의(지정된 구독에 있는)의 영향을 을(를) 적용하는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ec1b7-141">예제 12: 현재 구독에서 정책 할당에 대한 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ec1b7-142">지정된 정책 할당(현재 세션 컨텍스트의 구독에 있는)의 영향을 에인한 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="ec1b7-143">예제 13: 지정된 구독에서 정책 할당에 대한 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ec1b7-144">지정된 정책 할당(지정된 구독에 있는)의 영향을 을(를) 적용하는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="ec1b7-145">예제 14: 현재 구독의 지정된 리소스 그룹에서 정책 할당에 대한 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="ec1b7-146">지정된 정책 할당(현재 세션 컨텍스트의 구독에 있는 리소스 그룹에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="ec1b7-147">예제 15: OrderBy, Top 및 Select 쿼리 옵션을 사용하여 현재 구독 범위의 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="ec1b7-148">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ec1b7-149">이 명령은 타임스탬프 및 정책 할당 이름 속성에 따라 결과를 순서대로 지정하고 해당 순서대로 나열된 상위 5개만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="ec1b7-150">또한 각 레코드에 대한 열의 하위 집합만 나열할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="ec1b7-151">예제 16: From 및 To 쿼리 옵션을 사용하여 현재 구독 범위의 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="ec1b7-152">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정된 날짜 범위 내에서 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="ec1b7-153">예제 17: 필터 쿼리 옵션을 사용하여 현재 구독 범위의 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="ec1b7-154">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="ec1b7-155">이 명령은 정책 정의 작업(거부 또는 감사 작업 포함), 준수 상태(비준수 상태만 포함) 및 리소스 위치(eastus 위치 제외)에 따라 필터링하여 반환되는 결과를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="ec1b7-156">예제 18: 행 수 집계를 지정하는 적용을 사용하여 현재 구독 범위에서 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="ec1b7-157">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드의 수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="ec1b7-158">이 명령은 AdditionalProperties 속성 내에서 반환되는 정책 상태 레코드의 수만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="ec1b7-159">예제 19: 집계를 사용하여 그룹 지정 적용을 사용하여 현재 구독 범위에서 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="ec1b7-160">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ec1b7-161">이 명령은 규정 준수 상태에 따라 필터링하여 반환되는 결과를 제한합니다(비준수 상태만 포함).</span><span class="sxs-lookup"><span data-stu-id="ec1b7-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="ec1b7-162">정책 할당, 정책 집합 정의 및 정책 정의에 따라 결과를 그룹화하고 AdditionalProperties 속성 내에서 반환되는 각 그룹의 레코드 수를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="ec1b7-163">카운트 집계를 내선 순서로 계산하여 결과를 순서대로 순서대로 순서를 정하고 해당 순서대로 나열된 상위 5개만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="ec1b7-164">예제 20: 집계 없이 그룹 지정 적용을 사용하여 현재 구독 범위에서 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="ec1b7-165">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ec1b7-166">이 명령은 규정 준수 상태에 따라 필터링하여 반환되는 결과를 제한합니다(비준수 상태만 포함).</span><span class="sxs-lookup"><span data-stu-id="ec1b7-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="ec1b7-167">리소스 ID에 따라 결과를 그룹화합니다. 그러면 하나 이상의 정책에 대해 규정을 준수하지 않는 구독 내의 모든 리소스 목록이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="ec1b7-168">예제 21: 여러 그룹 지정을 적용하여 현재 구독 범위에서 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="ec1b7-169">예제 22: 리소스에 대한 정책 평가 세부 정보를 포함한 최신 정책 상태 확인</span><span class="sxs-lookup"><span data-stu-id="ec1b7-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="ec1b7-170">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 상태 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="ec1b7-171">이 명령은 규정 준수 상태에 따라 필터링하여 반환되는 결과를 제한합니다(비준수 상태만 포함).</span><span class="sxs-lookup"><span data-stu-id="ec1b7-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="ec1b7-172">정책 할당, 정책 집합 정의, 정책 정의 및 리소스 ID에 따라 결과를 먼저 그룹화합니다. 그런 다음 리소스 ID를 제외한 동일한 속성으로 이 그룹화의 결과를 더 그룹화하고, AdditionalProperties 속성 내에서 반환되는 이러한 각 그룹의 레코드 수를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="ec1b7-173">카운트 집계를 내선 순서로 계산하여 결과를 순서대로 순서대로 순서를 정하고 해당 순서대로 나열된 상위 5개만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="ec1b7-174">그러면 비준수 리소스 수가 가장 많은 상위 5개 정책이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="ec1b7-175">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec1b7-175">PARAMETERS</span></span>

### <span data-ttu-id="ec1b7-176">-All</span><span class="sxs-lookup"><span data-stu-id="ec1b7-176">-All</span></span>
<span data-ttu-id="ec1b7-177">지정된 시간 간격 내에 최신 정책만이 아닌 모든 정책 상태만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="ec1b7-178">-Apply</span><span class="sxs-lookup"><span data-stu-id="ec1b7-178">-Apply</span></span>
<span data-ttu-id="ec1b7-179">OData 표기 방법을 사용하여 집계에 식을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="ec1b7-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec1b7-180">-DefaultProfile</span></span>
<span data-ttu-id="ec1b7-181">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-182">-Expand</span><span class="sxs-lookup"><span data-stu-id="ec1b7-182">-Expand</span></span>
<span data-ttu-id="ec1b7-183">OData 표기 방법을 사용하여 식을 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-183">Expand expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-184">-Filter</span><span class="sxs-lookup"><span data-stu-id="ec1b7-184">-Filter</span></span>
<span data-ttu-id="ec1b7-185">OData 표기 방법을 사용하여 식 필터링</span><span class="sxs-lookup"><span data-stu-id="ec1b7-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="ec1b7-186">-From</span><span class="sxs-lookup"><span data-stu-id="ec1b7-186">-From</span></span>
<span data-ttu-id="ec1b7-187">쿼리할 간격의 시작 시간을 지정하는 ISO 8601 형식 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="ec1b7-188">지정하지 않으면 기본값은 'To' 매개 변수 값에서 1일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ec1b7-189">-ManagementGroupName</span></span>
<span data-ttu-id="ec1b7-190">관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-190">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="ec1b7-191">-OrderBy</span></span>
<span data-ttu-id="ec1b7-192">OData 표기 방법을 사용하여 식 순서를 정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="ec1b7-193">선택적 'desc'(기본값) 또는 'asc'가 있는 하나 이상의 콤마로 구분된 열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="ec1b7-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="ec1b7-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="ec1b7-195">정책 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-195">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ec1b7-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="ec1b7-197">정책 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-197">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ec1b7-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="ec1b7-199">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-199">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec1b7-200">-ResourceGroupName</span></span>
<span data-ttu-id="ec1b7-201">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-201">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec1b7-202">-ResourceId</span></span>
<span data-ttu-id="ec1b7-203">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-203">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-204">-Select</span><span class="sxs-lookup"><span data-stu-id="ec1b7-204">-Select</span></span>
<span data-ttu-id="ec1b7-205">OData 표기 방법을 사용하여 식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-205">Select expression using OData notation.</span></span>
<span data-ttu-id="ec1b7-206">하나 이상의 콤마로 구분된 열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="ec1b7-207">각 레코드의 열을 요청된 열로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="ec1b7-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec1b7-208">-SubscriptionId</span></span>
<span data-ttu-id="ec1b7-209">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-209">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-210">-To</span><span class="sxs-lookup"><span data-stu-id="ec1b7-210">-To</span></span>
<span data-ttu-id="ec1b7-211">쿼리할 간격의 종료 시간을 지정하는 ISO 8601 형식의 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="ec1b7-212">지정하지 않으면 기본값은 요청 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-212">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-213">-Top</span><span class="sxs-lookup"><span data-stu-id="ec1b7-213">-Top</span></span>
<span data-ttu-id="ec1b7-214">반환할 최대 레코드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-214">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1b7-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec1b7-215">CommonParameters</span></span>
<span data-ttu-id="ec1b7-216">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec1b7-217">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec1b7-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec1b7-218">입력</span><span class="sxs-lookup"><span data-stu-id="ec1b7-218">INPUTS</span></span>

### <span data-ttu-id="ec1b7-219">System.String</span><span class="sxs-lookup"><span data-stu-id="ec1b7-219">System.String</span></span>

## <span data-ttu-id="ec1b7-220">출력</span><span class="sxs-lookup"><span data-stu-id="ec1b7-220">OUTPUTS</span></span>

### <span data-ttu-id="ec1b7-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="ec1b7-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="ec1b7-222">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec1b7-222">NOTES</span></span>

## <span data-ttu-id="ec1b7-223">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec1b7-223">RELATED LINKS</span></span>

[<span data-ttu-id="ec1b7-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="ec1b7-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
