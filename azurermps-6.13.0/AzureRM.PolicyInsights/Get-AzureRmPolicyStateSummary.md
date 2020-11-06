---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528462"
---
# <span data-ttu-id="745b3-101">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="745b3-101">Get-AzureRmPolicyStateSummary</span></span>

## <span data-ttu-id="745b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="745b3-102">SYNOPSIS</span></span>
<span data-ttu-id="745b3-103">리소스에 대 한 최신 정책 준수 상태 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-103">Gets latest policy compliance states summary for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="745b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="745b3-104">SYNTAX</span></span>

### <span data-ttu-id="745b3-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="745b3-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="745b3-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="745b3-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="745b3-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="745b3-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="745b3-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="745b3-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="745b3-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="745b3-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="745b3-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="745b3-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="745b3-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="745b3-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="745b3-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="745b3-112">ResourceScope</span></span>
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="745b3-113">설명은</span><span class="sxs-lookup"><span data-stu-id="745b3-113">DESCRIPTION</span></span>
<span data-ttu-id="745b3-114">다양 한 범위의 최신 정책 준수 상태 번호에 대 한 요약 뷰를 가져와 정책 할당 및 정책 정의로 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="745b3-115">호환 되지 않는 정책 상태만 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="745b3-116">예제의</span><span class="sxs-lookup"><span data-stu-id="745b3-116">EXAMPLES</span></span>

### <span data-ttu-id="745b3-117">예제 1: 현재 구독 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

<span data-ttu-id="745b3-118">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="745b3-119">예제 2: 지정 된 구독 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="745b3-120">지정 된 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="745b3-121">예제 3: 관리 그룹 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="745b3-122">지정 된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="745b3-123">예제 4: 현재 구독의 리소스 그룹 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="745b3-124">지정 된 리소스 그룹 (현재 세션 컨텍스트의 구독) 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="745b3-125">예제 5: 지정 된 구독의 리소스 그룹 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="745b3-126">지정 된 리소스 그룹 (지정 된 구독) 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="745b3-127">예제 6: 리소스에 대 한 호환 되지 않는 최신 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="745b3-128">지정 된 리소스의 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="745b3-129">예제 7: 현재 구독의 정책 집합 정의에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="745b3-130">현재 세션 컨텍스트의 구독에 있는 지정 된 정책 집합 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="745b3-131">예제 8: 지정 된 구독에서 정책 집합 정의에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="745b3-132">지정 된 정책 집합 정의 (현재 세션 컨텍스트의 테 넌 트 내)의 모든 리소스에 대해 마지막 날에 생성 된 최근 정책 준수 상태의 요약 뷰를 가져옵니다 (지정한 구독에 존재 함).</span><span class="sxs-lookup"><span data-stu-id="745b3-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="745b3-133">예제 9: 현재 구독의 정책 정의에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="745b3-134">현재 세션 컨텍스트의 구독에 있는 지정 된 정책 정의에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="745b3-135">예제 10: 지정 된 구독에서 정책 정의에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="745b3-136">지정 된 정책 정의 (지정 된 구독에 존재 함)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="745b3-137">예제 11: 현재 구독에서 정책 할당에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="745b3-138">지정 된 정책 할당 (현재 세션 컨텍스트의 구독에 있음)에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="745b3-139">예 12: 지정 된 구독에서 정책 할당에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="745b3-140">지정 된 정책 할당 (지정 된 구독에 있음)에 의해 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="745b3-141">예제 13: 현재 구독에서 지정 된 리소스 그룹의 정책 할당에 대 한 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="745b3-142">지정 된 정책 할당 (현재 세션 컨텍스트에서 구독에 있는 리소스 그룹에 있음)의 영향을 받는 모든 리소스 (현재 세션 컨텍스트의 테 넌 트 내)에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="745b3-143">예 14: 현재 구독 범위에서 상위 쿼리 옵션을 사용 하 여 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

<span data-ttu-id="745b3-144">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="745b3-145">이 명령은 정책 할당 요약을 비규격 리소스 수를 기준으로 내림차순으로 정렬 하 고 해당 정책 할당 요약을 최상위 5 개만 차지 합니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="745b3-146">예 15: From 및 To 쿼리 옵션을 사용 하 여 현재 구독 범위에서 최신 비규격 정책 상태 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="745b3-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="745b3-147">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정 된 날짜 범위 내에서 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="745b3-148">예제 16: 현재 구독 범위에서 호환 되지 않는 최신 정책 상태 요약 가져오기, 필터 쿼리 옵션 사용</span><span class="sxs-lookup"><span data-stu-id="745b3-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="745b3-149">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성 된 최신 정책 준수 상태의 요약 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="745b3-150">이 명령은 정책 정의 작업 (거부 또는 감사 작업 포함) 및 리소스 위치 (e\ us 위치 제외)에 따라 필터링 하 여 반환 되는 결과를 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="745b3-151">변수</span><span class="sxs-lookup"><span data-stu-id="745b3-151">PARAMETERS</span></span>

### <span data-ttu-id="745b3-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745b3-152">-DefaultProfile</span></span>
<span data-ttu-id="745b3-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="745b3-154">-필터</span><span class="sxs-lookup"><span data-stu-id="745b3-154">-Filter</span></span>
<span data-ttu-id="745b3-155">OData 표시법을 사용 하 여 식을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="745b3-156">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="745b3-156">-From</span></span>
<span data-ttu-id="745b3-157">쿼리 간격의 시작 시간을 지정 하는 ISO 8601 형식이 지정 된 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="745b3-158">지정 하지 않으면 기본적으로 ' To ' 매개 변수 값은 1 일을 뺀 수입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="745b3-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="745b3-159">-ManagementGroupName</span></span>
<span data-ttu-id="745b3-160">관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-160">Management group name.</span></span>

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

### <span data-ttu-id="745b3-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="745b3-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="745b3-162">정책 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="745b3-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="745b3-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="745b3-164">정책 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-164">Policy definition name.</span></span>

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

### <span data-ttu-id="745b3-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="745b3-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="745b3-166">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="745b3-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="745b3-167">-ResourceGroupName</span></span>
<span data-ttu-id="745b3-168">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-168">Resource group name.</span></span>

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

### <span data-ttu-id="745b3-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="745b3-169">-ResourceId</span></span>
<span data-ttu-id="745b3-170">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-170">Resource ID.</span></span>

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

### <span data-ttu-id="745b3-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="745b3-171">-SubscriptionId</span></span>
<span data-ttu-id="745b3-172">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-172">Subscription ID.</span></span>

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

### <span data-ttu-id="745b3-173">-To</span><span class="sxs-lookup"><span data-stu-id="745b3-173">-To</span></span>
<span data-ttu-id="745b3-174">쿼리 간격의 종료 시간을 지정 하는 ISO 8601 형식이 지정 된 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="745b3-175">지정 하지 않으면 기본적으로 요청 시간이 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="745b3-176">-위쪽</span><span class="sxs-lookup"><span data-stu-id="745b3-176">-Top</span></span>
<span data-ttu-id="745b3-177">반환할 레코드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="745b3-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745b3-178">CommonParameters</span></span>
<span data-ttu-id="745b3-179">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="745b3-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745b3-180">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="745b3-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745b3-181">입력</span><span class="sxs-lookup"><span data-stu-id="745b3-181">INPUTS</span></span>

### <span data-ttu-id="745b3-182">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="745b3-182">System.String</span></span>

## <span data-ttu-id="745b3-183">출력</span><span class="sxs-lookup"><span data-stu-id="745b3-183">OUTPUTS</span></span>

### <span data-ttu-id="745b3-184">PolicyStateSummary-PolicyInsights. 모델.</span><span class="sxs-lookup"><span data-stu-id="745b3-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="745b3-185">상속자</span><span class="sxs-lookup"><span data-stu-id="745b3-185">NOTES</span></span>

## <span data-ttu-id="745b3-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="745b3-186">RELATED LINKS</span></span>

[<span data-ttu-id="745b3-187">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="745b3-187">Get-AzureRmPolicyState</span></span>](./Get-AzureRmPolicyState.md)
