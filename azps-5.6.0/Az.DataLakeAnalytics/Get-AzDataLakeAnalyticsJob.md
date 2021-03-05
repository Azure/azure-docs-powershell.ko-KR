---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 0078196d8b06ae791fa0855345eec02d1f2eb59c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974955"
---
# <span data-ttu-id="0eba2-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0eba2-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="0eba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eba2-102">SYNOPSIS</span></span>
<span data-ttu-id="0eba2-103">Data Lake Analytics 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="0eba2-104">구문</span><span class="sxs-lookup"><span data-stu-id="0eba2-104">SYNTAX</span></span>

### <span data-ttu-id="0eba2-105">GetAllInResourceGroupAndAccount(기본값)</span><span class="sxs-lookup"><span data-stu-id="0eba2-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eba2-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="0eba2-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eba2-107">설명</span><span class="sxs-lookup"><span data-stu-id="0eba2-107">DESCRIPTION</span></span>
<span data-ttu-id="0eba2-108">**Get-AzDataLakeAnalyticsJob** cmdlet은 Azure Data Lake Analytics 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="0eba2-109">작업을 지정하지 않으면 이 cmdlet은 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="0eba2-110">예제</span><span class="sxs-lookup"><span data-stu-id="0eba2-110">EXAMPLES</span></span>

### <span data-ttu-id="0eba2-111">예제 1: 지정된 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="0eba2-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="0eba2-112">이 명령은 지정된 ID를 사용하여 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="0eba2-113">예제 2: 지난 주에 제출된 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="0eba2-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="0eba2-114">이 명령은 지난 주에 제출된 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="0eba2-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0eba2-115">PARAMETERS</span></span>

### <span data-ttu-id="0eba2-116">-Account</span><span class="sxs-lookup"><span data-stu-id="0eba2-116">-Account</span></span>
<span data-ttu-id="0eba2-117">Data Lake Analytics 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0eba2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eba2-118">-DefaultProfile</span></span>
<span data-ttu-id="0eba2-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0eba2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eba2-120">-Include</span><span class="sxs-lookup"><span data-stu-id="0eba2-120">-Include</span></span>
<span data-ttu-id="0eba2-121">작업을 검색할 추가 정보 유형을 나타내는 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="0eba2-122">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eba2-123">없음</span><span class="sxs-lookup"><span data-stu-id="0eba2-123">None</span></span>
- <span data-ttu-id="0eba2-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="0eba2-124">DebugInfo</span></span>
- <span data-ttu-id="0eba2-125">통계</span><span class="sxs-lookup"><span data-stu-id="0eba2-125">Statistics</span></span>
- <span data-ttu-id="0eba2-126">모두</span><span class="sxs-lookup"><span data-stu-id="0eba2-126">All</span></span>

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

### <span data-ttu-id="0eba2-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="0eba2-127">-JobId</span></span>
<span data-ttu-id="0eba2-128">얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="0eba2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0eba2-129">-Name</span></span>
<span data-ttu-id="0eba2-130">작업 목록 결과를 필터링하는 데 사용할 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="0eba2-131">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eba2-132">없음</span><span class="sxs-lookup"><span data-stu-id="0eba2-132">None</span></span>
- <span data-ttu-id="0eba2-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="0eba2-133">DebugInfo</span></span>
- <span data-ttu-id="0eba2-134">통계</span><span class="sxs-lookup"><span data-stu-id="0eba2-134">Statistics</span></span>
- <span data-ttu-id="0eba2-135">모두</span><span class="sxs-lookup"><span data-stu-id="0eba2-135">All</span></span>

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

### <span data-ttu-id="0eba2-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="0eba2-136">-PipelineId</span></span>
<span data-ttu-id="0eba2-137">지정된 파이프라인의 작업 부분만 나타내는 선택적 ID를 반환해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="0eba2-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="0eba2-138">-RecurrenceId</span></span>
<span data-ttu-id="0eba2-139">지정된 재귀의 작업 부분만 나타내는 선택적 ID를 반환해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="0eba2-140">-Result</span><span class="sxs-lookup"><span data-stu-id="0eba2-140">-Result</span></span>
<span data-ttu-id="0eba2-141">작업 결과에 대한 결과 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="0eba2-142">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eba2-143">없음</span><span class="sxs-lookup"><span data-stu-id="0eba2-143">None</span></span>
- <span data-ttu-id="0eba2-144">취소</span><span class="sxs-lookup"><span data-stu-id="0eba2-144">Cancelled</span></span>
- <span data-ttu-id="0eba2-145">실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-145">Failed</span></span>
- <span data-ttu-id="0eba2-146">성공했습니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-146">Succeeded</span></span>

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

### <span data-ttu-id="0eba2-147">-State</span><span class="sxs-lookup"><span data-stu-id="0eba2-147">-State</span></span>
<span data-ttu-id="0eba2-148">작업 결과에 대한 상태 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="0eba2-149">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eba2-150">수락</span><span class="sxs-lookup"><span data-stu-id="0eba2-150">Accepted</span></span>
- <span data-ttu-id="0eba2-151">새로운</span><span class="sxs-lookup"><span data-stu-id="0eba2-151">New</span></span>
- <span data-ttu-id="0eba2-152">컴파일</span><span class="sxs-lookup"><span data-stu-id="0eba2-152">Compiling</span></span>
- <span data-ttu-id="0eba2-153">스컬링</span><span class="sxs-lookup"><span data-stu-id="0eba2-153">Scheduling</span></span>
- <span data-ttu-id="0eba2-154">큐에 대기</span><span class="sxs-lookup"><span data-stu-id="0eba2-154">Queued</span></span>
- <span data-ttu-id="0eba2-155">시작</span><span class="sxs-lookup"><span data-stu-id="0eba2-155">Starting</span></span>
- <span data-ttu-id="0eba2-156">일시 중지</span><span class="sxs-lookup"><span data-stu-id="0eba2-156">Paused</span></span>
- <span data-ttu-id="0eba2-157">실행 중</span><span class="sxs-lookup"><span data-stu-id="0eba2-157">Running</span></span>
- <span data-ttu-id="0eba2-158">종료</span><span class="sxs-lookup"><span data-stu-id="0eba2-158">Ended</span></span>

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

### <span data-ttu-id="0eba2-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="0eba2-159">-SubmittedAfter</span></span>
<span data-ttu-id="0eba2-160">날짜 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-160">Specifies a date filter.</span></span>
<span data-ttu-id="0eba2-161">이 매개 변수를 사용하여 지정된 날짜 이후에 제출된 작업으로 작업 목록 결과를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="0eba2-162">-submittedBefore</span><span class="sxs-lookup"><span data-stu-id="0eba2-162">-SubmittedBefore</span></span>
<span data-ttu-id="0eba2-163">날짜 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-163">Specifies a date filter.</span></span>
<span data-ttu-id="0eba2-164">이 매개 변수를 사용하여 지정된 날짜 전에 제출된 작업으로 작업 목록 결과를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="0eba2-165">-제출자</span><span class="sxs-lookup"><span data-stu-id="0eba2-165">-Submitter</span></span>
<span data-ttu-id="0eba2-166">사용자의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="0eba2-167">이 매개 변수를 사용하여 지정된 사용자가 제출한 작업으로 작업 목록 결과를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="0eba2-168">-Top</span><span class="sxs-lookup"><span data-stu-id="0eba2-168">-Top</span></span>
<span data-ttu-id="0eba2-169">반환할 작업 수를 나타내는 선택적 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="0eba2-170">기본값은 500입니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-170">Default value is 500</span></span>

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

### <span data-ttu-id="0eba2-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eba2-171">CommonParameters</span></span>
<span data-ttu-id="0eba2-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0eba2-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eba2-173">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0eba2-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eba2-174">입력</span><span class="sxs-lookup"><span data-stu-id="0eba2-174">INPUTS</span></span>

### <span data-ttu-id="0eba2-175">System.String</span><span class="sxs-lookup"><span data-stu-id="0eba2-175">System.String</span></span>

### <span data-ttu-id="0eba2-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0eba2-176">System.Guid</span></span>

### <span data-ttu-id="0eba2-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="0eba2-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="0eba2-178">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0eba2-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0eba2-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="0eba2-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="0eba2-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="0eba2-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="0eba2-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0eba2-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0eba2-182">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0eba2-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0eba2-183">출력</span><span class="sxs-lookup"><span data-stu-id="0eba2-183">OUTPUTS</span></span>

### <span data-ttu-id="0eba2-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="0eba2-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="0eba2-185">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0eba2-185">NOTES</span></span>

## <span data-ttu-id="0eba2-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0eba2-186">RELATED LINKS</span></span>

[<span data-ttu-id="0eba2-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0eba2-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="0eba2-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0eba2-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="0eba2-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0eba2-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


