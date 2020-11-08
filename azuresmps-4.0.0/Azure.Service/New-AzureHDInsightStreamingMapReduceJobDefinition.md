---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046009"
---
# <span data-ttu-id="430ad-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="430ad-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="430ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="430ad-102">SYNOPSIS</span></span>
<span data-ttu-id="430ad-103">새 스트리밍 MapReduce 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="430ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="430ad-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="430ad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="430ad-105">DESCRIPTION</span></span>
<span data-ttu-id="430ad-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="430ad-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="430ad-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="430ad-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="430ad-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="430ad-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="430ad-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="430ad-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="430ad-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="430ad-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="430ad-112">**새 AzureHDInsightStreamingMapReduceJobDefinition** Cmdlet은 Hadoop 스트리밍 작업의 매개 변수를 나타내는 새 작업 정의 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="430ad-113">예제의</span><span class="sxs-lookup"><span data-stu-id="430ad-113">EXAMPLES</span></span>

### <span data-ttu-id="430ad-114">예제 1: 스트리밍 MapReduce 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="430ad-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="430ad-115">이 명령은 지정 된 스트리밍 MapReduce 작업 정의를 만든 다음 $StreamingWordCount 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="430ad-116">변수</span><span class="sxs-lookup"><span data-stu-id="430ad-116">PARAMETERS</span></span>

### <span data-ttu-id="430ad-117">-인수</span><span class="sxs-lookup"><span data-stu-id="430ad-117">-Arguments</span></span>
<span data-ttu-id="430ad-118">Hadoop 작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="430ad-119">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="430ad-120">-CmdEnv</span></span>
<span data-ttu-id="430ad-121">데이터 노드에서 작업을 실행할 때 설정할 명령줄 환경 변수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-122">-Combiner</span><span class="sxs-lookup"><span data-stu-id="430ad-122">-Combiner</span></span>
<span data-ttu-id="430ad-123">Combiner 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-123">Specifies a Combiner file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-124">-정의</span><span class="sxs-lookup"><span data-stu-id="430ad-124">-Defines</span></span>
<span data-ttu-id="430ad-125">작업을 실행할 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-126">-파일</span><span class="sxs-lookup"><span data-stu-id="430ad-126">-Files</span></span>
<span data-ttu-id="430ad-127">작업에 필요한 파일 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="430ad-128">-InputPath</span></span>
<span data-ttu-id="430ad-129">입력 파일에 대 한 WASB 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="430ad-130">-JobName</span></span>
<span data-ttu-id="430ad-131">새 MapReduce 작업 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="430ad-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-133">-Mapper</span><span class="sxs-lookup"><span data-stu-id="430ad-133">-Mapper</span></span>
<span data-ttu-id="430ad-134">매퍼 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-134">Specifies a Mapper file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="430ad-135">-OutputPath</span></span>
<span data-ttu-id="430ad-136">작업 출력에 대 한 WASB 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-137">-프로필</span><span class="sxs-lookup"><span data-stu-id="430ad-137">-Profile</span></span>
<span data-ttu-id="430ad-138">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="430ad-139">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-140">-Reducer</span><span class="sxs-lookup"><span data-stu-id="430ad-140">-Reducer</span></span>
<span data-ttu-id="430ad-141">Reducer 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-141">Specifies a Reducer file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="430ad-142">-StatusFolder</span></span>
<span data-ttu-id="430ad-143">종료 코드와 작업 로그를 포함 하 여 작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430ad-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430ad-144">CommonParameters</span></span>
<span data-ttu-id="430ad-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="430ad-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430ad-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="430ad-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430ad-147">입력</span><span class="sxs-lookup"><span data-stu-id="430ad-147">INPUTS</span></span>

## <span data-ttu-id="430ad-148">출력</span><span class="sxs-lookup"><span data-stu-id="430ad-148">OUTPUTS</span></span>

## <span data-ttu-id="430ad-149">상속자</span><span class="sxs-lookup"><span data-stu-id="430ad-149">NOTES</span></span>

## <span data-ttu-id="430ad-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="430ad-150">RELATED LINKS</span></span>

[<span data-ttu-id="430ad-151">새로운 AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="430ad-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="430ad-152">새로운 AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="430ad-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="430ad-153">새로운 AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="430ad-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="430ad-154">새로운 AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="430ad-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


