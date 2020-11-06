---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
ms.openlocfilehash: 0c4e4f531dac3f75f0eff69ba1dcfc644473ea06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531342"
---
# <span data-ttu-id="28d18-101">Get-AzureRmPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="28d18-101">Get-AzureRmPolicyEvent</span></span>

## <span data-ttu-id="28d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28d18-102">SYNOPSIS</span></span>
<span data-ttu-id="28d18-103">리소스가 만들어지거나 업데이트 될 때 생성 되는 정책 평가 이벤트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28d18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28d18-104">SYNTAX</span></span>

### <span data-ttu-id="28d18-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="28d18-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28d18-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="28d18-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28d18-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="28d18-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28d18-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="28d18-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28d18-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="28d18-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28d18-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="28d18-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28d18-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="28d18-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28d18-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="28d18-112">ResourceScope</span></span>
```
Get-AzureRmPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28d18-113">설명은</span><span class="sxs-lookup"><span data-stu-id="28d18-113">DESCRIPTION</span></span>
<span data-ttu-id="28d18-114">리소스가 만들어지거나 업데이트 될 때 생성 되는 정책 평가 이벤트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="28d18-115">정책 이벤트 레코드는 지정 된 시간 간격에 따라 다양 한 범위에서 쿼리할 수 있습니다 (기본적으로 마지막 날).</span><span class="sxs-lookup"><span data-stu-id="28d18-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="28d18-116">결과를 필터링 하 고 그룹화 하 고 그룹 집계를 계산할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="28d18-117">예제의</span><span class="sxs-lookup"><span data-stu-id="28d18-117">EXAMPLES</span></span>

### <span data-ttu-id="28d18-118">예제 1: 현재 구독 범위에서 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent
```

<span data-ttu-id="28d18-119">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="28d18-120">예제 2: 지정 된 구독 범위에서 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="28d18-121">지정 된 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="28d18-122">예제 3: 관리 그룹 범위에서 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="28d18-123">지정 된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="28d18-124">예제 4: 현재 구독의 리소스 그룹 범위에서 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="28d18-125">지정 된 리소스 그룹 (현재 세션 컨텍스트의 구독) 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="28d18-126">예제 5: 지정 된 구독의 리소스 그룹 범위에서 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="28d18-127">지정 된 리소스 그룹 (지정 된 구독) 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="28d18-128">예제 6: 리소스에 대 한 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="28d18-129">지정 된 리소스의 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="28d18-130">예제 7: 현재 구독에서 정책 집합 정의에 대 한 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="28d18-131">현재 세션 컨텍스트의 구독에 있는 지정 된 정책 집합 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="28d18-132">예제 8: 지정 된 구독에서 정책 집합 정의에 대 한 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="28d18-133">지정 된 정책 집합 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="28d18-134">예제 9: 현재 구독에서 정책 정의에 대 한 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="28d18-135">현재 세션 컨텍스트의 구독에 있는 지정 된 정책 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="28d18-136">예제 10: 지정 된 구독에서 정책 정의에 대 한 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="28d18-137">지정 된 정책 정의 (지정 된 구독에 있음)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="28d18-138">예제 11: 현재 구독에서 정책 할당에 대 한 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="28d18-139">지정 된 정책 할당 (현재 세션 컨텍스트의 구독에 있음)에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="28d18-140">예 12: 지정 된 구독에서 정책 할당에 대 한 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="28d18-141">지정 된 정책 할당 (지정 된 구독에 있음)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="28d18-142">예제 13: 현재 구독에서 지정 된 리소스 그룹의 정책 할당에 대 한 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="28d18-143">지정 된 정책 할당 (현재 세션 컨텍스트에서 구독에 있는 리소스 그룹에 있음)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="28d18-144">예제 14: 현재 구독 범위에서 정책 이벤트 가져오기-OrderBy 사용, 상위 및 선택 쿼리 옵션</span><span class="sxs-lookup"><span data-stu-id="28d18-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="28d18-145">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="28d18-146">이 명령은 타임 스탬프 및 정책 할당 이름 속성을 기준으로 결과를 정렬 하 고 해당 순서로 나열 된 상위 5 개만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="28d18-147">또한 각 레코드에 대 한 열의 하위 집합만 나열 하도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="28d18-148">예제 15: From 및 To 쿼리 옵션을 사용 하 여 현재 구독 범위에서 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="28d18-149">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정 된 날짜 범위 내에서 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="28d18-150">예제 16: 필터 쿼리 옵션을 사용 하 여 현재 구독 범위에서 정책 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="28d18-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="28d18-151">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="28d18-152">이 명령은 정책 정의 작업 (거부 또는 감사 작업 포함) 및 리소스 위치 (e\ us 위치 제외)에 따라 필터링 하 여 반환 되는 결과를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="28d18-153">예제 17: Apply를 사용 하 여 현재 구독 범위에서 정책 이벤트 가져오기 행 개수 집계 지정</span><span class="sxs-lookup"><span data-stu-id="28d18-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="28d18-154">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드의 수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="28d18-155">이 명령은 AdditionalProperties 속성 내에서 반환 되는 정책 이벤트 레코드의 수만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="28d18-156">예 18: Apply를 사용 하 여 현재 구독 범위에서 정책 이벤트 가져오기 집계로 그룹화 지정</span><span class="sxs-lookup"><span data-stu-id="28d18-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="28d18-157">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="28d18-158">이 명령은 정책 정의 작업 (감사 및 거부 이벤트만 포함)을 기준으로 필터링 하 여 반환 되는 결과를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="28d18-159">정책 할당, 정책 정의, 정책 정의 작업, 리소스 id를 기준으로 결과를 그룹화 하 고 AdditionalProperties 속성 내에서 반환 되는 각 그룹의 레코드 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="28d18-160">결과를 개수 집계 별로 내림차순으로 정렬 하 고 해당 순서로 나열 된 상위 5 개만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="28d18-161">예제 19: 현재 구독 범위에서 정책 이벤트 가져오기, 적용을 사용 하 여 집계 없이 그룹화 지정</span><span class="sxs-lookup"><span data-stu-id="28d18-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="28d18-162">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="28d18-163">이 명령은 정책 정의 작업 (감사 및 거부 이벤트만 포함)을 기준으로 필터링 하 여 반환 되는 결과를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="28d18-164">리소스 id를 기준으로 결과를 그룹화 합니다. 이렇게 하면 하나 이상의 감사 또는 거부 정책에 대 한 정책 이벤트를 생성 한 구독 내의 모든 리소스 목록이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="28d18-165">예제 20: 적용을 통해 현재 구독 범위에서 정책 이벤트 가져오기 여러 그룹화 지정</span><span class="sxs-lookup"><span data-stu-id="28d18-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="28d18-166">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 정책 이벤트 레코드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="28d18-167">이 명령은 정책 정의 작업 (거부 이벤트만 포함)을 기준으로 필터링 하 여 반환 되는 결과를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="28d18-168">정책 할당, 정책 정의 및 리소스 id를 기준으로 결과를 먼저 그룹화 합니다. 그런 다음이 그룹화의 결과를 리소스 id를 제외한 동일한 속성으로 그룹화 하 고, AdditionalProperties 속성 내에서 반환 되는 이러한 각 그룹의 레코드 수를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="28d18-169">결과를 개수 집계 별로 내림차순으로 정렬 하 고 해당 순서로 나열 된 상위 5 개만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="28d18-170">이렇게 하면 최대 거부 리소스를 포함 하는 상위 5 개 거부 정책이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="28d18-171">변수</span><span class="sxs-lookup"><span data-stu-id="28d18-171">PARAMETERS</span></span>

### <span data-ttu-id="28d18-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="28d18-172">-Apply</span></span>
<span data-ttu-id="28d18-173">OData 표시법을 사용 하 여 집계에 대 한 식을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="28d18-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d18-174">-DefaultProfile</span></span>
<span data-ttu-id="28d18-175">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d18-176">-필터</span><span class="sxs-lookup"><span data-stu-id="28d18-176">-Filter</span></span>
<span data-ttu-id="28d18-177">OData 표시법을 사용 하 여 식을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="28d18-178">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="28d18-178">-From</span></span>
<span data-ttu-id="28d18-179">쿼리 간격의 시작 시간을 지정 하는 ISO 8601 형식이 지정 된 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="28d18-180">지정 하지 않으면 기본적으로 ' To ' 매개 변수 값은 1 일을 뺀 수입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="28d18-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="28d18-181">-ManagementGroupName</span></span>
<span data-ttu-id="28d18-182">관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-182">Management group name.</span></span>

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

### <span data-ttu-id="28d18-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="28d18-183">-OrderBy</span></span>
<span data-ttu-id="28d18-184">OData 표시법을 사용 하는 정렬 식입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="28d18-185">선택적 ' desc ' (기본값) 또는 ' asc '가 있는 하나 이상의 쉼표로 구분 된 열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="28d18-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="28d18-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="28d18-187">정책 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="28d18-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="28d18-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="28d18-189">정책 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-189">Policy definition name.</span></span>

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

### <span data-ttu-id="28d18-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="28d18-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="28d18-191">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="28d18-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d18-192">-ResourceGroupName</span></span>
<span data-ttu-id="28d18-193">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-193">Resource group name.</span></span>

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

### <span data-ttu-id="28d18-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28d18-194">-ResourceId</span></span>
<span data-ttu-id="28d18-195">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-195">Resource ID.</span></span>

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

### <span data-ttu-id="28d18-196">-선택</span><span class="sxs-lookup"><span data-stu-id="28d18-196">-Select</span></span>
<span data-ttu-id="28d18-197">OData 표시법을 사용 하 여 식을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-197">Select expression using OData notation.</span></span>
<span data-ttu-id="28d18-198">하나 이상의 쉼표로 구분 된 열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="28d18-199">각 레코드의 열을 요청한 값 으로만 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="28d18-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28d18-200">-SubscriptionId</span></span>
<span data-ttu-id="28d18-201">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-201">Subscription ID.</span></span>

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

### <span data-ttu-id="28d18-202">-To</span><span class="sxs-lookup"><span data-stu-id="28d18-202">-To</span></span>
<span data-ttu-id="28d18-203">쿼리 간격의 종료 시간을 지정 하는 ISO 8601 형식이 지정 된 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="28d18-204">지정 하지 않으면 기본적으로 요청 시간이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="28d18-205">-위쪽</span><span class="sxs-lookup"><span data-stu-id="28d18-205">-Top</span></span>
<span data-ttu-id="28d18-206">반환할 레코드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="28d18-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d18-207">CommonParameters</span></span>
<span data-ttu-id="28d18-208">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d18-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d18-209">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28d18-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d18-210">입력</span><span class="sxs-lookup"><span data-stu-id="28d18-210">INPUTS</span></span>

### <span data-ttu-id="28d18-211">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28d18-211">System.String</span></span>

## <span data-ttu-id="28d18-212">출력</span><span class="sxs-lookup"><span data-stu-id="28d18-212">OUTPUTS</span></span>

### <span data-ttu-id="28d18-213">Microsoft. Azure. PolicyInsights. \* 정책 이벤트</span><span class="sxs-lookup"><span data-stu-id="28d18-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="28d18-214">상속자</span><span class="sxs-lookup"><span data-stu-id="28d18-214">NOTES</span></span>

## <span data-ttu-id="28d18-215">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28d18-215">RELATED LINKS</span></span>