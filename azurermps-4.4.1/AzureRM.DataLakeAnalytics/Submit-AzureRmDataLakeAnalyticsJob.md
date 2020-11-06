---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532304"
---
# <span data-ttu-id="4f10e-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f10e-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="4f10e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f10e-102">SYNOPSIS</span></span>
<span data-ttu-id="4f10e-103">작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f10e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f10e-104">SYNTAX</span></span>

### <span data-ttu-id="4f10e-105">U-SQL 용 스크립트 경로를 사용 하 여 작업 제출</span><span class="sxs-lookup"><span data-stu-id="4f10e-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f10e-106">제출 U-SQL 작업</span><span class="sxs-lookup"><span data-stu-id="4f10e-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f10e-107">스크립트 경로를 사용 하 여 U-SQL에 대 한 자세한 정보를 포함 한 작업 제출</span><span class="sxs-lookup"><span data-stu-id="4f10e-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f10e-108">되풀이 정보가 포함 된 U-SQL 작업 제출</span><span class="sxs-lookup"><span data-stu-id="4f10e-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f10e-109">U-SQL에 대 한 스크립트 경로를 사용 하 여 작업 제출 및 파이프라인 정보</span><span class="sxs-lookup"><span data-stu-id="4f10e-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f10e-110">되풀이 및 파이프라인 정보가 포함 된 U-SQL 작업 제출</span><span class="sxs-lookup"><span data-stu-id="4f10e-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f10e-111">설명은</span><span class="sxs-lookup"><span data-stu-id="4f10e-111">DESCRIPTION</span></span>
<span data-ttu-id="4f10e-112">**AzureRmDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake Analytics 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="4f10e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4f10e-113">EXAMPLES</span></span>

### <span data-ttu-id="4f10e-114">예제 1: 작업 제출</span><span class="sxs-lookup"><span data-stu-id="4f10e-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="4f10e-115">이 명령은 Data Lake Analytics 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="4f10e-116">변수</span><span class="sxs-lookup"><span data-stu-id="4f10e-116">PARAMETERS</span></span>

### <span data-ttu-id="4f10e-117">-계정</span><span class="sxs-lookup"><span data-stu-id="4f10e-117">-Account</span></span>
<span data-ttu-id="4f10e-118">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4f10e-119">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="4f10e-119">-CompileMode</span></span>
<span data-ttu-id="4f10e-120">작업의 컴파일 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="4f10e-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f10e-122">의미 체계</span><span class="sxs-lookup"><span data-stu-id="4f10e-122">Semantic</span></span>
- <span data-ttu-id="4f10e-123">수준의</span><span class="sxs-lookup"><span data-stu-id="4f10e-123">Full</span></span>
- <span data-ttu-id="4f10e-124">SingleBox</span><span class="sxs-lookup"><span data-stu-id="4f10e-124">SingleBox</span></span>

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

### <span data-ttu-id="4f10e-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="4f10e-125">-CompileOnly</span></span>
<span data-ttu-id="4f10e-126">이 cmdlet이 작업을 실행 하지 않고 컴파일 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-126">Indicates that this cmdlet compiles the job without running it.</span></span>

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

### <span data-ttu-id="4f10e-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="4f10e-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="4f10e-128">작업의 허용 가능한 최대 병렬 처리를 나타내는 작업의 데이터 호수 분석 단위 (DLAU)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-129">-이름</span><span class="sxs-lookup"><span data-stu-id="4f10e-129">-Name</span></span>
<span data-ttu-id="4f10e-130">작업 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="4f10e-131">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="4f10e-131">-PipelineId</span></span>
<span data-ttu-id="4f10e-132">이 작업의 제출을 나타내는 ID는 되풀이 작업 집합의 일부 이며 작업 파이프라인에도 연결 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-133">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4f10e-133">-PipelineName</span></span>
<span data-ttu-id="4f10e-134">이 작업과 연결 된 파이프라인에 대 한 선택적 친근 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="4f10e-135">-PipelineUri</span></span>
<span data-ttu-id="4f10e-136">이 파이프라인과 연결 된 원래 서비스에 연결 하는 선택적 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-137">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="4f10e-137">-Priority</span></span>
<span data-ttu-id="4f10e-138">작업의 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="4f10e-139">지정 하지 않은 경우 우선 순위는 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="4f10e-140">숫자가 작으면 높은 작업 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-140">A low number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="4f10e-141">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="4f10e-141">-RecurrenceId</span></span>
<span data-ttu-id="4f10e-142">이 작업의 제출을 나타내는 ID는 동일한 되풀이 ID를 사용 하는 되풀이 작업 집합의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-143">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="4f10e-143">-RecurrenceName</span></span>
<span data-ttu-id="4f10e-144">작업 간의 되풀이 상관 관계에 대 한 선택적 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="4f10e-145">-RunId</span></span>
<span data-ttu-id="4f10e-146">파이프라인의 특정 실행 반복을 식별 하는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-147">런타임</span><span class="sxs-lookup"><span data-stu-id="4f10e-147">-Runtime</span></span>
<span data-ttu-id="4f10e-148">작업의 런타임 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-148">Specifies the runtime version of the job.</span></span>

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

### <span data-ttu-id="4f10e-149">-스크립트</span><span class="sxs-lookup"><span data-stu-id="4f10e-149">-Script</span></span>
<span data-ttu-id="4f10e-150">실행할 스크립트의 내용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="4f10e-151">-ScriptPath</span></span>
<span data-ttu-id="4f10e-152">실행할 스크립트의 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f10e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f10e-153">-DefaultProfile</span></span>
<span data-ttu-id="4f10e-154">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f10e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f10e-155">CommonParameters</span></span>
<span data-ttu-id="4f10e-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f10e-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f10e-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f10e-158">입력</span><span class="sxs-lookup"><span data-stu-id="4f10e-158">INPUTS</span></span>

### <span data-ttu-id="4f10e-159">이름</span><span class="sxs-lookup"><span data-stu-id="4f10e-159">String</span></span>
<span data-ttu-id="4f10e-160">' Script ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4f10e-161">출력</span><span class="sxs-lookup"><span data-stu-id="4f10e-161">OUTPUTS</span></span>

### <span data-ttu-id="4f10e-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="4f10e-162">JobInformation</span></span>
<span data-ttu-id="4f10e-163">제출 된 작업에 대 한 초기 작업 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="4f10e-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="4f10e-164">상속자</span><span class="sxs-lookup"><span data-stu-id="4f10e-164">NOTES</span></span>

## <span data-ttu-id="4f10e-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f10e-165">RELATED LINKS</span></span>

[<span data-ttu-id="4f10e-166">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f10e-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4f10e-167">중지-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f10e-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="4f10e-168">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4f10e-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


