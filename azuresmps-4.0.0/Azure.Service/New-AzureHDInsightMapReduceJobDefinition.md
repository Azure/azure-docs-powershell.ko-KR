---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045916"
---
# <span data-ttu-id="e4394-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e4394-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="e4394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4394-102">SYNOPSIS</span></span>
<span data-ttu-id="e4394-103">새 MapReduce 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="e4394-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4394-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4394-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e4394-105">DESCRIPTION</span></span>
<span data-ttu-id="e4394-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e4394-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e4394-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4394-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e4394-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e4394-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e4394-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e4394-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e4394-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e4394-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e4394-112">**AzureHDInsightMapReduceJobDefinition** cmdlet은 새 MapReduce 작업을 정의 하 여 Azure HDInsight 클러스터에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e4394-113">예제의</span><span class="sxs-lookup"><span data-stu-id="e4394-113">EXAMPLES</span></span>

### <span data-ttu-id="e4394-114">예제 1: MapReduce 작업 정의, 작업 실행 및 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="e4394-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="e4394-115">첫 번째 명령은 현재 구독의 ID를 가져온 다음 $SubId 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="e4394-116">두 번째 명령은 $Clustername 변수에 이름 MyCluster를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="e4394-117">세 번째 명령은 **새 AzureHDInsightMapReduceJobDefinition** cmdlet을 사용 하 여 MapReduce 작업 정의를 만든 다음이를 $WordCountJob 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="e4394-118">네 번째 명령은 다음 cmdlet을 사용 하 여 일련의 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="e4394-119">$ClusterName에서 작업을 시작 하려면 **-AzureHDInsightJob** 을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="e4394-120">**Wait-AzureHDInsightJob** 작업이 완료 될 때까지 기다리거나 완료 진행률을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="e4394-121">작업 출력을 가져오는 **AzureHDInsightJobOutput** .</span><span class="sxs-lookup"><span data-stu-id="e4394-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="e4394-122">변수</span><span class="sxs-lookup"><span data-stu-id="e4394-122">PARAMETERS</span></span>

### <span data-ttu-id="e4394-123">-인수</span><span class="sxs-lookup"><span data-stu-id="e4394-123">-Arguments</span></span>
<span data-ttu-id="e4394-124">Hadoop 작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="e4394-125">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e4394-126">-ClassName</span><span class="sxs-lookup"><span data-stu-id="e4394-126">-ClassName</span></span>
<span data-ttu-id="e4394-127">"JAR (Java Archive)" 파일에서 작업 클래스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4394-128">-정의</span><span class="sxs-lookup"><span data-stu-id="e4394-128">-Defines</span></span>
<span data-ttu-id="e4394-129">작업을 실행할 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="e4394-130">-파일</span><span class="sxs-lookup"><span data-stu-id="e4394-130">-Files</span></span>
<span data-ttu-id="e4394-131">작업에 필요한 WASB 파일 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="e4394-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="e4394-132">-JarFile</span></span>
<span data-ttu-id="e4394-133">MapReduce 작업의 코드 및 종속성을 포함 하는 JAR 파일의 정규화 된 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4394-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="e4394-134">-JobName</span></span>
<span data-ttu-id="e4394-135">MapReduce 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="e4394-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-136">This parameter is optional.</span></span>
<span data-ttu-id="e4394-137">이 매개 변수를 지정 하지 않으면 *ClassName* 매개 변수의 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="e4394-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="e4394-138">-LibJars</span></span>
<span data-ttu-id="e4394-139">작업에 대 한 참조 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="e4394-140">-프로필</span><span class="sxs-lookup"><span data-stu-id="e4394-140">-Profile</span></span>
<span data-ttu-id="e4394-141">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4394-142">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4394-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e4394-143">-StatusFolder</span></span>
<span data-ttu-id="e4394-144">종료 코드와 작업 로그를 포함 하 여 작업에 대 한 표준 출력과 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="e4394-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4394-145">CommonParameters</span></span>
<span data-ttu-id="e4394-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4394-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4394-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4394-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4394-148">입력</span><span class="sxs-lookup"><span data-stu-id="e4394-148">INPUTS</span></span>

## <span data-ttu-id="e4394-149">출력</span><span class="sxs-lookup"><span data-stu-id="e4394-149">OUTPUTS</span></span>

## <span data-ttu-id="e4394-150">상속자</span><span class="sxs-lookup"><span data-stu-id="e4394-150">NOTES</span></span>

## <span data-ttu-id="e4394-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4394-151">RELATED LINKS</span></span>

[<span data-ttu-id="e4394-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="e4394-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="e4394-153">새로운 AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e4394-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="e4394-154">새로운 AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e4394-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="e4394-155">새로운 AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e4394-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="e4394-156">시작-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e4394-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="e4394-157">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e4394-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


