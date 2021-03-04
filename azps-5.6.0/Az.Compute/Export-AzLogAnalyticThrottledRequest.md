---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 02d78a36bcd2afc6eef037a0b043c5db89d37f0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969403"
---
# <span data-ttu-id="5fd55-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5fd55-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="5fd55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fd55-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd55-103">주어진 시간 창에서 이 구독에 대한 총 스로틀된 Api 요청을 표시하는 로그를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="5fd55-104">구문</span><span class="sxs-lookup"><span data-stu-id="5fd55-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fd55-105">설명</span><span class="sxs-lookup"><span data-stu-id="5fd55-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd55-106">이렇게 하여 Microsoft.Compute API 호출의 총 수를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="5fd55-107">로그는 GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent 또는 GroupByApplicationId의 5개 옵션으로 추가로 집계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-107">The logs can be further aggregated by five options: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="5fd55-108">이 cmdlet은 CRP 로그만 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="5fd55-109">컴퓨팅 리소스 공급자의 API 제한에 대한 개요는 https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5fd55-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="5fd55-110">예제</span><span class="sxs-lookup"><span data-stu-id="5fd55-110">EXAMPLES</span></span>

### <span data-ttu-id="5fd55-111">예제 1: 작업 이름으로 집계된 레코드 내보내기</span><span class="sxs-lookup"><span data-stu-id="5fd55-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="5fd55-112">이 명령은 2018-02-20T17:54:14와 2018-02-22T17:54:17 사이의 총 Microsoft.Compute API 호출을 작업 이름으로 집계합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="5fd55-113">예제 2: 애플리케이션 ID로 집계된 레코드 내보내기</span><span class="sxs-lookup"><span data-stu-id="5fd55-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="5fd55-114">이 명령은 2018-02-20T17:54:14와 2018-02-22T17:54:17 사이의 총 Microsoft.Compute API 호출을 적용 ID로 집계합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="5fd55-115">예제 3: 사용자 에이전트에 의해 집계된 레코드 내보내기</span><span class="sxs-lookup"><span data-stu-id="5fd55-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="5fd55-116">이 명령은 사용자 에이전트에 의해 집계된 주어진 SAS URI에 2018-02-20T17:54:14 및 2018-02-22T17:54:17 사이의 총 스로틀된 Microsoft.Compute API 호출을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="5fd55-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5fd55-117">PARAMETERS</span></span>

### <span data-ttu-id="5fd55-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fd55-118">-AsJob</span></span>
<span data-ttu-id="5fd55-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5fd55-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fd55-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="5fd55-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="5fd55-121">LogAnalytics Api가 출력 로그를 기록하는 로깅 Blob 컨테이너의 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd55-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd55-122">-DefaultProfile</span></span>
<span data-ttu-id="5fd55-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fd55-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="5fd55-124">-FromTime</span></span>
<span data-ttu-id="5fd55-125">쿼리의 시간부터</span><span class="sxs-lookup"><span data-stu-id="5fd55-125">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd55-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="5fd55-126">-GroupByApplicationId</span></span>
<span data-ttu-id="5fd55-127">애플리케이션 ID로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="5fd55-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="5fd55-128">-GroupByOperationName</span></span>
<span data-ttu-id="5fd55-129">작업 이름에 따라 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="5fd55-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="5fd55-130">-GroupByResourceName</span></span>
<span data-ttu-id="5fd55-131">리소스 이름으로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="5fd55-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="5fd55-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="5fd55-133">스로틀 정책에 따라 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="5fd55-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="5fd55-134">-GroupByUserAgent</span></span>
<span data-ttu-id="5fd55-135">UserAgent로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="5fd55-136">-Location</span><span class="sxs-lookup"><span data-stu-id="5fd55-136">-Location</span></span>
<span data-ttu-id="5fd55-137">로그 분석이 검색되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-137">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fd55-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5fd55-138">-NoWait</span></span>
<span data-ttu-id="5fd55-139">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5fd55-140">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5fd55-141">-ToTime</span><span class="sxs-lookup"><span data-stu-id="5fd55-141">-ToTime</span></span>
<span data-ttu-id="5fd55-142">쿼리 시간까지</span><span class="sxs-lookup"><span data-stu-id="5fd55-142">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fd55-143">-확인</span><span class="sxs-lookup"><span data-stu-id="5fd55-143">-Confirm</span></span>
<span data-ttu-id="5fd55-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd55-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd55-145">-WhatIf</span></span>
<span data-ttu-id="5fd55-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd55-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd55-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd55-148">CommonParameters</span></span>
<span data-ttu-id="5fd55-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5fd55-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd55-150">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fd55-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd55-151">입력</span><span class="sxs-lookup"><span data-stu-id="5fd55-151">INPUTS</span></span>

### <span data-ttu-id="5fd55-152">System.String</span><span class="sxs-lookup"><span data-stu-id="5fd55-152">System.String</span></span>

## <span data-ttu-id="5fd55-153">출력</span><span class="sxs-lookup"><span data-stu-id="5fd55-153">OUTPUTS</span></span>

### <span data-ttu-id="5fd55-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="5fd55-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="5fd55-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5fd55-155">NOTES</span></span>

## <span data-ttu-id="5fd55-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fd55-156">RELATED LINKS</span></span>
