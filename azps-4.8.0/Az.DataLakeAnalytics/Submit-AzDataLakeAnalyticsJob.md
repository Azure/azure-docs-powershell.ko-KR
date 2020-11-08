---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047861"
---
# <span data-ttu-id="ceaf4-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ceaf4-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="ceaf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceaf4-102">SYNOPSIS</span></span>
<span data-ttu-id="ceaf4-103">작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-103">Submits a job.</span></span>

## <span data-ttu-id="ceaf4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ceaf4-104">SYNTAX</span></span>

### <span data-ttu-id="ceaf4-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="ceaf4-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceaf4-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="ceaf4-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceaf4-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="ceaf4-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceaf4-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="ceaf4-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceaf4-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="ceaf4-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ceaf4-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="ceaf4-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ceaf4-111">설명은</span><span class="sxs-lookup"><span data-stu-id="ceaf4-111">DESCRIPTION</span></span>
<span data-ttu-id="ceaf4-112">**AzDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake Analytics 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="ceaf4-113">예제의</span><span class="sxs-lookup"><span data-stu-id="ceaf4-113">EXAMPLES</span></span>

### <span data-ttu-id="ceaf4-114">예제 1: 작업 제출</span><span class="sxs-lookup"><span data-stu-id="ceaf4-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="ceaf4-115">이 명령은 Data Lake Analytics 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="ceaf4-116">예제 2: 스크립트 매개 변수를 사용 하 여 작업 제출</span><span class="sxs-lookup"><span data-stu-id="ceaf4-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="ceaf4-117">U-SQL 스크립트 매개 변수는 기본 스크립트 콘텐츠 위에 앞에 붙습니다 (예: DECLARE @Department string = "Sales"). @NumRecords Int = 1000를 선언 합니다. @StartDateTime Datetime = New datetime (2017, 12, 6, 0, 0, 0, 0)을 선언 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="ceaf4-118">변수</span><span class="sxs-lookup"><span data-stu-id="ceaf4-118">PARAMETERS</span></span>

### <span data-ttu-id="ceaf4-119">-계정</span><span class="sxs-lookup"><span data-stu-id="ceaf4-119">-Account</span></span>
<span data-ttu-id="ceaf4-120">작업을 제출할 데이터 호수 분석 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="ceaf4-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="ceaf4-121">-AnalyticsUnits</span></span>
<span data-ttu-id="ceaf4-122">이 작업에 사용할 분석 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-122">The analytics units to use for this job.</span></span> <span data-ttu-id="ceaf4-123">일반적으로 스크립트 전용 분석 단위는 더 빠르게 스크립트 실행 시간을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="ceaf4-124">-CompileMode</span></span>
<span data-ttu-id="ceaf4-125">이 작업에서 수행할 컴파일 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="ceaf4-126">유효한 값:</span><span class="sxs-lookup"><span data-stu-id="ceaf4-126">Valid values:</span></span> 
- <span data-ttu-id="ceaf4-127">의미 체계 (의미적 검사 및 필요한 온전성 검사만 수행)</span><span class="sxs-lookup"><span data-stu-id="ceaf4-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="ceaf4-128">전체 (전체 컴파일)</span><span class="sxs-lookup"><span data-stu-id="ceaf4-128">Full (Full compilation)</span></span>
- <span data-ttu-id="ceaf4-129">SingleBox (로컬에서 수행 되는 전체 컴파일)</span><span class="sxs-lookup"><span data-stu-id="ceaf4-129">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="ceaf4-130">-CompileOnly</span></span>
<span data-ttu-id="ceaf4-131">제출 서류가 작업을 빌드 해야 하며 true로 설정 된 경우 실행 되지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceaf4-132">-DefaultProfile</span></span>
<span data-ttu-id="ceaf4-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ceaf4-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ceaf4-134">-이름</span><span class="sxs-lookup"><span data-stu-id="ceaf4-134">-Name</span></span>
<span data-ttu-id="ceaf4-135">제출할 작업의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-135">The friendly name of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="ceaf4-136">-PipelineId</span></span>
<span data-ttu-id="ceaf4-137">이 작업의 제출을 나타내는 ID는 되풀이 작업 집합의 일부 이며 작업 파이프라인에도 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="ceaf4-138">-PipelineName</span></span>
<span data-ttu-id="ceaf4-139">이 작업과 연결 된 파이프라인에 대 한 선택적 친근 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="ceaf4-140">-PipelineUri</span></span>
<span data-ttu-id="ceaf4-141">이 파이프라인과 연결 된 원래 서비스에 연결 하는 선택적 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-142">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="ceaf4-142">-Priority</span></span>
<span data-ttu-id="ceaf4-143">작업의 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-143">The priority of the job.</span></span> <span data-ttu-id="ceaf4-144">지정 하지 않은 경우 우선 순위는 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="ceaf4-145">숫자가 낮을수록 높은 작업 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-145">A lower number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="ceaf4-146">-RecurrenceId</span></span>
<span data-ttu-id="ceaf4-147">이 작업의 제출을 나타내는 ID는 동일한 되풀이 ID를 사용 하는 되풀이 작업 집합의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="ceaf4-148">-RecurrenceName</span></span>
<span data-ttu-id="ceaf4-149">작업 간의 되풀이 상관 관계에 대 한 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="ceaf4-150">-RunId</span></span>
<span data-ttu-id="ceaf4-151">파이프라인의 특정 실행 반복을 식별 하는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-152">런타임</span><span class="sxs-lookup"><span data-stu-id="ceaf4-152">-Runtime</span></span>
<span data-ttu-id="ceaf4-153">선택적으로 작업에 사용할 런타임 버전을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="ceaf4-154">설정 되지 않은 상태로 두면 기본 런타임이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-154">If left unset, the default runtime is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-155">-스크립트</span><span class="sxs-lookup"><span data-stu-id="ceaf4-155">-Script</span></span>
<span data-ttu-id="ceaf4-156">실행할 스크립트 (인라인 작성)</span><span class="sxs-lookup"><span data-stu-id="ceaf4-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="ceaf4-157">-ScriptParameter</span></span>
<span data-ttu-id="ceaf4-158">이 작업의 스크립트 매개 변수는 값에 대 한 매개 변수 이름 (문자열)의 사전 (바이트, sbyte, int, uint (또는 uint32), long, ulong (uint64), float, double, decimal, short (or int16), ushort (또는 uint16), char, string, DateTime, bool, Guid 또는 byte [])입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="ceaf4-159">-ScriptPath</span></span>
<span data-ttu-id="ceaf4-160">제출할 스크립트 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceaf4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceaf4-161">CommonParameters</span></span>
<span data-ttu-id="ceaf4-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceaf4-163">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceaf4-164">입력</span><span class="sxs-lookup"><span data-stu-id="ceaf4-164">INPUTS</span></span>

### <span data-ttu-id="ceaf4-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ceaf4-165">System.String</span></span>

### <span data-ttu-id="ceaf4-166">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ceaf4-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ceaf4-167">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-167">System.Int32</span></span>

### <span data-ttu-id="ceaf4-168">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="ceaf4-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="ceaf4-169">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="ceaf4-169">System.Guid</span></span>

### <span data-ttu-id="ceaf4-170">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ceaf4-171">출력</span><span class="sxs-lookup"><span data-stu-id="ceaf4-171">OUTPUTS</span></span>

### <span data-ttu-id="ceaf4-172">DataLake에 대 한 정보를 보려면</span><span class="sxs-lookup"><span data-stu-id="ceaf4-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="ceaf4-173">상속자</span><span class="sxs-lookup"><span data-stu-id="ceaf4-173">NOTES</span></span>

## <span data-ttu-id="ceaf4-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceaf4-174">RELATED LINKS</span></span>

[<span data-ttu-id="ceaf4-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ceaf4-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ceaf4-176">중지-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ceaf4-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ceaf4-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ceaf4-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


