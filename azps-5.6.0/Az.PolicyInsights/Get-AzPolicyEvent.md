---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 7c9ee7af59acc90fba6a17e78ffd3dfc4822472d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989170"
---
# <span data-ttu-id="4bbbd-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4bbbd-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="4bbbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbbd-103">리소스가 만들어지거나 업데이트될 때 생성된 정책 평가 이벤트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="4bbbd-104">구문</span><span class="sxs-lookup"><span data-stu-id="4bbbd-104">SYNTAX</span></span>

### <span data-ttu-id="4bbbd-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="4bbbd-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbbd-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="4bbbd-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbbd-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="4bbbd-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbbd-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="4bbbd-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbbd-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="4bbbd-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbbd-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="4bbbd-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbbd-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="4bbbd-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbbd-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="4bbbd-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bbbd-113">설명</span><span class="sxs-lookup"><span data-stu-id="4bbbd-113">DESCRIPTION</span></span>
<span data-ttu-id="4bbbd-114">리소스가 만들어지거나 업데이트될 때 생성된 정책 평가 이벤트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="4bbbd-115">정책 이벤트 레코드는 지정된 시간 간격(기본값에서 마지막 날)에 따라 다양한 범위에서 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="4bbbd-116">결과를 필터링하고 그룹화하고 그룹 집계를 계산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="4bbbd-117">예제</span><span class="sxs-lookup"><span data-stu-id="4bbbd-117">EXAMPLES</span></span>

### <span data-ttu-id="4bbbd-118">예제 1: 현재 구독 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="4bbbd-119">현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="4bbbd-120">예제 2: 지정된 구독 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="4bbbd-121">지정된 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="4bbbd-122">예제 3: 관리 그룹 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="4bbbd-123">지정된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="4bbbd-124">예제 4: 현재 구독의 리소스 그룹 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="4bbbd-125">지정된 리소스 그룹 내의 모든 리소스(현재 세션 컨텍스트의 구독)에 대한 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="4bbbd-126">예제 5: 지정된 구독의 리소스 그룹 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="4bbbd-127">지정된 리소스 그룹 내의 모든 리소스(지정된 구독에서)에 대한 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="4bbbd-128">예제 6: 리소스에 대한 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="4bbbd-129">지정된 리소스에 대한 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="4bbbd-130">예제 7: 현재 구독에서 정책 집합 정의에 대한 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="4bbbd-131">지정된 정책 집합 정의(현재 세션 컨텍스트의 구독에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="4bbbd-132">예제 8: 지정된 구독에서 정책 집합 정의에 대한 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="4bbbd-133">지정된 정책 집합 정의(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="4bbbd-134">예제 9: 현재 구독에서 정책 정의에 대한 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="4bbbd-135">지정된 정책 정의(현재 세션 컨텍스트의 구독에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="4bbbd-136">예제 10: 지정된 구독에서 정책 정의에 대한 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="4bbbd-137">지정된 정책 정의(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="4bbbd-138">예제 11: 현재 구독에서 정책 할당에 대한 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="4bbbd-139">지정된 정책 할당(현재 세션 컨텍스트의 구독에 있는 구독에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="4bbbd-140">예제 12: 지정된 구독에서 정책 할당에 대한 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="4bbbd-141">지정된 정책 할당(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="4bbbd-142">예제 13: 현재 구독의 지정된 리소스 그룹에서 정책 할당에 대한 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="4bbbd-143">지정된 정책 할당(현재 세션 컨텍스트의 구독의 리소스 그룹에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="4bbbd-144">예제 14: OrderBy, Top 및 Select 쿼리 옵션을 사용하여 현재 구독 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="4bbbd-145">현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="4bbbd-146">명령은 타임스탬프 및 정책 할당 이름 속성에 따라 결과를 순서대로 지정하고 해당 순서대로 나열된 상위 5개만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="4bbbd-147">또한 각 레코드에 대한 열의 하위 집합만 나열하기로 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="4bbbd-148">예제 15: 시작 및 쿼리 옵션으로 현재 구독 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="4bbbd-149">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정된 날짜 범위 내에서 생성된 정책 이벤트 레코드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="4bbbd-150">예제 16: 필터 쿼리 옵션을 사용하여 현재 구독 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="4bbbd-151">현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="4bbbd-152">명령은 정책 정의 작업(거부 또는 감사 작업 포함) 및 리소스 위치(eastus 위치 제외)에 따라 필터링하여 반환되는 결과를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="4bbbd-153">예제 17: 행 수 집계 적용을 사용하여 현재 구독 범위에서 정책 이벤트 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="4bbbd-154">현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드의 수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="4bbbd-155">명령은 추가Properties 속성 내에서 반환되는 정책 이벤트 레코드의 수만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="4bbbd-156">예제 18: 집계를 사용하여 그룹 지정 적용을 사용하여 현재 구독 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="4bbbd-157">현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="4bbbd-158">명령은 정책 정의 작업(감사 및 거부 이벤트만 포함)에 따라 필터링하여 반환되는 결과를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="4bbbd-159">정책 할당, 정책 정의, 정책 정의 작업 및 리소스 ID에 따라 결과를 그룹화하고, 추가Properties 속성 내에서 반환되는 각 그룹의 레코드 수를 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="4bbbd-160">내선 순서로 개수 집계를 통해 결과를 순서대로 순서를 정하고, 해당 순서대로 나열된 상위 5개만이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="4bbbd-161">예제 19: 집계 없이 그룹 지정 적용을 사용하여 현재 구독 범위에서 정책 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="4bbbd-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="4bbbd-162">현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="4bbbd-163">명령은 정책 정의 작업(감사 및 거부 이벤트만 포함)에 따라 필터링하여 반환되는 결과를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="4bbbd-164">리소스 ID를 기반으로 결과를 그룹화합니다. 그러면 하나 이상의 감사 또는 거부 정책에 대한 정책 이벤트를 생성한 구독 내의 모든 리소스 목록을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="4bbbd-165">예제 20: 여러 그룹 지정 적용을 사용하여 현재 구독 범위에서 정책 이벤트 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="4bbbd-166">현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="4bbbd-167">명령은 정책 정의 작업(거부 이벤트만 포함)에 따라 필터링하여 반환되는 결과를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="4bbbd-168">정책 할당, 정책 정의 및 리소스 ID를 기준으로 결과를 먼저 그룹화합니다. 그런 다음 리소스 ID를 제외한 동일한 속성으로 이 그룹화의 결과를 더 그룹화하고, 이러한 각 그룹의 레코드 수를 계산합니다. 이는 AdditionalProperties 속성 내에서 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="4bbbd-169">내선 순서로 개수 집계를 통해 결과를 순서대로 순서를 정하고, 해당 순서대로 나열된 상위 5개만이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="4bbbd-170">이렇게 하여 거부된 리소스 수가 가장 많은 상위 5개 거부 정책을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="4bbbd-171">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4bbbd-171">PARAMETERS</span></span>

### <span data-ttu-id="4bbbd-172">-적용</span><span class="sxs-lookup"><span data-stu-id="4bbbd-172">-Apply</span></span>
<span data-ttu-id="4bbbd-173">OData 표기어를 사용하여 집계에 식을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="4bbbd-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbbd-174">-DefaultProfile</span></span>
<span data-ttu-id="4bbbd-175">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bbbd-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="4bbbd-176">-Filter</span></span>
<span data-ttu-id="4bbbd-177">OData 표기어를 사용하여 식 필터링</span><span class="sxs-lookup"><span data-stu-id="4bbbd-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="4bbbd-178">-From</span><span class="sxs-lookup"><span data-stu-id="4bbbd-178">-From</span></span>
<span data-ttu-id="4bbbd-179">쿼리할 간격의 시작 시간을 지정하는 ISO 8601 서식 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="4bbbd-180">지정하지 않으면 기본값은 'To' 매개 변수 값에서 1일을 1일로 입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="4bbbd-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbbd-181">-ManagementGroupName</span></span>
<span data-ttu-id="4bbbd-182">관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-182">Management group name.</span></span>

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

### <span data-ttu-id="4bbbd-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="4bbbd-183">-OrderBy</span></span>
<span data-ttu-id="4bbbd-184">OData 표기어를 사용하여 식 순서를 정합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="4bbbd-185">선택적 'desc'(기본값) 또는 'asc'가 있는 하나 이상의 콤마로 구분된 열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="4bbbd-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="4bbbd-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="4bbbd-187">정책 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="4bbbd-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="4bbbd-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="4bbbd-189">정책 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-189">Policy definition name.</span></span>

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

### <span data-ttu-id="4bbbd-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="4bbbd-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="4bbbd-191">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="4bbbd-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbbd-192">-ResourceGroupName</span></span>
<span data-ttu-id="4bbbd-193">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-193">Resource group name.</span></span>

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

### <span data-ttu-id="4bbbd-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bbbd-194">-ResourceId</span></span>
<span data-ttu-id="4bbbd-195">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-195">Resource ID.</span></span>

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

### <span data-ttu-id="4bbbd-196">-Select</span><span class="sxs-lookup"><span data-stu-id="4bbbd-196">-Select</span></span>
<span data-ttu-id="4bbbd-197">OData 표기식을 사용하여 식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-197">Select expression using OData notation.</span></span>
<span data-ttu-id="4bbbd-198">하나 이상의 콤마로 구분된 열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="4bbbd-199">각 레코드의 열을 요청된 열로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="4bbbd-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bbbd-200">-SubscriptionId</span></span>
<span data-ttu-id="4bbbd-201">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-201">Subscription ID.</span></span>

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

### <span data-ttu-id="4bbbd-202">-To</span><span class="sxs-lookup"><span data-stu-id="4bbbd-202">-To</span></span>
<span data-ttu-id="4bbbd-203">쿼리할 간격의 종료 시간을 지정하는 ISO 8601 서식 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="4bbbd-204">지정하지 않으면 기본적으로 요청 시간으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="4bbbd-205">-Top</span><span class="sxs-lookup"><span data-stu-id="4bbbd-205">-Top</span></span>
<span data-ttu-id="4bbbd-206">반환할 최대 레코드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="4bbbd-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbbd-207">CommonParameters</span></span>
<span data-ttu-id="4bbbd-208">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4bbbd-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbbd-209">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bbbd-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbbd-210">입력</span><span class="sxs-lookup"><span data-stu-id="4bbbd-210">INPUTS</span></span>

### <span data-ttu-id="4bbbd-211">System.String</span><span class="sxs-lookup"><span data-stu-id="4bbbd-211">System.String</span></span>

## <span data-ttu-id="4bbbd-212">출력</span><span class="sxs-lookup"><span data-stu-id="4bbbd-212">OUTPUTS</span></span>

### <span data-ttu-id="4bbbd-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4bbbd-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="4bbbd-214">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4bbbd-214">NOTES</span></span>

## <span data-ttu-id="4bbbd-215">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bbbd-215">RELATED LINKS</span></span>
