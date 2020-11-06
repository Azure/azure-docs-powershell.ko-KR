---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537308"
---
# <span data-ttu-id="4c35e-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4c35e-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="4c35e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c35e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c35e-103">Data Lake Analytics 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c35e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c35e-104">SYNTAX</span></span>

### <span data-ttu-id="4c35e-105">리소스 그룹 및 계정에서 모두 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4c35e-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c35e-106">특정 JobInformation</span><span class="sxs-lookup"><span data-stu-id="4c35e-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c35e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4c35e-107">DESCRIPTION</span></span>
<span data-ttu-id="4c35e-108">**AzureRmDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake 분석 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="4c35e-109">작업을 지정 하지 않으면이 cmdlet은 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="4c35e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4c35e-110">EXAMPLES</span></span>

### <span data-ttu-id="4c35e-111">예제 1: 지정 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="4c35e-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="4c35e-112">이 명령은 지정 된 ID의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="4c35e-113">예제 2: 지난 주에 제출 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="4c35e-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="4c35e-114">이 명령은 지난 주에 제출 된 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="4c35e-115">변수</span><span class="sxs-lookup"><span data-stu-id="4c35e-115">PARAMETERS</span></span>

### <span data-ttu-id="4c35e-116">-계정</span><span class="sxs-lookup"><span data-stu-id="4c35e-116">-Account</span></span>
<span data-ttu-id="4c35e-117">Data Lake Analytics 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="4c35e-118">-포함</span><span class="sxs-lookup"><span data-stu-id="4c35e-118">-Include</span></span>
<span data-ttu-id="4c35e-119">작업에 대해 검색할 추가 정보 유형을 나타내는 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="4c35e-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c35e-121">않아야</span><span class="sxs-lookup"><span data-stu-id="4c35e-121">None</span></span>
- <span data-ttu-id="4c35e-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="4c35e-122">DebugInfo</span></span>
- <span data-ttu-id="4c35e-123">통계</span><span class="sxs-lookup"><span data-stu-id="4c35e-123">Statistics</span></span>
- <span data-ttu-id="4c35e-124">모든</span><span class="sxs-lookup"><span data-stu-id="4c35e-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="4c35e-125">-JobId</span></span>
<span data-ttu-id="4c35e-126">가져올 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-127">-이름</span><span class="sxs-lookup"><span data-stu-id="4c35e-127">-Name</span></span>
<span data-ttu-id="4c35e-128">작업 목록 결과를 필터링 하는 데 사용할 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="4c35e-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c35e-130">않아야</span><span class="sxs-lookup"><span data-stu-id="4c35e-130">None</span></span>
- <span data-ttu-id="4c35e-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="4c35e-131">DebugInfo</span></span>
- <span data-ttu-id="4c35e-132">통계</span><span class="sxs-lookup"><span data-stu-id="4c35e-132">Statistics</span></span>
- <span data-ttu-id="4c35e-133">모든</span><span class="sxs-lookup"><span data-stu-id="4c35e-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-134">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="4c35e-134">-PipelineId</span></span>
<span data-ttu-id="4c35e-135">지정 된 파이프라인의 작업 부분만 반환 해야 함을 나타내는 선택적 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-136">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="4c35e-136">-RecurrenceId</span></span>
<span data-ttu-id="4c35e-137">지정 된 되풀이의 작업 부분만 반환 해야 하는 선택적 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-138">-결과</span><span class="sxs-lookup"><span data-stu-id="4c35e-138">-Result</span></span>
<span data-ttu-id="4c35e-139">작업 결과에 대 한 결과 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="4c35e-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c35e-141">않아야</span><span class="sxs-lookup"><span data-stu-id="4c35e-141">None</span></span>
- <span data-ttu-id="4c35e-142">되었습니다</span><span class="sxs-lookup"><span data-stu-id="4c35e-142">Cancelled</span></span>
- <span data-ttu-id="4c35e-143">못함</span><span class="sxs-lookup"><span data-stu-id="4c35e-143">Failed</span></span>
- <span data-ttu-id="4c35e-144">했음을</span><span class="sxs-lookup"><span data-stu-id="4c35e-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-145">-상태</span><span class="sxs-lookup"><span data-stu-id="4c35e-145">-State</span></span>
<span data-ttu-id="4c35e-146">작업 결과에 대 한 상태 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="4c35e-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c35e-148">들였습니다</span><span class="sxs-lookup"><span data-stu-id="4c35e-148">Accepted</span></span>
- <span data-ttu-id="4c35e-149">새로운</span><span class="sxs-lookup"><span data-stu-id="4c35e-149">New</span></span>
- <span data-ttu-id="4c35e-150">컴파일에</span><span class="sxs-lookup"><span data-stu-id="4c35e-150">Compiling</span></span>
- <span data-ttu-id="4c35e-151">일정</span><span class="sxs-lookup"><span data-stu-id="4c35e-151">Scheduling</span></span>
- <span data-ttu-id="4c35e-152">시킵니다</span><span class="sxs-lookup"><span data-stu-id="4c35e-152">Queued</span></span>
- <span data-ttu-id="4c35e-153">시작</span><span class="sxs-lookup"><span data-stu-id="4c35e-153">Starting</span></span>
- <span data-ttu-id="4c35e-154">정지</span><span class="sxs-lookup"><span data-stu-id="4c35e-154">Paused</span></span>
- <span data-ttu-id="4c35e-155">실행</span><span class="sxs-lookup"><span data-stu-id="4c35e-155">Running</span></span>
- <span data-ttu-id="4c35e-156">종료</span><span class="sxs-lookup"><span data-stu-id="4c35e-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-157">-다음 시간 후에 submitted</span><span class="sxs-lookup"><span data-stu-id="4c35e-157">-SubmittedAfter</span></span>
<span data-ttu-id="4c35e-158">날짜 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-158">Specifies a date filter.</span></span>
<span data-ttu-id="4c35e-159">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 날짜 이후에 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-160">-이전에 submitted</span><span class="sxs-lookup"><span data-stu-id="4c35e-160">-SubmittedBefore</span></span>
<span data-ttu-id="4c35e-161">날짜 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-161">Specifies a date filter.</span></span>
<span data-ttu-id="4c35e-162">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 날짜 이전에 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-163">-제출자</span><span class="sxs-lookup"><span data-stu-id="4c35e-163">-Submitter</span></span>
<span data-ttu-id="4c35e-164">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="4c35e-165">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 사용자가 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-166">-위쪽</span><span class="sxs-lookup"><span data-stu-id="4c35e-166">-Top</span></span>
<span data-ttu-id="4c35e-167">반환할 작업의 수를 나타내는 선택적 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="4c35e-168">기본값은 500입니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c35e-169">-DefaultProfile</span></span>
<span data-ttu-id="4c35e-170">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c35e-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c35e-171">CommonParameters</span></span>
<span data-ttu-id="4c35e-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c35e-173">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c35e-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c35e-174">입력</span><span class="sxs-lookup"><span data-stu-id="4c35e-174">INPUTS</span></span>

### <span data-ttu-id="4c35e-175">Shap</span><span class="sxs-lookup"><span data-stu-id="4c35e-175">Guid</span></span>
<span data-ttu-id="4c35e-176">' JobId ' 매개 변수는 파이프라인에서 ' Guid ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="4c35e-177">출력</span><span class="sxs-lookup"><span data-stu-id="4c35e-177">OUTPUTS</span></span>

### <span data-ttu-id="4c35e-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="4c35e-178">JobInformation</span></span>
<span data-ttu-id="4c35e-179">지정 된 작업 정보 세부 정보</span><span class="sxs-lookup"><span data-stu-id="4c35e-179">The specified job information details</span></span>

### <span data-ttu-id="4c35e-180">목록<JobInformation></span><span class="sxs-lookup"><span data-stu-id="4c35e-180">List<JobInformation></span></span>
<span data-ttu-id="4c35e-181">지정 된 Data Lake Analytics 계정의 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4c35e-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="4c35e-182">상속자</span><span class="sxs-lookup"><span data-stu-id="4c35e-182">NOTES</span></span>

## <span data-ttu-id="4c35e-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c35e-183">RELATED LINKS</span></span>

[<span data-ttu-id="4c35e-184">중지-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4c35e-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4c35e-185">제출-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4c35e-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4c35e-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4c35e-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


