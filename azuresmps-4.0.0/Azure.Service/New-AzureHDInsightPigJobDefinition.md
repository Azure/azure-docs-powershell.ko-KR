---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046010"
---
# <span data-ttu-id="89d3e-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="89d3e-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="89d3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="89d3e-103">HDInsight 서비스에 대 한 새 문 돼지 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="89d3e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89d3e-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89d3e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89d3e-105">DESCRIPTION</span></span>
<span data-ttu-id="89d3e-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="89d3e-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="89d3e-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="89d3e-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="89d3e-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="89d3e-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="89d3e-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="89d3e-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="89d3e-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="89d3e-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="89d3e-112">**AzureHDInsightPigJobDefinition** 는 Azure HDInsight 서비스에 대 한 문 돼지 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="89d3e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="89d3e-113">EXAMPLES</span></span>

### <span data-ttu-id="89d3e-114">예제 1: 새 문 돼지 작업 정의</span><span class="sxs-lookup"><span data-stu-id="89d3e-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="89d3e-115">첫 번째 명령은 문자열 값을 선언한 다음 $0 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="89d3e-116">두 번째 명령은 문 돼지 작업 쿼리를 만든 다음이를 $QueryString 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="89d3e-117">마지막 명령은 $QueryString에서 쿼리를 사용 하는 문 돼지 작업 정의를 만든 다음, 작업 정의를 $PigJobDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="89d3e-118">변수</span><span class="sxs-lookup"><span data-stu-id="89d3e-118">PARAMETERS</span></span>

### <span data-ttu-id="89d3e-119">-인수</span><span class="sxs-lookup"><span data-stu-id="89d3e-119">-Arguments</span></span>
<span data-ttu-id="89d3e-120">문 돼지 작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="89d3e-121">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="89d3e-122">-파일</span><span class="sxs-lookup"><span data-stu-id="89d3e-122">-File</span></span>
<span data-ttu-id="89d3e-123">실행할 쿼리를 포함 하는 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="89d3e-124">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-124">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d3e-125">-파일</span><span class="sxs-lookup"><span data-stu-id="89d3e-125">-Files</span></span>
<span data-ttu-id="89d3e-126">문 돼지 작업에 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="89d3e-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="89d3e-127">-Profile</span></span>
<span data-ttu-id="89d3e-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89d3e-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89d3e-130">-쿼리</span><span class="sxs-lookup"><span data-stu-id="89d3e-130">-Query</span></span>
<span data-ttu-id="89d3e-131">문 돼지 작업 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-131">Specifies a Pig job query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d3e-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="89d3e-132">-StatusFolder</span></span>
<span data-ttu-id="89d3e-133">종료 코드와 작업 로그를 포함 하 여 작업에 대 한 표준 출력과 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="89d3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d3e-134">CommonParameters</span></span>
<span data-ttu-id="89d3e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89d3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d3e-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d3e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d3e-137">입력</span><span class="sxs-lookup"><span data-stu-id="89d3e-137">INPUTS</span></span>

## <span data-ttu-id="89d3e-138">출력</span><span class="sxs-lookup"><span data-stu-id="89d3e-138">OUTPUTS</span></span>

## <span data-ttu-id="89d3e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="89d3e-139">NOTES</span></span>

## <span data-ttu-id="89d3e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89d3e-140">RELATED LINKS</span></span>

[<span data-ttu-id="89d3e-141">새로운 AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="89d3e-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="89d3e-142">새로운 AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="89d3e-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="89d3e-143">새로운 AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="89d3e-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="89d3e-144">새로운 AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="89d3e-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


