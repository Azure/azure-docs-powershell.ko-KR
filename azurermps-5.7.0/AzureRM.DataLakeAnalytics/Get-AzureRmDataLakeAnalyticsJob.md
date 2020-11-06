---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525136"
---
# <span data-ttu-id="76f73-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="76f73-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="76f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f73-102">SYNOPSIS</span></span>
<span data-ttu-id="76f73-103">Data Lake Analytics 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76f73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76f73-104">SYNTAX</span></span>

### <span data-ttu-id="76f73-105">GetAllInResourceGroupAndAccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="76f73-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76f73-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="76f73-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76f73-107">설명은</span><span class="sxs-lookup"><span data-stu-id="76f73-107">DESCRIPTION</span></span>
<span data-ttu-id="76f73-108">**AzureRmDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake 분석 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="76f73-109">작업을 지정 하지 않으면이 cmdlet은 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="76f73-110">예제의</span><span class="sxs-lookup"><span data-stu-id="76f73-110">EXAMPLES</span></span>

### <span data-ttu-id="76f73-111">예제 1: 지정 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="76f73-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="76f73-112">이 명령은 지정 된 ID의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="76f73-113">예제 2: 지난 주에 제출 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="76f73-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="76f73-114">이 명령은 지난 주에 제출 된 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="76f73-115">변수</span><span class="sxs-lookup"><span data-stu-id="76f73-115">PARAMETERS</span></span>

### <span data-ttu-id="76f73-116">-계정</span><span class="sxs-lookup"><span data-stu-id="76f73-116">-Account</span></span>
<span data-ttu-id="76f73-117">Data Lake Analytics 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f73-118">-DefaultProfile</span></span>
<span data-ttu-id="76f73-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="76f73-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76f73-120">-포함</span><span class="sxs-lookup"><span data-stu-id="76f73-120">-Include</span></span>
<span data-ttu-id="76f73-121">작업에 대해 검색할 추가 정보 유형을 나타내는 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="76f73-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76f73-123">않아야</span><span class="sxs-lookup"><span data-stu-id="76f73-123">None</span></span>
- <span data-ttu-id="76f73-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="76f73-124">DebugInfo</span></span>
- <span data-ttu-id="76f73-125">통계</span><span class="sxs-lookup"><span data-stu-id="76f73-125">Statistics</span></span>
- <span data-ttu-id="76f73-126">모든</span><span class="sxs-lookup"><span data-stu-id="76f73-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="76f73-127">-JobId</span></span>
<span data-ttu-id="76f73-128">가져올 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-129">-이름</span><span class="sxs-lookup"><span data-stu-id="76f73-129">-Name</span></span>
<span data-ttu-id="76f73-130">작업 목록 결과를 필터링 하는 데 사용할 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="76f73-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76f73-132">않아야</span><span class="sxs-lookup"><span data-stu-id="76f73-132">None</span></span>
- <span data-ttu-id="76f73-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="76f73-133">DebugInfo</span></span>
- <span data-ttu-id="76f73-134">통계</span><span class="sxs-lookup"><span data-stu-id="76f73-134">Statistics</span></span>
- <span data-ttu-id="76f73-135">모든</span><span class="sxs-lookup"><span data-stu-id="76f73-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="76f73-136">-PipelineId</span></span>
<span data-ttu-id="76f73-137">지정 된 파이프라인의 작업 부분만 반환 해야 함을 나타내는 선택적 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="76f73-138">-RecurrenceId</span></span>
<span data-ttu-id="76f73-139">지정 된 되풀이의 작업 부분만 반환 해야 하는 선택적 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-140">-결과</span><span class="sxs-lookup"><span data-stu-id="76f73-140">-Result</span></span>
<span data-ttu-id="76f73-141">작업 결과에 대 한 결과 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="76f73-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76f73-143">않아야</span><span class="sxs-lookup"><span data-stu-id="76f73-143">None</span></span>
- <span data-ttu-id="76f73-144">되었습니다</span><span class="sxs-lookup"><span data-stu-id="76f73-144">Cancelled</span></span>
- <span data-ttu-id="76f73-145">못함</span><span class="sxs-lookup"><span data-stu-id="76f73-145">Failed</span></span>
- <span data-ttu-id="76f73-146">했음을</span><span class="sxs-lookup"><span data-stu-id="76f73-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-147">-상태</span><span class="sxs-lookup"><span data-stu-id="76f73-147">-State</span></span>
<span data-ttu-id="76f73-148">작업 결과에 대 한 상태 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="76f73-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76f73-150">들였습니다</span><span class="sxs-lookup"><span data-stu-id="76f73-150">Accepted</span></span>
- <span data-ttu-id="76f73-151">새로운</span><span class="sxs-lookup"><span data-stu-id="76f73-151">New</span></span>
- <span data-ttu-id="76f73-152">컴파일에</span><span class="sxs-lookup"><span data-stu-id="76f73-152">Compiling</span></span>
- <span data-ttu-id="76f73-153">일정</span><span class="sxs-lookup"><span data-stu-id="76f73-153">Scheduling</span></span>
- <span data-ttu-id="76f73-154">시킵니다</span><span class="sxs-lookup"><span data-stu-id="76f73-154">Queued</span></span>
- <span data-ttu-id="76f73-155">시작</span><span class="sxs-lookup"><span data-stu-id="76f73-155">Starting</span></span>
- <span data-ttu-id="76f73-156">정지</span><span class="sxs-lookup"><span data-stu-id="76f73-156">Paused</span></span>
- <span data-ttu-id="76f73-157">실행</span><span class="sxs-lookup"><span data-stu-id="76f73-157">Running</span></span>
- <span data-ttu-id="76f73-158">종료</span><span class="sxs-lookup"><span data-stu-id="76f73-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-159">-다음 시간 후에 submitted</span><span class="sxs-lookup"><span data-stu-id="76f73-159">-SubmittedAfter</span></span>
<span data-ttu-id="76f73-160">날짜 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-160">Specifies a date filter.</span></span>
<span data-ttu-id="76f73-161">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 날짜 이후에 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-162">-이전에 submitted</span><span class="sxs-lookup"><span data-stu-id="76f73-162">-SubmittedBefore</span></span>
<span data-ttu-id="76f73-163">날짜 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-163">Specifies a date filter.</span></span>
<span data-ttu-id="76f73-164">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 날짜 이전에 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-165">-제출자</span><span class="sxs-lookup"><span data-stu-id="76f73-165">-Submitter</span></span>
<span data-ttu-id="76f73-166">사용자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="76f73-167">이 매개 변수를 사용 하 여 작업 목록 결과를 지정 된 사용자가 제출한 작업으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-168">-위쪽</span><span class="sxs-lookup"><span data-stu-id="76f73-168">-Top</span></span>
<span data-ttu-id="76f73-169">반환할 작업의 수를 나타내는 선택적 값입니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="76f73-170">기본값은 500입니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f73-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f73-171">CommonParameters</span></span>
<span data-ttu-id="76f73-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f73-173">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f73-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f73-174">입력</span><span class="sxs-lookup"><span data-stu-id="76f73-174">INPUTS</span></span>

### <span data-ttu-id="76f73-175">Shap</span><span class="sxs-lookup"><span data-stu-id="76f73-175">Guid</span></span>
<span data-ttu-id="76f73-176">' JobId ' 매개 변수는 파이프라인에서 ' Guid ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="76f73-177">출력</span><span class="sxs-lookup"><span data-stu-id="76f73-177">OUTPUTS</span></span>

### <span data-ttu-id="76f73-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="76f73-178">JobInformation</span></span>
<span data-ttu-id="76f73-179">지정 된 작업 정보 세부 정보</span><span class="sxs-lookup"><span data-stu-id="76f73-179">The specified job information details</span></span>

### <span data-ttu-id="76f73-180">목록<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="76f73-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="76f73-181">지정 된 Data Lake Analytics 계정의 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="76f73-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="76f73-182">상속자</span><span class="sxs-lookup"><span data-stu-id="76f73-182">NOTES</span></span>

## <span data-ttu-id="76f73-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76f73-183">RELATED LINKS</span></span>

[<span data-ttu-id="76f73-184">중지-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="76f73-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="76f73-185">제출-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="76f73-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="76f73-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="76f73-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


