---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 90b467ccd046bf7d08b9faff4c03dcc858ae0076
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212885"
---
# <span data-ttu-id="9015a-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="9015a-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="9015a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9015a-102">SYNOPSIS</span></span>
<span data-ttu-id="9015a-103">지정 된 시간 창에이 구독에서 수행한 Api 요청을 표시 하는 로그를 내보내어 제한 작업을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="9015a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9015a-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9015a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9015a-105">DESCRIPTION</span></span>
<span data-ttu-id="9015a-106">미리 정의 된 시간 간격으로 성공, 실패 또는 제한 상태에 따라 Microsoft의 Compute API에 대 한 구독 호출에 대 한 통계 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="9015a-107">로그는 세 개의 매개 변수 (GroupByOperationName, GroupByThrottlePolicy 또는 Groupbyoperationname)로 그룹화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="9015a-108">이 cmdlet은 계산 리소스 공급자 로그만 수집 합니다. 또한 디스크 및 스냅샷 리소스 종류에 대 한 데이터를 아직 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="9015a-109">계산 리소스 공급자의 API 제한에 대 한 개요는를 참조 하세요 https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="9015a-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="9015a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9015a-110">EXAMPLES</span></span>

### <span data-ttu-id="9015a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9015a-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="9015a-112">이 명령은 작업 이름으로 집계 된 지정 된 SAS URI에서 2018-02-20T17:54:14, 2018 년 2 월-02-2T17:54:17 사이에 성공, 실패 또는 스로틀 됨에 따라 구분 되는 계산 API 호출을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="9015a-113">변수</span><span class="sxs-lookup"><span data-stu-id="9015a-113">PARAMETERS</span></span>

### <span data-ttu-id="9015a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9015a-114">-AsJob</span></span>
<span data-ttu-id="9015a-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9015a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9015a-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="9015a-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="9015a-117">LogAnalytics Api가 출력 로그를 기록 하는 로깅 blob 컨테이너의 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="9015a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9015a-118">-DefaultProfile</span></span>
<span data-ttu-id="9015a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9015a-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="9015a-120">-FromTime</span></span>
<span data-ttu-id="9015a-121">쿼리 시작 시간</span><span class="sxs-lookup"><span data-stu-id="9015a-121">From time of the query</span></span>

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

### <span data-ttu-id="9015a-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="9015a-122">-GroupByOperationName</span></span>
<span data-ttu-id="9015a-123">쿼리 결과를 작업 이름으로 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="9015a-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="9015a-124">-GroupByResourceName</span></span>
<span data-ttu-id="9015a-125">자원 이름에 따라 쿼리 결과를 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="9015a-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="9015a-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="9015a-127">적용 된 스로틀 정책에 따라 쿼리 결과를 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="9015a-128">-Intlength</span><span class="sxs-lookup"><span data-stu-id="9015a-128">-IntervalLength</span></span>
<span data-ttu-id="9015a-129">LogAnalytics 통화 요금 로그를 만드는 데 사용 되는 간격 값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="9015a-130">-위치</span><span class="sxs-lookup"><span data-stu-id="9015a-130">-Location</span></span>
<span data-ttu-id="9015a-131">로그 분석을 쿼리 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-131">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="9015a-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9015a-132">-NoWait</span></span>
<span data-ttu-id="9015a-133">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-133">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9015a-134">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-134">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9015a-135">-ToTime</span><span class="sxs-lookup"><span data-stu-id="9015a-135">-ToTime</span></span>
<span data-ttu-id="9015a-136">쿼리 시간</span><span class="sxs-lookup"><span data-stu-id="9015a-136">To time of the query</span></span>

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

### <span data-ttu-id="9015a-137">-확인</span><span class="sxs-lookup"><span data-stu-id="9015a-137">-Confirm</span></span>
<span data-ttu-id="9015a-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9015a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9015a-139">-WhatIf</span></span>
<span data-ttu-id="9015a-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9015a-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9015a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9015a-142">CommonParameters</span></span>
<span data-ttu-id="9015a-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9015a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9015a-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9015a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9015a-145">입력</span><span class="sxs-lookup"><span data-stu-id="9015a-145">INPUTS</span></span>

### <span data-ttu-id="9015a-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9015a-146">System.String</span></span>

## <span data-ttu-id="9015a-147">출력</span><span class="sxs-lookup"><span data-stu-id="9015a-147">OUTPUTS</span></span>

### <span data-ttu-id="9015a-148">PSLogAnalyticsOperationResult의. m a.</span><span class="sxs-lookup"><span data-stu-id="9015a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="9015a-149">상속자</span><span class="sxs-lookup"><span data-stu-id="9015a-149">NOTES</span></span>

## <span data-ttu-id="9015a-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9015a-150">RELATED LINKS</span></span>
