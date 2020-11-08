---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214715"
---
# <span data-ttu-id="24886-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="24886-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="24886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24886-102">SYNOPSIS</span></span>
<span data-ttu-id="24886-103">리소스에 대 한 최신 정책 준수 상태 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="24886-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24886-104">SYNTAX</span></span>

### <span data-ttu-id="24886-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="24886-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24886-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="24886-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24886-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="24886-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24886-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="24886-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24886-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="24886-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24886-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="24886-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24886-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="24886-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24886-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="24886-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24886-113">설명은</span><span class="sxs-lookup"><span data-stu-id="24886-113">DESCRIPTION</span></span>
<span data-ttu-id="24886-114">다양 한 범위의 최신 정책 준수 상태 번호에 대 한 요약 뷰를 가져와 정책 할당 및 정책 정의로 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="24886-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="24886-115">호환 되지 않는 정책 상태만 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="24886-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="24886-116">예제의</span><span class="sxs-lookup"><span data-stu-id="24886-116">EXAMPLES</span></span>

### <span data-ttu-id="24886-117">예제 1: 현재 구독 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="24886-118">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="24886-119">예제 2: 지정 된 구독 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="24886-120">지정 된 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="24886-121">예제 3: 관리 그룹 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="24886-122">지정 된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="24886-123">예제 4: 현재 구독의 리소스 그룹 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="24886-124">지정 된 리소스 그룹 (현재 세션 컨텍스트의 구독) 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="24886-125">예제 5: 지정 된 구독의 리소스 그룹 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="24886-126">지정 된 리소스 그룹 (지정 된 구독) 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="24886-127">예제 6: 리소스에 대 한 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="24886-128">지정 된 리소스의 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="24886-129">예제 7: 현재 구독의 정책 집합 정의에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="24886-130">현재 세션 컨텍스트의 구독에 있는 지정 된 정책 집합 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="24886-131">예제 8: 지정 된 구독에서 정책 집합 정의에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="24886-132">지정 된 정책 집합 정의 (현재 세션 컨텍스트의 테 넌 트 내)의 모든 리소스에 대해 마지막 날에 생성 된 최근 정책 준수 상태의 요약 뷰를 가져옵니다 (지정한 구독에 존재 함).</span><span class="sxs-lookup"><span data-stu-id="24886-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="24886-133">예제 9: 현재 구독의 정책 정의에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="24886-134">현재 세션 컨텍스트의 구독에 있는 지정 된 정책 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="24886-135">예제 10: 지정 된 구독에서 정책 정의에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="24886-136">지정 된 정책 정의 (지정 된 구독에 존재 함)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="24886-137">예제 11: 현재 구독에서 정책 할당에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="24886-138">지정 된 정책 할당 (현재 세션 컨텍스트의 구독에 있음)에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="24886-139">예 12: 지정 된 구독에서 정책 할당에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="24886-140">지정 된 정책 할당 (지정 된 구독에 있음)에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="24886-141">예제 13: 현재 구독에서 지정 된 리소스 그룹의 정책 할당에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="24886-142">지정 된 정책 할당 (현재 세션 컨텍스트에서 구독에 있는 리소스 그룹에 있음)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="24886-143">예 14: 현재 구독 범위에서 상위 쿼리 옵션을 사용 하 여 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="24886-144">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="24886-145">이 명령은 정책 할당 요약을 비규격 리소스 수를 기준으로 내림차순으로 정렬 하 고 해당 정책 할당 요약을 최상위 5 개만 차지 합니다.</span><span class="sxs-lookup"><span data-stu-id="24886-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="24886-146">예 15: From 및 To 쿼리 옵션을 사용 하 여 현재 구독 범위에서 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="24886-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="24886-147">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정 된 날짜 범위 내에서 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="24886-148">예제 16: 현재 구독 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기, 필터 쿼리 옵션 사용</span><span class="sxs-lookup"><span data-stu-id="24886-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="24886-149">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24886-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="24886-150">이 명령은 정책 정의 작업 (거부 또는 감사 작업 포함) 및 리소스 위치 (e\ us 위치 제외)에 따라 필터링 하 여 반환 되는 결과를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="24886-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="24886-151">변수</span><span class="sxs-lookup"><span data-stu-id="24886-151">PARAMETERS</span></span>

### <span data-ttu-id="24886-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24886-152">-DefaultProfile</span></span>
<span data-ttu-id="24886-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24886-154">-필터</span><span class="sxs-lookup"><span data-stu-id="24886-154">-Filter</span></span>
<span data-ttu-id="24886-155">OData 표시법을 사용 하 여 식을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="24886-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="24886-156">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="24886-156">-From</span></span>
<span data-ttu-id="24886-157">쿼리 간격의 시작 시간을 지정 하는 ISO 8601 형식이 지정 된 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="24886-158">지정 하지 않으면 기본적으로 ' To ' 매개 변수 값은 1 일을 뺀 수입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="24886-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="24886-159">-ManagementGroupName</span></span>
<span data-ttu-id="24886-160">관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-160">Management group name.</span></span>

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

### <span data-ttu-id="24886-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="24886-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="24886-162">정책 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="24886-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="24886-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="24886-164">정책 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-164">Policy definition name.</span></span>

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

### <span data-ttu-id="24886-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="24886-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="24886-166">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="24886-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24886-167">-ResourceGroupName</span></span>
<span data-ttu-id="24886-168">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-168">Resource group name.</span></span>

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

### <span data-ttu-id="24886-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24886-169">-ResourceId</span></span>
<span data-ttu-id="24886-170">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-170">Resource ID.</span></span>

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

### <span data-ttu-id="24886-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24886-171">-SubscriptionId</span></span>
<span data-ttu-id="24886-172">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-172">Subscription ID.</span></span>

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

### <span data-ttu-id="24886-173">-To</span><span class="sxs-lookup"><span data-stu-id="24886-173">-To</span></span>
<span data-ttu-id="24886-174">쿼리 간격의 종료 시간을 지정 하는 ISO 8601 형식이 지정 된 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="24886-175">지정 하지 않으면 기본적으로 요청 시간이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="24886-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="24886-176">-위쪽</span><span class="sxs-lookup"><span data-stu-id="24886-176">-Top</span></span>
<span data-ttu-id="24886-177">반환할 레코드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="24886-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="24886-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24886-178">CommonParameters</span></span>
<span data-ttu-id="24886-179">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24886-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24886-180">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="24886-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24886-181">입력</span><span class="sxs-lookup"><span data-stu-id="24886-181">INPUTS</span></span>

### <span data-ttu-id="24886-182">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24886-182">System.String</span></span>

## <span data-ttu-id="24886-183">출력</span><span class="sxs-lookup"><span data-stu-id="24886-183">OUTPUTS</span></span>

### <span data-ttu-id="24886-184">PolicyStateSummary-PolicyInsights. 모델.</span><span class="sxs-lookup"><span data-stu-id="24886-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="24886-185">상속자</span><span class="sxs-lookup"><span data-stu-id="24886-185">NOTES</span></span>

## <span data-ttu-id="24886-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24886-186">RELATED LINKS</span></span>

[<span data-ttu-id="24886-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="24886-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
