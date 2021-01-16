---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330134"
---
# <span data-ttu-id="3151d-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="3151d-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="3151d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3151d-102">SYNOPSIS</span></span>
<span data-ttu-id="3151d-103">주어진 기간에 이 구독에 대한 총 스로틀된 API 요청을 표시하는 로그를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="3151d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3151d-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3151d-105">설명</span><span class="sxs-lookup"><span data-stu-id="3151d-105">DESCRIPTION</span></span>
<span data-ttu-id="3151d-106">이렇게 하여 스로틀된 Microsoft.Compute API 호출의 총 수를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="3151d-107">로그는 GroupByOperationName, GroupByThrottlePolicy 또는 GroupByResourceName의 세 가지 옵션으로 추가로 집계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="3151d-108">이 cmdlet은 CRP 로그만 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="3151d-109">Compute 리소스 공급자의 API 제한에 대한 개요는 https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3151d-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="3151d-110">예제</span><span class="sxs-lookup"><span data-stu-id="3151d-110">EXAMPLES</span></span>

### <span data-ttu-id="3151d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3151d-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="3151d-112">이 명령은 작업 이름으로 집계된 주어진 SAS URI에 2018-02-20T17:54:14와 2018-02-22T17:54:17 사이의 총 스로틀된 Microsoft.Compute API 호출을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="3151d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3151d-113">PARAMETERS</span></span>

### <span data-ttu-id="3151d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3151d-114">-AsJob</span></span>
<span data-ttu-id="3151d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3151d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3151d-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="3151d-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="3151d-117">LogAnalytics Api가 출력 로그를 기록하는 로깅 Blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="3151d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3151d-118">-DefaultProfile</span></span>
<span data-ttu-id="3151d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3151d-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="3151d-120">-FromTime</span></span>
<span data-ttu-id="3151d-121">쿼리 시간부터</span><span class="sxs-lookup"><span data-stu-id="3151d-121">From time of the query</span></span>

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

### <span data-ttu-id="3151d-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="3151d-122">-GroupByOperationName</span></span>
<span data-ttu-id="3151d-123">작업 이름으로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="3151d-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="3151d-124">-GroupByResourceName</span></span>
<span data-ttu-id="3151d-125">리소스 이름으로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="3151d-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="3151d-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="3151d-127">적용된 제한 정책에 따라 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="3151d-128">-Location</span><span class="sxs-lookup"><span data-stu-id="3151d-128">-Location</span></span>
<span data-ttu-id="3151d-129">로그 분석이 검색되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="3151d-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3151d-130">-NoWait</span></span>
<span data-ttu-id="3151d-131">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3151d-132">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3151d-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="3151d-133">-ToTime</span></span>
<span data-ttu-id="3151d-134">쿼리 시간</span><span class="sxs-lookup"><span data-stu-id="3151d-134">To time of the query</span></span>

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

### <span data-ttu-id="3151d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3151d-135">-Confirm</span></span>
<span data-ttu-id="3151d-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3151d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3151d-137">-WhatIf</span></span>
<span data-ttu-id="3151d-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3151d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3151d-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3151d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3151d-140">CommonParameters</span></span>
<span data-ttu-id="3151d-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3151d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3151d-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3151d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3151d-143">입력</span><span class="sxs-lookup"><span data-stu-id="3151d-143">INPUTS</span></span>

### <span data-ttu-id="3151d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3151d-144">System.String</span></span>

## <span data-ttu-id="3151d-145">출력</span><span class="sxs-lookup"><span data-stu-id="3151d-145">OUTPUTS</span></span>

### <span data-ttu-id="3151d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="3151d-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="3151d-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3151d-147">NOTES</span></span>

## <span data-ttu-id="3151d-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3151d-148">RELATED LINKS</span></span>
