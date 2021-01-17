---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345357"
---
# <span data-ttu-id="7e10b-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e10b-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="7e10b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e10b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e10b-103">작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-103">Submits a job.</span></span>

## <span data-ttu-id="7e10b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e10b-104">SYNTAX</span></span>

### <span data-ttu-id="7e10b-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="7e10b-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e10b-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="7e10b-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e10b-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="7e10b-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e10b-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="7e10b-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e10b-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="7e10b-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e10b-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="7e10b-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e10b-111">설명</span><span class="sxs-lookup"><span data-stu-id="7e10b-111">DESCRIPTION</span></span>
<span data-ttu-id="7e10b-112">**Submit-AzDataLakeAnalyticsJob** cmdlet은 Azure Data Lake Analytics 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="7e10b-113">예제</span><span class="sxs-lookup"><span data-stu-id="7e10b-113">EXAMPLES</span></span>

### <span data-ttu-id="7e10b-114">예제 1: 작업 제출</span><span class="sxs-lookup"><span data-stu-id="7e10b-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="7e10b-115">이 명령은 Data Lake Analytics 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="7e10b-116">예제 2: 스크립트 매개 변수를 사용하여 작업 제출</span><span class="sxs-lookup"><span data-stu-id="7e10b-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="7e10b-117">U-SQL 스크립트 매개 변수는 기본 스크립트 내용 위에 추가됩니다(예: DECLARE @Department 문자열 = "판매"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="7e10b-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="7e10b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e10b-118">PARAMETERS</span></span>

### <span data-ttu-id="7e10b-119">-Account</span><span class="sxs-lookup"><span data-stu-id="7e10b-119">-Account</span></span>
<span data-ttu-id="7e10b-120">작업이 제출될 Data Lake Analytics 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="7e10b-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="7e10b-121">-AnalyticsUnits</span></span>
<span data-ttu-id="7e10b-122">이 작업에서 사용할 분석 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-122">The analytics units to use for this job.</span></span> <span data-ttu-id="7e10b-123">일반적으로 스크립트 전용의 분석 단위가 1개 더 수록 스크립트 실행 시간이 빨라집니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="7e10b-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="7e10b-124">-CompileMode</span></span>
<span data-ttu-id="7e10b-125">이 작업에서 수행될 컴파일의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="7e10b-126">유효한 값:</span><span class="sxs-lookup"><span data-stu-id="7e10b-126">Valid values:</span></span> 
- <span data-ttu-id="7e10b-127">Semantic(유의적 검사 및 필요한 모든성 검사만 수행)</span><span class="sxs-lookup"><span data-stu-id="7e10b-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="7e10b-128">전체(전체 컴파일)</span><span class="sxs-lookup"><span data-stu-id="7e10b-128">Full (Full compilation)</span></span>
- <span data-ttu-id="7e10b-129">SingleBox(로컬로 수행되는 전체 컴파일)</span><span class="sxs-lookup"><span data-stu-id="7e10b-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="7e10b-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="7e10b-130">-CompileOnly</span></span>
<span data-ttu-id="7e10b-131">제출이 작업을 빌드하고 true로 설정된 경우 실행하지 말아야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="7e10b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e10b-132">-DefaultProfile</span></span>
<span data-ttu-id="7e10b-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7e10b-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e10b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7e10b-134">-Name</span></span>
<span data-ttu-id="7e10b-135">제출할 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="7e10b-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="7e10b-136">-PipelineId</span></span>
<span data-ttu-id="7e10b-137">이 작업의 제출을 나타내는 ID는 작업 파이프라인과 연결된 재발 작업 집합의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="7e10b-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="7e10b-138">-PipelineName</span></span>
<span data-ttu-id="7e10b-139">이 작업과 연결된 파이프라인에 대한 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="7e10b-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="7e10b-140">-PipelineUri</span></span>
<span data-ttu-id="7e10b-141">이 파이프라인과 연결된 원래 서비스에 연결되는 선택적 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="7e10b-142">-Priority</span><span class="sxs-lookup"><span data-stu-id="7e10b-142">-Priority</span></span>
<span data-ttu-id="7e10b-143">작업의 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-143">The priority of the job.</span></span> <span data-ttu-id="7e10b-144">지정하지 않으면 우선 순위는 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="7e10b-145">숫자가 낮을수록 작업 우선 순위가 높을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="7e10b-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="7e10b-146">-RecurrenceId</span></span>
<span data-ttu-id="7e10b-147">이 작업의 제출을 나타내는 ID는 동일한 recurrence ID가 있는 재발 작업 집합의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="7e10b-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="7e10b-148">-RecurrenceName</span></span>
<span data-ttu-id="7e10b-149">작업 간의 재발 상관 관계에 대한 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="7e10b-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="7e10b-150">-RunId</span></span>
<span data-ttu-id="7e10b-151">파이프라인의 이 특정 실행을 식별하는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="7e10b-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="7e10b-152">-Runtime</span></span>
<span data-ttu-id="7e10b-153">선택적으로 작업에서 사용할 런타임 버전을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="7e10b-154">설정하지 않은 경우 기본 런타임이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="7e10b-155">-Script</span><span class="sxs-lookup"><span data-stu-id="7e10b-155">-Script</span></span>
<span data-ttu-id="7e10b-156">실행할 스크립트(인라인으로 작성).</span><span class="sxs-lookup"><span data-stu-id="7e10b-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="7e10b-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="7e10b-157">-ScriptParameter</span></span>
<span data-ttu-id="7e10b-158">이 작업의 스크립트 매개 변수 매개 변수는 값(byte, sbyte, int, uint(또는 uint32) 조합), long, ulong(또는 uint64), float, double, decimal, short(또는 int16), ushort(또는 uint16), char, string, DateTime, bool, Guid 또는 byte[]의 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="7e10b-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="7e10b-159">-ScriptPath</span></span>
<span data-ttu-id="7e10b-160">제출할 스크립트 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="7e10b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e10b-161">CommonParameters</span></span>
<span data-ttu-id="7e10b-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e10b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e10b-163">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7e10b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e10b-164">입력</span><span class="sxs-lookup"><span data-stu-id="7e10b-164">INPUTS</span></span>

### <span data-ttu-id="7e10b-165">System.String</span><span class="sxs-lookup"><span data-stu-id="7e10b-165">System.String</span></span>

### <span data-ttu-id="7e10b-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e10b-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7e10b-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7e10b-167">System.Int32</span></span>

### <span data-ttu-id="7e10b-168">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="7e10b-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="7e10b-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7e10b-169">System.Guid</span></span>

### <span data-ttu-id="7e10b-170">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7e10b-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7e10b-171">출력</span><span class="sxs-lookup"><span data-stu-id="7e10b-171">OUTPUTS</span></span>

### <span data-ttu-id="7e10b-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="7e10b-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="7e10b-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e10b-173">NOTES</span></span>

## <span data-ttu-id="7e10b-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e10b-174">RELATED LINKS</span></span>

[<span data-ttu-id="7e10b-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e10b-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="7e10b-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e10b-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="7e10b-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e10b-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


