---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: bbf275b08421265130da898b670b46c95b15c34c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877102"
---
# <span data-ttu-id="0df1c-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="0df1c-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="0df1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df1c-102">SYNOPSIS</span></span>
<span data-ttu-id="0df1c-103">지정 된 시간 창에이 구독에서 수행한 Api 요청을 표시 하는 로그를 내보내어 제한 작업을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="0df1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0df1c-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval  [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins>
 [-GroupByOperationName] [-GroupByThrottlePolicy] [-GroupByResourceName] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0df1c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0df1c-105">DESCRIPTION</span></span>
<span data-ttu-id="0df1c-106">이렇게 하면 집계 된 수의 Microsoft. 연산, 실패 또는 시간 간격으로 표시 되는 제한 API 통화가 구분 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="0df1c-107">로그는 세 개의 매개 변수 (GroupByOperationName, GroupByThrottlePolicy 또는 Groupbyoperationname)로 그룹화 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="0df1c-108">이 cmdlet은 CRP 로그만 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="0df1c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0df1c-109">EXAMPLES</span></span>

### <span data-ttu-id="0df1c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0df1c-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="0df1c-111">이 명령은 작업 이름으로 집계 된 지정 된 SAS URI에서 2018-02-20T17:54:14, 2018 년 2 월-02-2T17:54:17 사이에 성공, 실패 또는 스로틀 됨에 따라 구분 되는 계산 API 호출을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="0df1c-112">변수</span><span class="sxs-lookup"><span data-stu-id="0df1c-112">PARAMETERS</span></span>

### <span data-ttu-id="0df1c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0df1c-113">-AsJob</span></span>
<span data-ttu-id="0df1c-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0df1c-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="0df1c-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="0df1c-116">LogAnalytics Api가 출력 로그를 기록 하는 로깅 blob 컨테이너의 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df1c-117">-DefaultProfile</span></span>
<span data-ttu-id="0df1c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="0df1c-119">-FromTime</span></span>
<span data-ttu-id="0df1c-120">쿼리 시작 시간</span><span class="sxs-lookup"><span data-stu-id="0df1c-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="0df1c-121">-GroupByOperationName</span></span>
<span data-ttu-id="0df1c-122">쿼리 결과를 작업 이름으로 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="0df1c-123">-GroupByResourceName</span></span>
<span data-ttu-id="0df1c-124">자원 이름에 따라 쿼리 결과를 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="0df1c-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="0df1c-126">적용 된 스로틀 정책에 따라 쿼리 결과를 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-127">-Intlength</span><span class="sxs-lookup"><span data-stu-id="0df1c-127">-IntervalLength</span></span>
<span data-ttu-id="0df1c-128">LogAnalytics 통화 요금 로그를 만드는 데 사용 되는 간격 값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases: 
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-129">-위치</span><span class="sxs-lookup"><span data-stu-id="0df1c-129">-Location</span></span>
<span data-ttu-id="0df1c-130">로그 분석을 쿼리 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="0df1c-131">-ToTime</span></span>
<span data-ttu-id="0df1c-132">쿼리 시간</span><span class="sxs-lookup"><span data-stu-id="0df1c-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-133">-확인</span><span class="sxs-lookup"><span data-stu-id="0df1c-133">-Confirm</span></span>
<span data-ttu-id="0df1c-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0df1c-135">-WhatIf</span></span>
<span data-ttu-id="0df1c-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0df1c-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df1c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df1c-138">CommonParameters</span></span>
<span data-ttu-id="0df1c-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df1c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df1c-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0df1c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df1c-141">입력</span><span class="sxs-lookup"><span data-stu-id="0df1c-141">INPUTS</span></span>

### <span data-ttu-id="0df1c-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0df1c-142">System.String</span></span>

## <span data-ttu-id="0df1c-143">출력</span><span class="sxs-lookup"><span data-stu-id="0df1c-143">OUTPUTS</span></span>

### <span data-ttu-id="0df1c-144">PSLogAnalyticsOperationResult의. m a.</span><span class="sxs-lookup"><span data-stu-id="0df1c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="0df1c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="0df1c-145">NOTES</span></span>

## <span data-ttu-id="0df1c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0df1c-146">RELATED LINKS</span></span>

