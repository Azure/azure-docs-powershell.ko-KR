---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206264"
---
# <span data-ttu-id="1e792-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="1e792-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="1e792-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e792-102">SYNOPSIS</span></span>
<span data-ttu-id="1e792-103">리소스에 대한 최신 정책 준수 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="1e792-104">구문</span><span class="sxs-lookup"><span data-stu-id="1e792-104">SYNTAX</span></span>

### <span data-ttu-id="1e792-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="1e792-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e792-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="1e792-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e792-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="1e792-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e792-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="1e792-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e792-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="1e792-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e792-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="1e792-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e792-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="1e792-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e792-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="1e792-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e792-113">설명</span><span class="sxs-lookup"><span data-stu-id="1e792-113">DESCRIPTION</span></span>
<span data-ttu-id="1e792-114">정책 할당 및 정책 정의로 세분화하여 다양한 범위에서 최신 정책 준수 상태 번호의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="1e792-115">비준수 정책 상태만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="1e792-116">예제</span><span class="sxs-lookup"><span data-stu-id="1e792-116">EXAMPLES</span></span>

### <span data-ttu-id="1e792-117">예제 1: 현재 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="1e792-118">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="1e792-119">예제 2: 지정된 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="1e792-120">지정된 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="1e792-121">예제 3: 관리 그룹 범위에서 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="1e792-122">지정된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="1e792-123">예제 4: 현재 구독의 리소스 그룹 범위에서 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="1e792-124">지정된 리소스 그룹 내의 모든 리소스(현재 세션 컨텍스트의 구독에서)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="1e792-125">예제 5: 지정된 구독의 리소스 그룹 범위에서 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="1e792-126">지정된 리소스 그룹 내의 모든 리소스(지정된 구독에서)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="1e792-127">예제 6: 리소스에 대한 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="1e792-128">지정된 리소스에 대한 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="1e792-129">예제 7: 현재 구독의 정책 집합 정의에 대한 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="1e792-130">지정된 정책 집합 정의(현재 세션 컨텍스트의 구독에 있는)에 영향을 준 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="1e792-131">예제 8: 지정된 구독에서 정책 집합 정의에 대한 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="1e792-132">지정된 정책 집합 정의(지정된 구독에 존재하는)에 의해 영향을 준 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="1e792-133">예제 9: 현재 구독의 정책 정의에 대한 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="1e792-134">지정된 정책 정의(현재 세션 컨텍스트의 구독에 있는)에 영향을 준 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="1e792-135">예제 10: 지정된 구독의 정책 정의에 대한 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="1e792-136">지정된 정책 정의(지정된 구독에 존재하는)에 의해 영향을 준 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="1e792-137">예제 11: 현재 구독의 정책 할당에 대한 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="1e792-138">지정된 정책 할당(현재 세션 컨텍스트의 구독에 있는)에 영향을 준 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="1e792-139">예제 12: 지정된 구독에서 정책 할당에 대한 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="1e792-140">지정된 정책 할당(지정된 구독에 있는)의 영향을 을(를) 적용하는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="1e792-141">예제 13: 현재 구독의 지정된 리소스 그룹에 있는 정책 할당에 대한 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="1e792-142">지정된 정책 할당(현재 세션 컨텍스트의 구독에 있는 리소스 그룹에 있는 리소스 그룹에 있는)의 영향을 준 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="1e792-143">예제 14: 상위 쿼리 옵션을 사용하여 현재 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="1e792-144">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="1e792-145">이 명령은 비준수 리소스 수를 내선 순서로 정책 할당 요약을 결과에 순서대로 지정하고 해당 정책 할당 요약 중 상위 5개만 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="1e792-146">예제 15: From 및 To 쿼리 옵션을 사용하여 현재 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="1e792-147">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정된 날짜 범위 내에서 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="1e792-148">예제 16: 필터 쿼리 옵션을 사용하여 현재 구독 범위에서 최신 비준수 정책 상태 요약을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="1e792-149">현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 마지막 날에 생성된 최신 정책 준수 상태의 요약 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="1e792-150">이 명령은 정책 정의 작업(거부 또는 감사 작업 포함) 및 리소스 위치(eastus 위치 제외)에 따라 필터링하여 반환되는 결과를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="1e792-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e792-151">PARAMETERS</span></span>

### <span data-ttu-id="1e792-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e792-152">-DefaultProfile</span></span>
<span data-ttu-id="1e792-153">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e792-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="1e792-154">-Filter</span></span>
<span data-ttu-id="1e792-155">OData 표기 방법을 사용하여 식 필터링</span><span class="sxs-lookup"><span data-stu-id="1e792-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="1e792-156">-From</span><span class="sxs-lookup"><span data-stu-id="1e792-156">-From</span></span>
<span data-ttu-id="1e792-157">쿼리할 간격의 시작 시간을 지정하는 ISO 8601 형식의 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="1e792-158">지정하지 않으면 기본값은 'To' 매개 변수 값에서 1일을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="1e792-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1e792-159">-ManagementGroupName</span></span>
<span data-ttu-id="1e792-160">관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-160">Management group name.</span></span>

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

### <span data-ttu-id="1e792-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="1e792-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="1e792-162">정책 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="1e792-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="1e792-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="1e792-164">정책 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-164">Policy definition name.</span></span>

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

### <span data-ttu-id="1e792-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="1e792-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="1e792-166">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="1e792-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e792-167">-ResourceGroupName</span></span>
<span data-ttu-id="1e792-168">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-168">Resource group name.</span></span>

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

### <span data-ttu-id="1e792-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e792-169">-ResourceId</span></span>
<span data-ttu-id="1e792-170">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-170">Resource ID.</span></span>

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

### <span data-ttu-id="1e792-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e792-171">-SubscriptionId</span></span>
<span data-ttu-id="1e792-172">구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-172">Subscription ID.</span></span>

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

### <span data-ttu-id="1e792-173">-To</span><span class="sxs-lookup"><span data-stu-id="1e792-173">-To</span></span>
<span data-ttu-id="1e792-174">쿼리할 간격의 종료 시간을 지정하는 ISO 8601 형식의 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="1e792-175">지정하지 않으면 기본값은 요청 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="1e792-176">-Top</span><span class="sxs-lookup"><span data-stu-id="1e792-176">-Top</span></span>
<span data-ttu-id="1e792-177">반환할 최대 레코드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="1e792-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e792-178">CommonParameters</span></span>
<span data-ttu-id="1e792-179">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1e792-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e792-180">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e792-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e792-181">입력</span><span class="sxs-lookup"><span data-stu-id="1e792-181">INPUTS</span></span>

### <span data-ttu-id="1e792-182">System.String</span><span class="sxs-lookup"><span data-stu-id="1e792-182">System.String</span></span>

## <span data-ttu-id="1e792-183">출력</span><span class="sxs-lookup"><span data-stu-id="1e792-183">OUTPUTS</span></span>

### <span data-ttu-id="1e792-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="1e792-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="1e792-185">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1e792-185">NOTES</span></span>

## <span data-ttu-id="1e792-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e792-186">RELATED LINKS</span></span>

[<span data-ttu-id="1e792-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="1e792-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
