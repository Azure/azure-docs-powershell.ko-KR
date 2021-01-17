---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 90b467ccd046bf7d08b9faff4c03dcc858ae0076
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364155"
---
# <span data-ttu-id="57353-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="57353-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="57353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57353-102">SYNOPSIS</span></span>
<span data-ttu-id="57353-103">주어진 시간 창에서 이 구독에 의해 만들어진 API 요청을 표시하는 로그를 내보내서 스로틀링 활동을 보여 집니다.</span><span class="sxs-lookup"><span data-stu-id="57353-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="57353-104">구문</span><span class="sxs-lookup"><span data-stu-id="57353-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57353-105">설명</span><span class="sxs-lookup"><span data-stu-id="57353-105">DESCRIPTION</span></span>
<span data-ttu-id="57353-106">미리 정의한 시간 간격으로 성공, 실패 또는 스로틀된 상태에 따라 구독의 호출에 대한 통계 데이터를 Microsoft.Compute API로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57353-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="57353-107">로그는 GroupByOperationName, GroupByThrottlePolicy 또는 GroupByResourceName의 세 매개 변수로 추가로 그룹화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57353-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="57353-108">이 cmdlet은 Compute 리소스 공급자 로그만 수집합니다. 또한 디스크 및 스냅숏 리소스 종류에 대한 데이터는 아직 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="57353-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="57353-109">Compute 리소스 공급자의 API 제한에 대한 개요는 https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="57353-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="57353-110">예제</span><span class="sxs-lookup"><span data-stu-id="57353-110">EXAMPLES</span></span>

### <span data-ttu-id="57353-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="57353-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="57353-112">이 명령은 2018-02-20T17:54:14와 2018-02-22T17:54:17 사이의 성공, 실패 또는 스로틀로 구분된 Microsoft.Compute API 호출의 집계된 숫자를 작업 이름으로 집계된 주어진 SAS URI에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="57353-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="57353-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57353-113">PARAMETERS</span></span>

### <span data-ttu-id="57353-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57353-114">-AsJob</span></span>
<span data-ttu-id="57353-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="57353-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57353-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="57353-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="57353-117">LogAnalytics Api가 출력 로그를 기록하는 로깅 Blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="57353-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="57353-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57353-118">-DefaultProfile</span></span>
<span data-ttu-id="57353-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57353-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57353-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="57353-120">-FromTime</span></span>
<span data-ttu-id="57353-121">쿼리 시간부터</span><span class="sxs-lookup"><span data-stu-id="57353-121">From time of the query</span></span>

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

### <span data-ttu-id="57353-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="57353-122">-GroupByOperationName</span></span>
<span data-ttu-id="57353-123">작업 이름으로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="57353-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="57353-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="57353-124">-GroupByResourceName</span></span>
<span data-ttu-id="57353-125">리소스 이름으로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="57353-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="57353-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="57353-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="57353-127">적용된 제한 정책에 따라 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="57353-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="57353-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="57353-128">-IntervalLength</span></span>
<span data-ttu-id="57353-129">LogAnalytics 호출 속도 로그를 만드는 데 사용되는 간격 값(분)입니다.</span><span class="sxs-lookup"><span data-stu-id="57353-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57353-130">-Location</span><span class="sxs-lookup"><span data-stu-id="57353-130">-Location</span></span>
<span data-ttu-id="57353-131">로그 분석이 검색되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="57353-131">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="57353-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="57353-132">-NoWait</span></span>
<span data-ttu-id="57353-133">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="57353-133">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="57353-134">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57353-134">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="57353-135">-ToTime</span><span class="sxs-lookup"><span data-stu-id="57353-135">-ToTime</span></span>
<span data-ttu-id="57353-136">쿼리 시간</span><span class="sxs-lookup"><span data-stu-id="57353-136">To time of the query</span></span>

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

### <span data-ttu-id="57353-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57353-137">-Confirm</span></span>
<span data-ttu-id="57353-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57353-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57353-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57353-139">-WhatIf</span></span>
<span data-ttu-id="57353-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57353-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57353-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57353-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57353-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57353-142">CommonParameters</span></span>
<span data-ttu-id="57353-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57353-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57353-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57353-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57353-145">입력</span><span class="sxs-lookup"><span data-stu-id="57353-145">INPUTS</span></span>

### <span data-ttu-id="57353-146">System.String</span><span class="sxs-lookup"><span data-stu-id="57353-146">System.String</span></span>

## <span data-ttu-id="57353-147">출력</span><span class="sxs-lookup"><span data-stu-id="57353-147">OUTPUTS</span></span>

### <span data-ttu-id="57353-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="57353-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="57353-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57353-149">NOTES</span></span>

## <span data-ttu-id="57353-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57353-150">RELATED LINKS</span></span>
