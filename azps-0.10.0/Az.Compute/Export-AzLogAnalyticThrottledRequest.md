---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-AzLogAnalyticThrottledRequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 45f0a75b07d0fae07092ffbe2b23f42cfa6d707a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877103"
---
# <span data-ttu-id="d3455-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d3455-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="d3455-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3455-102">SYNOPSIS</span></span>
<span data-ttu-id="d3455-103">지정 된 시간 창에이 구독에 대 한 총 제한 Api 요청을 표시 하는 로그를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="d3455-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3455-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3455-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3455-105">DESCRIPTION</span></span>
<span data-ttu-id="d3455-106">이렇게 하면 제한 API 호출의 총 수가 내보내집니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="d3455-107">GroupByOperationName, GroupByThrottlePolicy 또는 Groupbyoperationname 등 세 가지 옵션으로 로그를 집계할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="d3455-108">이 cmdlet은 CRP 로그만 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="d3455-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d3455-109">EXAMPLES</span></span>

### <span data-ttu-id="d3455-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3455-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="d3455-111">이 명령은 지정 된 SAS URI에서 작업 이름별로 집계 되는 2018-02-20T17a: 54:14 및 2018 년 2 월-02-2T17:54:17 사이의 총 스로틀 있는 Microsoft. 연산 API 호출을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="d3455-112">변수</span><span class="sxs-lookup"><span data-stu-id="d3455-112">PARAMETERS</span></span>

### <span data-ttu-id="d3455-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3455-113">-AsJob</span></span>
<span data-ttu-id="d3455-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d3455-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3455-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="d3455-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="d3455-116">LogAnalytics Api가 출력 로그를 기록 하는 로깅 blob 컨테이너의 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="d3455-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3455-117">-DefaultProfile</span></span>
<span data-ttu-id="d3455-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3455-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="d3455-119">-FromTime</span></span>
<span data-ttu-id="d3455-120">쿼리 시작 시간</span><span class="sxs-lookup"><span data-stu-id="d3455-120">From time of the query</span></span>

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

### <span data-ttu-id="d3455-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="d3455-121">-GroupByOperationName</span></span>
<span data-ttu-id="d3455-122">쿼리 결과를 작업 이름으로 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="d3455-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="d3455-123">-GroupByResourceName</span></span>
<span data-ttu-id="d3455-124">자원 이름에 따라 쿼리 결과를 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="d3455-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="d3455-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="d3455-126">적용 된 스로틀 정책에 따라 쿼리 결과를 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="d3455-127">-위치</span><span class="sxs-lookup"><span data-stu-id="d3455-127">-Location</span></span>
<span data-ttu-id="d3455-128">로그 분석을 쿼리 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="d3455-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="d3455-129">-ToTime</span></span>
<span data-ttu-id="d3455-130">쿼리 시간</span><span class="sxs-lookup"><span data-stu-id="d3455-130">To time of the query</span></span>

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

### <span data-ttu-id="d3455-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d3455-131">-Confirm</span></span>
<span data-ttu-id="d3455-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3455-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3455-133">-WhatIf</span></span>
<span data-ttu-id="d3455-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3455-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3455-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3455-136">CommonParameters</span></span>
<span data-ttu-id="d3455-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3455-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3455-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3455-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3455-139">입력</span><span class="sxs-lookup"><span data-stu-id="d3455-139">INPUTS</span></span>

### <span data-ttu-id="d3455-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3455-140">System.String</span></span>

## <span data-ttu-id="d3455-141">출력</span><span class="sxs-lookup"><span data-stu-id="d3455-141">OUTPUTS</span></span>

### <span data-ttu-id="d3455-142">PSLogAnalyticsOperationResult의. m a.</span><span class="sxs-lookup"><span data-stu-id="d3455-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="d3455-143">상속자</span><span class="sxs-lookup"><span data-stu-id="d3455-143">NOTES</span></span>

## <span data-ttu-id="d3455-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3455-144">RELATED LINKS</span></span>

