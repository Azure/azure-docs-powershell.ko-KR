---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046248"
---
# <span data-ttu-id="f4f24-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="f4f24-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="f4f24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f24-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f24-103">HDInsight 클러스터에 하이브 쿼리를 제출 하 고 쿼리 실행의 진행률을 표시 하 고 한 번의 작업으로 쿼리 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="f4f24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4f24-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4f24-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f4f24-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f24-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f4f24-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f4f24-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4f24-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f4f24-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f4f24-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f4f24-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f4f24-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f4f24-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f4f24-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f4f24-112">**AzureHDInsightHiveJob** Cmdlet은 HDInsight 클러스터에 하이브 쿼리를 제출 하 고 쿼리 실행의 진행률을 표시 하 고 한 번의 작업으로 쿼리 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="f4f24-113">**AzureHDInsightHiveJob** 를 실행 하기 전에 Use-AzureHDInsightCluster cmdlet을 실행 하 여 쿼리를 제출할 HDInsight 클러스터를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="f4f24-114">예제의</span><span class="sxs-lookup"><span data-stu-id="f4f24-114">EXAMPLES</span></span>

### <span data-ttu-id="f4f24-115">예제 1: 하이브 쿼리 제출</span><span class="sxs-lookup"><span data-stu-id="f4f24-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="f4f24-116">첫 번째 명령은 **AzureHDInsightCluster** cmdlet을 사용 하 여 현재 구독에서 하이브 쿼리에 사용할 클러스터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="f4f24-117">두 번째 명령은 **AzureHDInsightHiveJob** cmdlet을 사용 하 여 Hive 쿼리를 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="f4f24-118">변수</span><span class="sxs-lookup"><span data-stu-id="f4f24-118">PARAMETERS</span></span>

### <span data-ttu-id="f4f24-119">-인수</span><span class="sxs-lookup"><span data-stu-id="f4f24-119">-Arguments</span></span>
<span data-ttu-id="f4f24-120">Hadoop 작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="f4f24-121">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="f4f24-122">-정의</span><span class="sxs-lookup"><span data-stu-id="f4f24-122">-Defines</span></span>
<span data-ttu-id="f4f24-123">작업을 실행할 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="f4f24-124">-파일</span><span class="sxs-lookup"><span data-stu-id="f4f24-124">-File</span></span>
<span data-ttu-id="f4f24-125">실행할 쿼리를 포함 하는 Azure Blob Storage의 파일에 대 한 WASB (Windows Azure Storage Blob) 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="f4f24-126">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-126">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="f4f24-127">-파일</span><span class="sxs-lookup"><span data-stu-id="f4f24-127">-Files</span></span>
<span data-ttu-id="f4f24-128">하이브 작업에 필요한 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-128">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="f4f24-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="f4f24-129">-JobName</span></span>
<span data-ttu-id="f4f24-130">하이브 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="f4f24-131">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본값 "Hive:"를 사용 합니다. \<first 100 characters of Query\></span><span class="sxs-lookup"><span data-stu-id="f4f24-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="f4f24-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="f4f24-132">-Profile</span></span>
<span data-ttu-id="f4f24-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4f24-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4f24-135">-쿼리</span><span class="sxs-lookup"><span data-stu-id="f4f24-135">-Query</span></span>
<span data-ttu-id="f4f24-136">하이브 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-136">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="f4f24-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="f4f24-137">-RunAsFileJob</span></span>
<span data-ttu-id="f4f24-138">이 cmdlet이 쿼리를 저장할 기본 Azure 저장소 계정에 파일을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="f4f24-139">이 cmdlet은이 파일을 참조 하는 작업을 실행 하도록 스크립트로 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="f4f24-140">이 기능을 사용 하 여 백분율 기호 (%) 등의 특수 문자를 처리할 수 있습니다. Templeton는 URL 매개 변수로 백분율 기호가 있는 쿼리를 해석 하기 때문에 Templeton를 통한 작업 제출에 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="f4f24-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f4f24-141">-StatusFolder</span></span>
<span data-ttu-id="f4f24-142">종료 코드와 작업 로그를 포함 하 여 작업에 대 한 표준 출력과 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="f4f24-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f24-143">CommonParameters</span></span>
<span data-ttu-id="f4f24-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4f24-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f24-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f24-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f24-146">입력</span><span class="sxs-lookup"><span data-stu-id="f4f24-146">INPUTS</span></span>

## <span data-ttu-id="f4f24-147">출력</span><span class="sxs-lookup"><span data-stu-id="f4f24-147">OUTPUTS</span></span>

## <span data-ttu-id="f4f24-148">상속자</span><span class="sxs-lookup"><span data-stu-id="f4f24-148">NOTES</span></span>

## <span data-ttu-id="f4f24-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4f24-149">RELATED LINKS</span></span>

[<span data-ttu-id="f4f24-150">새로운 AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f4f24-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f4f24-151">-AzureHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="f4f24-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


