---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045915"
---
# <span data-ttu-id="dd960-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="dd960-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="dd960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd960-102">SYNOPSIS</span></span>
<span data-ttu-id="dd960-103">새 Sqoop 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="dd960-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd960-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dd960-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dd960-105">DESCRIPTION</span></span>
<span data-ttu-id="dd960-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="dd960-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="dd960-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="dd960-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="dd960-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="dd960-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="dd960-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="dd960-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="dd960-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dd960-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="dd960-112">**AzureHDInsightSqoopJobDefinition** Cmdlet은 Azure HDInsight 클러스터에서 실행할 sqoop 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="dd960-113">Sqoop는 Hadoop 클러스터와 관계형 데이터베이스 간에 데이터를 전송 하는 도구입니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="dd960-114">Sqoop를 사용 하 여 SQL Server 데이터베이스에서 Hadoop 분산 파일 시스템 (HDFS)으로 데이터를 가져오고, 데이터를 Hadoop MapReduce로 변환한 다음, HDFS의 데이터를 다시 SQL Server 데이터베이스에 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="dd960-115">예제의</span><span class="sxs-lookup"><span data-stu-id="dd960-115">EXAMPLES</span></span>

### <span data-ttu-id="dd960-116">예제 1: 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="dd960-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="dd960-117">이 명령은 AzureSQL Server 데이터베이스에서 HDInsight 클러스터로 테이블의 모든 행을 가져온 다음, 작업 정의를 $SqoopJobDef 변수에 저장 하는 Sqoop 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="dd960-118">변수</span><span class="sxs-lookup"><span data-stu-id="dd960-118">PARAMETERS</span></span>

### <span data-ttu-id="dd960-119">-명령</span><span class="sxs-lookup"><span data-stu-id="dd960-119">-Command</span></span>
<span data-ttu-id="dd960-120">Sqoop 명령 및 해당 인수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-120">Specifies a Sqoop command and its arguments.</span></span>

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

### <span data-ttu-id="dd960-121">-파일</span><span class="sxs-lookup"><span data-stu-id="dd960-121">-File</span></span>
<span data-ttu-id="dd960-122">실행할 명령이 포함 된 스크립트 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="dd960-123">스크립트 파일은 WASB에 위치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-123">The script file must be located on WASB.</span></span>

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

### <span data-ttu-id="dd960-124">-파일</span><span class="sxs-lookup"><span data-stu-id="dd960-124">-Files</span></span>
<span data-ttu-id="dd960-125">작업에 필요한 WASB 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-125">Specifies the collection of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="dd960-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="dd960-126">-Profile</span></span>
<span data-ttu-id="dd960-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd960-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd960-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="dd960-129">-StatusFolder</span></span>
<span data-ttu-id="dd960-130">종료 코드와 작업 로그를 포함 하 여 작업에 대 한 표준 출력과 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="dd960-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd960-131">CommonParameters</span></span>
<span data-ttu-id="dd960-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd960-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd960-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd960-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd960-134">입력</span><span class="sxs-lookup"><span data-stu-id="dd960-134">INPUTS</span></span>

## <span data-ttu-id="dd960-135">출력</span><span class="sxs-lookup"><span data-stu-id="dd960-135">OUTPUTS</span></span>

## <span data-ttu-id="dd960-136">상속자</span><span class="sxs-lookup"><span data-stu-id="dd960-136">NOTES</span></span>

## <span data-ttu-id="dd960-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd960-137">RELATED LINKS</span></span>

[<span data-ttu-id="dd960-138">새로운 AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="dd960-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="dd960-139">새로운 AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="dd960-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="dd960-140">새로운 AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="dd960-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="dd960-141">새로운 AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="dd960-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


