---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 2719f875d4a21f47b05b55b7880e4654237baafd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204952"
---
# <span data-ttu-id="967ac-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="967ac-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="967ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="967ac-102">SYNOPSIS</span></span>
<span data-ttu-id="967ac-103">주어진 시간 창에서 이 구독에 의해 만들어진 API 요청을 표시하는 로그를 내보내서 스로틀링 활동을 보여 집니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="967ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="967ac-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="967ac-105">설명</span><span class="sxs-lookup"><span data-stu-id="967ac-105">DESCRIPTION</span></span>
<span data-ttu-id="967ac-106">미리 정의한 시간 간격으로 구독의 호출에 대한 통계 데이터를 성공, 실패 또는 스로틀된 상태에 따라 Microsoft.Compute API로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="967ac-107">로그는 GroupByOperationName, GroupByThrottlePolicy 또는 GroupByResourceName의 세 매개 변수로 추가로 그룹화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="967ac-108">이 cmdlet은 Compute 리소스 공급자 로그만 수집합니다. 또한 디스크 및 스냅숏 리소스 종류에 대한 데이터는 아직 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="967ac-109">Compute 리소스 공급자의 API 제한에 대한 개요는 https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="967ac-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="967ac-110">예제</span><span class="sxs-lookup"><span data-stu-id="967ac-110">EXAMPLES</span></span>

### <span data-ttu-id="967ac-111">예제 1: 작업 이름으로 집계된 레코드 내보내기</span><span class="sxs-lookup"><span data-stu-id="967ac-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="967ac-112">이 명령은 2018-02-20T17:54:14와 2018-02-22T17:54:17 사이의 성공, 실패 또는 스로틀로 구분된 Microsoft.Compute API 호출의 집계된 숫자를 작업 이름으로 집계된 주어진 SAS URI에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="967ac-113">예제 2: 애플리케이션 ID로 집계된 레코드 내보내기</span><span class="sxs-lookup"><span data-stu-id="967ac-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId
```

<span data-ttu-id="967ac-114">이 명령은 2018-02-20T17:54:14와 2018-02-22T17:54:17 사이의 성공, 실패 또는 스로틀로 구분된 Microsoft.Compute API 호출의 집계된 수를 애플리케이션 ID별로 집계된 주어진 SAS URI에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="967ac-115">예제 3: 사용자 에이전트에 의해 집계된 레코드 내보내기</span><span class="sxs-lookup"><span data-stu-id="967ac-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
```

<span data-ttu-id="967ac-116">이 명령은 사용자 에이전트별로 집계된 주어진 SAS URI에 2018-02-20T17:54:14와 2018-02-22T17:54:17 사이에 성공, 실패 또는 스로틀로 구분된 Microsoft.Compute API 호출의 집계된 번호를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="967ac-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="967ac-117">PARAMETERS</span></span>

### <span data-ttu-id="967ac-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="967ac-118">-AsJob</span></span>
<span data-ttu-id="967ac-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="967ac-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="967ac-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="967ac-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="967ac-121">LogAnalytics Api가 출력 로그를 기록하는 로깅 Blob 컨테이너의 SAS URI입니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="967ac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="967ac-122">-DefaultProfile</span></span>
<span data-ttu-id="967ac-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="967ac-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="967ac-124">-FromTime</span></span>
<span data-ttu-id="967ac-125">쿼리 시간부터</span><span class="sxs-lookup"><span data-stu-id="967ac-125">From time of the query</span></span>

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

### <span data-ttu-id="967ac-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="967ac-126">-GroupByApplicationId</span></span>
<span data-ttu-id="967ac-127">애플리케이션 ID로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="967ac-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="967ac-128">-GroupByOperationName</span></span>
<span data-ttu-id="967ac-129">작업 이름으로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="967ac-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="967ac-130">-GroupByResourceName</span></span>
<span data-ttu-id="967ac-131">리소스 이름으로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="967ac-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="967ac-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="967ac-133">적용된 제한 정책에 따라 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="967ac-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="967ac-134">-GroupByUserAgent</span></span>
<span data-ttu-id="967ac-135">UserAgent로 쿼리 결과를 그룹화합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="967ac-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="967ac-136">-IntervalLength</span></span>
<span data-ttu-id="967ac-137">LogAnalytics 호출 속도 로그를 만드는 데 사용되는 간격 값(분)입니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="967ac-138">-Location</span><span class="sxs-lookup"><span data-stu-id="967ac-138">-Location</span></span>
<span data-ttu-id="967ac-139">로그 분석이 검색되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-139">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="967ac-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="967ac-140">-NoWait</span></span>
<span data-ttu-id="967ac-141">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="967ac-142">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="967ac-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="967ac-143">-ToTime</span></span>
<span data-ttu-id="967ac-144">쿼리 시간</span><span class="sxs-lookup"><span data-stu-id="967ac-144">To time of the query</span></span>

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

### <span data-ttu-id="967ac-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="967ac-145">-Confirm</span></span>
<span data-ttu-id="967ac-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="967ac-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="967ac-147">-WhatIf</span></span>
<span data-ttu-id="967ac-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="967ac-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="967ac-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="967ac-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967ac-150">CommonParameters</span></span>
<span data-ttu-id="967ac-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="967ac-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="967ac-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="967ac-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967ac-153">입력</span><span class="sxs-lookup"><span data-stu-id="967ac-153">INPUTS</span></span>

### <span data-ttu-id="967ac-154">System.String</span><span class="sxs-lookup"><span data-stu-id="967ac-154">System.String</span></span>

## <span data-ttu-id="967ac-155">출력</span><span class="sxs-lookup"><span data-stu-id="967ac-155">OUTPUTS</span></span>

### <span data-ttu-id="967ac-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="967ac-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="967ac-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="967ac-157">NOTES</span></span>

## <span data-ttu-id="967ac-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="967ac-158">RELATED LINKS</span></span>
