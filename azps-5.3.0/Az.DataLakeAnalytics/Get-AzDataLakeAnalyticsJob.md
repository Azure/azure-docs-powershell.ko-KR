---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493482"
---
# <span data-ttu-id="a29b7-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a29b7-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="a29b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a29b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a29b7-103">Data Lake Analytics 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="a29b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="a29b7-104">SYNTAX</span></span>

### <span data-ttu-id="a29b7-105">GetAllInResourceGroupAndAccount(기본값)</span><span class="sxs-lookup"><span data-stu-id="a29b7-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a29b7-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="a29b7-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a29b7-107">설명</span><span class="sxs-lookup"><span data-stu-id="a29b7-107">DESCRIPTION</span></span>
<span data-ttu-id="a29b7-108">**Get-AzDataLakeAnalyticsJob** cmdlet은 Azure Data Lake Analytics 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="a29b7-109">작업을 지정하지 않으면 이 cmdlet은 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="a29b7-110">예제</span><span class="sxs-lookup"><span data-stu-id="a29b7-110">EXAMPLES</span></span>

### <span data-ttu-id="a29b7-111">예제 1: 지정된 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="a29b7-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="a29b7-112">이 명령은 지정된 ID를 사용하여 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="a29b7-113">예제 2: 지난 주에 제출된 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="a29b7-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="a29b7-114">이 명령은 지난 주에 제출된 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="a29b7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a29b7-115">PARAMETERS</span></span>

### <span data-ttu-id="a29b7-116">-Account</span><span class="sxs-lookup"><span data-stu-id="a29b7-116">-Account</span></span>
<span data-ttu-id="a29b7-117">Data Lake Analytics 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a29b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29b7-118">-DefaultProfile</span></span>
<span data-ttu-id="a29b7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a29b7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a29b7-120">-Include</span><span class="sxs-lookup"><span data-stu-id="a29b7-120">-Include</span></span>
<span data-ttu-id="a29b7-121">작업 관련 정보를 검색할 추가 정보의 유형을 나타내는 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="a29b7-122">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a29b7-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a29b7-123">없음</span><span class="sxs-lookup"><span data-stu-id="a29b7-123">None</span></span>
- <span data-ttu-id="a29b7-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="a29b7-124">DebugInfo</span></span>
- <span data-ttu-id="a29b7-125">통계</span><span class="sxs-lookup"><span data-stu-id="a29b7-125">Statistics</span></span>
- <span data-ttu-id="a29b7-126">모두</span><span class="sxs-lookup"><span data-stu-id="a29b7-126">All</span></span>

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

### <span data-ttu-id="a29b7-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="a29b7-127">-JobId</span></span>
<span data-ttu-id="a29b7-128">얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="a29b7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a29b7-129">-Name</span></span>
<span data-ttu-id="a29b7-130">작업 목록 결과를 필터링하는 데 사용할 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="a29b7-131">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a29b7-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a29b7-132">없음</span><span class="sxs-lookup"><span data-stu-id="a29b7-132">None</span></span>
- <span data-ttu-id="a29b7-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="a29b7-133">DebugInfo</span></span>
- <span data-ttu-id="a29b7-134">통계</span><span class="sxs-lookup"><span data-stu-id="a29b7-134">Statistics</span></span>
- <span data-ttu-id="a29b7-135">모두</span><span class="sxs-lookup"><span data-stu-id="a29b7-135">All</span></span>

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

### <span data-ttu-id="a29b7-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="a29b7-136">-PipelineId</span></span>
<span data-ttu-id="a29b7-137">지정된 파이프라인의 작업 부분만 나타내는 선택적 ID가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="a29b7-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="a29b7-138">-RecurrenceId</span></span>
<span data-ttu-id="a29b7-139">지정된 재귀의 작업 부분만 나타내는 선택적 ID가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="a29b7-140">-Result</span><span class="sxs-lookup"><span data-stu-id="a29b7-140">-Result</span></span>
<span data-ttu-id="a29b7-141">작업 결과에 대한 결과 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="a29b7-142">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a29b7-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a29b7-143">없음</span><span class="sxs-lookup"><span data-stu-id="a29b7-143">None</span></span>
- <span data-ttu-id="a29b7-144">Cancelled</span><span class="sxs-lookup"><span data-stu-id="a29b7-144">Cancelled</span></span>
- <span data-ttu-id="a29b7-145">실패</span><span class="sxs-lookup"><span data-stu-id="a29b7-145">Failed</span></span>
- <span data-ttu-id="a29b7-146">성공</span><span class="sxs-lookup"><span data-stu-id="a29b7-146">Succeeded</span></span>

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

### <span data-ttu-id="a29b7-147">-State</span><span class="sxs-lookup"><span data-stu-id="a29b7-147">-State</span></span>
<span data-ttu-id="a29b7-148">작업 결과에 대한 상태 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="a29b7-149">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a29b7-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a29b7-150">수락</span><span class="sxs-lookup"><span data-stu-id="a29b7-150">Accepted</span></span>
- <span data-ttu-id="a29b7-151">새로운</span><span class="sxs-lookup"><span data-stu-id="a29b7-151">New</span></span>
- <span data-ttu-id="a29b7-152">컴파일</span><span class="sxs-lookup"><span data-stu-id="a29b7-152">Compiling</span></span>
- <span data-ttu-id="a29b7-153">Scheduling</span><span class="sxs-lookup"><span data-stu-id="a29b7-153">Scheduling</span></span>
- <span data-ttu-id="a29b7-154">큐에 대기</span><span class="sxs-lookup"><span data-stu-id="a29b7-154">Queued</span></span>
- <span data-ttu-id="a29b7-155">시작</span><span class="sxs-lookup"><span data-stu-id="a29b7-155">Starting</span></span>
- <span data-ttu-id="a29b7-156">일시 중지</span><span class="sxs-lookup"><span data-stu-id="a29b7-156">Paused</span></span>
- <span data-ttu-id="a29b7-157">실행 중</span><span class="sxs-lookup"><span data-stu-id="a29b7-157">Running</span></span>
- <span data-ttu-id="a29b7-158">종료</span><span class="sxs-lookup"><span data-stu-id="a29b7-158">Ended</span></span>

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

### <span data-ttu-id="a29b7-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="a29b7-159">-SubmittedAfter</span></span>
<span data-ttu-id="a29b7-160">날짜 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-160">Specifies a date filter.</span></span>
<span data-ttu-id="a29b7-161">이 매개 변수를 사용하여 지정된 날짜 이후에 제출된 작업으로 작업 목록 결과를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="a29b7-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="a29b7-162">-SubmittedBefore</span></span>
<span data-ttu-id="a29b7-163">날짜 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-163">Specifies a date filter.</span></span>
<span data-ttu-id="a29b7-164">이 매개 변수를 사용하여 지정된 날짜 전에 제출된 작업으로 작업 목록 결과를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="a29b7-165">-Submitter</span><span class="sxs-lookup"><span data-stu-id="a29b7-165">-Submitter</span></span>
<span data-ttu-id="a29b7-166">사용자의 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="a29b7-167">이 매개 변수를 사용하여 지정된 사용자가 제출한 작업으로 작업 목록 결과를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="a29b7-168">-Top</span><span class="sxs-lookup"><span data-stu-id="a29b7-168">-Top</span></span>
<span data-ttu-id="a29b7-169">반환할 작업 수를 나타내는 선택적 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="a29b7-170">기본값은 500입니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-170">Default value is 500</span></span>

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

### <span data-ttu-id="a29b7-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29b7-171">CommonParameters</span></span>
<span data-ttu-id="a29b7-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a29b7-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29b7-173">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a29b7-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29b7-174">입력</span><span class="sxs-lookup"><span data-stu-id="a29b7-174">INPUTS</span></span>

### <span data-ttu-id="a29b7-175">System.String</span><span class="sxs-lookup"><span data-stu-id="a29b7-175">System.String</span></span>

### <span data-ttu-id="a29b7-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a29b7-176">System.Guid</span></span>

### <span data-ttu-id="a29b7-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="a29b7-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="a29b7-178">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a29b7-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a29b7-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="a29b7-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="a29b7-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="a29b7-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="a29b7-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a29b7-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a29b7-182">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a29b7-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a29b7-183">출력</span><span class="sxs-lookup"><span data-stu-id="a29b7-183">OUTPUTS</span></span>

### <span data-ttu-id="a29b7-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="a29b7-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="a29b7-185">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a29b7-185">NOTES</span></span>

## <span data-ttu-id="a29b7-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a29b7-186">RELATED LINKS</span></span>

[<span data-ttu-id="a29b7-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a29b7-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="a29b7-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a29b7-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="a29b7-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a29b7-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


