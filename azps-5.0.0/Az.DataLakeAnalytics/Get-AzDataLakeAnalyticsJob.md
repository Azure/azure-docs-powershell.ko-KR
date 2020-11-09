---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305846"
---
# <span data-ttu-id="a052c-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a052c-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="a052c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a052c-102">SYNOPSIS</span></span>
<span data-ttu-id="a052c-103">Data Lake Analytics 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="a052c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a052c-104">SYNTAX</span></span>

### <span data-ttu-id="a052c-105">GetAllInResourceGroupAndAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="a052c-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a052c-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="a052c-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a052c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a052c-107">DESCRIPTION</span></span>
<span data-ttu-id="a052c-108">**AzDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake 분석 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="a052c-109">작업을 지정 하지 않으면이 cmdlet은 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="a052c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a052c-110">EXAMPLES</span></span>

### <span data-ttu-id="a052c-111">예제 1: 지정 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="a052c-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="a052c-112">이 명령은 지정 된 ID의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="a052c-113">예제 2: 지난 주에 제출 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="a052c-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="a052c-114">이 명령은 지난 주에 제출 된 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="a052c-115">변수</span><span class="sxs-lookup"><span data-stu-id="a052c-115">PARAMETERS</span></span>

### <span data-ttu-id="a052c-116">-계정</span><span class="sxs-lookup"><span data-stu-id="a052c-116">-Account</span></span>
<span data-ttu-id="a052c-117">Data Lake Analytics 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a052c-118">-DefaultProfile</span></span>
<span data-ttu-id="a052c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a052c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a052c-120">-포함</span><span class="sxs-lookup"><span data-stu-id="a052c-120">-Include</span></span>
<span data-ttu-id="a052c-121">작업에 대해 검색할 추가 정보 유형을 나타내는 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="a052c-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a052c-123">않아야</span><span class="sxs-lookup"><span data-stu-id="a052c-123">None</span></span>
- <span data-ttu-id="a052c-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="a052c-124">DebugInfo</span></span>
- <span data-ttu-id="a052c-125">통계</span><span class="sxs-lookup"><span data-stu-id="a052c-125">Statistics</span></span>
- <span data-ttu-id="a052c-126">모든</span><span class="sxs-lookup"><span data-stu-id="a052c-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="a052c-127">-JobId</span></span>
<span data-ttu-id="a052c-128">가져올 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-129">-이름</span><span class="sxs-lookup"><span data-stu-id="a052c-129">-Name</span></span>
<span data-ttu-id="a052c-130">작업 목록 결과를 필터링 하는 데 사용할 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="a052c-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a052c-132">않아야</span><span class="sxs-lookup"><span data-stu-id="a052c-132">None</span></span>
- <span data-ttu-id="a052c-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="a052c-133">DebugInfo</span></span>
- <span data-ttu-id="a052c-134">통계</span><span class="sxs-lookup"><span data-stu-id="a052c-134">Statistics</span></span>
- <span data-ttu-id="a052c-135">모든</span><span class="sxs-lookup"><span data-stu-id="a052c-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="a052c-136">-PipelineId</span></span>
<span data-ttu-id="a052c-137">지정 된 파이프라인의 작업 부분만 반환 해야 함을 나타내는 선택적 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="a052c-138">-RecurrenceId</span></span>
<span data-ttu-id="a052c-139">지정 된 되풀이의 작업 부분만 반환 해야 하는 선택적 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-140">-결과</span><span class="sxs-lookup"><span data-stu-id="a052c-140">-Result</span></span>
<span data-ttu-id="a052c-141">작업 결과에 대 한 결과 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="a052c-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a052c-143">않아야</span><span class="sxs-lookup"><span data-stu-id="a052c-143">None</span></span>
- <span data-ttu-id="a052c-144">되었습니다</span><span class="sxs-lookup"><span data-stu-id="a052c-144">Cancelled</span></span>
- <span data-ttu-id="a052c-145">못함</span><span class="sxs-lookup"><span data-stu-id="a052c-145">Failed</span></span>
- <span data-ttu-id="a052c-146">했음을</span><span class="sxs-lookup"><span data-stu-id="a052c-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-147">-상태</span><span class="sxs-lookup"><span data-stu-id="a052c-147">-State</span></span>
<span data-ttu-id="a052c-148">작업 결과에 대 한 상태 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="a052c-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a052c-150">들였습니다</span><span class="sxs-lookup"><span data-stu-id="a052c-150">Accepted</span></span>
- <span data-ttu-id="a052c-151">새로운</span><span class="sxs-lookup"><span data-stu-id="a052c-151">New</span></span>
- <span data-ttu-id="a052c-152">컴파일에</span><span class="sxs-lookup"><span data-stu-id="a052c-152">Compiling</span></span>
- <span data-ttu-id="a052c-153">일정</span><span class="sxs-lookup"><span data-stu-id="a052c-153">Scheduling</span></span>
- <span data-ttu-id="a052c-154">시킵니다</span><span class="sxs-lookup"><span data-stu-id="a052c-154">Queued</span></span>
- <span data-ttu-id="a052c-155">시작</span><span class="sxs-lookup"><span data-stu-id="a052c-155">Starting</span></span>
- <span data-ttu-id="a052c-156">정지</span><span class="sxs-lookup"><span data-stu-id="a052c-156">Paused</span></span>
- <span data-ttu-id="a052c-157">실행</span><span class="sxs-lookup"><span data-stu-id="a052c-157">Running</span></span>
- <span data-ttu-id="a052c-158">종료</span><span class="sxs-lookup"><span data-stu-id="a052c-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-159">-다음 시간 후에 submitted</span><span class="sxs-lookup"><span data-stu-id="a052c-159">-SubmittedAfter</span></span>
<span data-ttu-id="a052c-160">날짜 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-160">Specifies a date filter.</span></span>
<span data-ttu-id="a052c-161">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 날짜 이후에 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-162">-이전에 submitted</span><span class="sxs-lookup"><span data-stu-id="a052c-162">-SubmittedBefore</span></span>
<span data-ttu-id="a052c-163">날짜 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-163">Specifies a date filter.</span></span>
<span data-ttu-id="a052c-164">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 날짜 이전에 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-165">-제출자</span><span class="sxs-lookup"><span data-stu-id="a052c-165">-Submitter</span></span>
<span data-ttu-id="a052c-166">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="a052c-167">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 사용자가 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-168">-위쪽</span><span class="sxs-lookup"><span data-stu-id="a052c-168">-Top</span></span>
<span data-ttu-id="a052c-169">반환할 작업의 수를 나타내는 선택적 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="a052c-170">기본값은 500입니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a052c-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a052c-171">CommonParameters</span></span>
<span data-ttu-id="a052c-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a052c-173">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a052c-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a052c-174">입력</span><span class="sxs-lookup"><span data-stu-id="a052c-174">INPUTS</span></span>

### <span data-ttu-id="a052c-175">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a052c-175">System.String</span></span>

### <span data-ttu-id="a052c-176">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="a052c-176">System.Guid</span></span>

### <span data-ttu-id="a052c-177">DataLakeAnalytics/DataLakeAnalyticsEnums + ExtendedJobData (Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a052c-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="a052c-178">시스템 Null 허용 ' 1 [[CoreLib, System.webserver, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a052c-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a052c-179">DataLake를 JobState []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="a052c-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="a052c-180">DataLake의 JobResult []을 (를)</span><span class="sxs-lookup"><span data-stu-id="a052c-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="a052c-181">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="a052c-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a052c-182">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a052c-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a052c-183">출력</span><span class="sxs-lookup"><span data-stu-id="a052c-183">OUTPUTS</span></span>

### <span data-ttu-id="a052c-184">DataLake에 대 한 정보를 보려면</span><span class="sxs-lookup"><span data-stu-id="a052c-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="a052c-185">상속자</span><span class="sxs-lookup"><span data-stu-id="a052c-185">NOTES</span></span>

## <span data-ttu-id="a052c-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a052c-186">RELATED LINKS</span></span>

[<span data-ttu-id="a052c-187">중지-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a052c-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="a052c-188">제출-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a052c-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="a052c-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a052c-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


