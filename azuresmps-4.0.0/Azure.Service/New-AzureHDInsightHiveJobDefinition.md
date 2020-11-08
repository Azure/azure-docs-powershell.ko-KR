---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045917"
---
# <span data-ttu-id="30176-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="30176-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="30176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30176-102">SYNOPSIS</span></span>
<span data-ttu-id="30176-103">HDInsight 서비스에 대 한 새 하이브 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="30176-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30176-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30176-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30176-105">DESCRIPTION</span></span>
<span data-ttu-id="30176-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30176-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="30176-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30176-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="30176-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="30176-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="30176-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="30176-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="30176-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="30176-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="30176-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="30176-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="30176-112">**AzureHDInsightHiveJobDefinition** Cmdlet은 Azure HDInsight 서비스에 대 한 하이브 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="30176-113">예제의</span><span class="sxs-lookup"><span data-stu-id="30176-113">EXAMPLES</span></span>

### <span data-ttu-id="30176-114">예제 1: 하이브 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="30176-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="30176-115">이 명령은 미리 정의 된 쿼리 문자열을 사용 하는 Hive 작업 정의를 만든 다음 $HiveJobDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="30176-116">변수</span><span class="sxs-lookup"><span data-stu-id="30176-116">PARAMETERS</span></span>

### <span data-ttu-id="30176-117">-인수</span><span class="sxs-lookup"><span data-stu-id="30176-117">-Arguments</span></span>
<span data-ttu-id="30176-118">Hadoop 작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="30176-119">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="30176-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="30176-120">-정의</span><span class="sxs-lookup"><span data-stu-id="30176-120">-Defines</span></span>
<span data-ttu-id="30176-121">작업이 실행 될 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

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

### <span data-ttu-id="30176-122">-파일</span><span class="sxs-lookup"><span data-stu-id="30176-122">-File</span></span>
<span data-ttu-id="30176-123">실행할 쿼리를 포함 하는 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="30176-124">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30176-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="30176-125">-파일</span><span class="sxs-lookup"><span data-stu-id="30176-125">-Files</span></span>
<span data-ttu-id="30176-126">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="30176-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="30176-127">-JobName</span></span>
<span data-ttu-id="30176-128">정의할 하이브 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="30176-129">이 매개 변수를 지정 하지 않으면 기본 이름인 "Hive:"가 사용 됩니다. \<first 100 characters of query\></span><span class="sxs-lookup"><span data-stu-id="30176-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

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

### <span data-ttu-id="30176-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="30176-130">-Profile</span></span>
<span data-ttu-id="30176-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30176-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="30176-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30176-133">-쿼리</span><span class="sxs-lookup"><span data-stu-id="30176-133">-Query</span></span>
<span data-ttu-id="30176-134">하이브 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-134">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="30176-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="30176-135">-RunAsFileJob</span></span>
<span data-ttu-id="30176-136">이 cmdlet이 쿼리를 저장할 기본 Azure 저장소 계정에 파일을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="30176-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="30176-137">이 cmdlet은이 파일을 참조 하는 작업을 실행 하도록 스크립트로 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="30176-138">이 기능을 사용 하 여 백분율 기호 (%) 등의 특수 문자를 처리할 수 있습니다. Templeton는 URL 매개 변수로 백분율 기호가 있는 쿼리를 해석 하기 때문에 Templeton를 통한 작업 제출에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30176-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="30176-139">-StatusFolder</span></span>
<span data-ttu-id="30176-140">종료 코드와 작업 로그를 포함 하 여 작업에 대 한 표준 출력과 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="30176-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30176-141">CommonParameters</span></span>
<span data-ttu-id="30176-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30176-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30176-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30176-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30176-144">입력</span><span class="sxs-lookup"><span data-stu-id="30176-144">INPUTS</span></span>

## <span data-ttu-id="30176-145">출력</span><span class="sxs-lookup"><span data-stu-id="30176-145">OUTPUTS</span></span>

## <span data-ttu-id="30176-146">상속자</span><span class="sxs-lookup"><span data-stu-id="30176-146">NOTES</span></span>

## <span data-ttu-id="30176-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30176-147">RELATED LINKS</span></span>

[<span data-ttu-id="30176-148">새로운 AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="30176-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="30176-149">새로운 AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="30176-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="30176-150">새로운 AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="30176-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="30176-151">새로운 AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="30176-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


