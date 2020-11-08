---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045424"
---
# <span data-ttu-id="ebcf4-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ebcf4-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="ebcf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebcf4-102">SYNOPSIS</span></span>
<span data-ttu-id="ebcf4-103">HDInsight 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="ebcf4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebcf4-104">SYNTAX</span></span>

### <span data-ttu-id="ebcf4-105">HDInsight 클러스터에서 jobDetails 시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ebcf4-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ebcf4-106">HDInsight 클러스터 (특정 구독 자격 증명 포함)에서 jobDetails 시작</span><span class="sxs-lookup"><span data-stu-id="ebcf4-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ebcf4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ebcf4-107">DESCRIPTION</span></span>
<span data-ttu-id="ebcf4-108">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ebcf4-109">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ebcf4-110">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ebcf4-111">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ebcf4-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ebcf4-112">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ebcf4-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ebcf4-113">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ebcf4-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ebcf4-114">**AzureHDInsightJob** cmdlet은 지정 된 클러스터에서 정의 된 Azure HDInsight 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="ebcf4-115">시작할 작업은 MapReduce job, 스트리밍 작업, 하이브 작업 또는 문 돼지 job 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="ebcf4-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ebcf4-116">EXAMPLES</span></span>

### <span data-ttu-id="ebcf4-117">예제 1: HDInsight 작업 시작</span><span class="sxs-lookup"><span data-stu-id="ebcf4-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="ebcf4-118">첫 번째 명령은 현재 구독 ID를 가져온 다음 $SubId 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="ebcf4-119">두 번째 명령은 $ClusterName 변수에 이름 Cluster01를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="ebcf4-120">세 번째 명령은 **새 AzureHDInsightMapReduceJobDefinition** cmdlet을 사용 하 여 MapReduce 작업 정의를 만든 다음이를 $WordCountJob 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="ebcf4-121">마지막 명령은 파이프라인 연산자를 사용 하 여 $WordCountJob를 **시작 AzureHDInsightJob** cmdlet에 전달 하 여 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="ebcf4-122">작업이 시작 되 면 **AzureHDInsightJob** cmdlet에 전달 되어 작업 출력을 가져오기 위해 작업을 **get-AzureHDInsightJobOutput** cmdlet에 전달 하기 전에 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="ebcf4-123">변수</span><span class="sxs-lookup"><span data-stu-id="ebcf4-123">PARAMETERS</span></span>

### <span data-ttu-id="ebcf4-124">-인증서</span><span class="sxs-lookup"><span data-stu-id="ebcf4-124">-Certificate</span></span>
<span data-ttu-id="ebcf4-125">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcf4-126">-클러스터</span><span class="sxs-lookup"><span data-stu-id="ebcf4-126">-Cluster</span></span>
<span data-ttu-id="ebcf4-127">클러스터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-127">Specifies a cluster.</span></span>
<span data-ttu-id="ebcf4-128">이 cmdlet은이 매개 변수에서 지정 하는 클러스터의 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebcf4-129">-Credential</span><span class="sxs-lookup"><span data-stu-id="ebcf4-129">-Credential</span></span>
<span data-ttu-id="ebcf4-130">클러스터에 대 한 직접 HTTP 액세스에 대 한 클러스터 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="ebcf4-131">*구독* 매개 변수 대신이 매개 변수를 지정 하 여 클러스터에 대 한 액세스를 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcf4-132">-끝점</span><span class="sxs-lookup"><span data-stu-id="ebcf4-132">-Endpoint</span></span>
<span data-ttu-id="ebcf4-133">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ebcf4-134">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcf4-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ebcf4-135">-HostedService</span></span>
<span data-ttu-id="ebcf4-136">기본 네임 스페이스를 사용 하지 않으려는 경우 HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcf4-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ebcf4-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="ebcf4-138">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcf4-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="ebcf4-139">-JobDefinition</span></span>
<span data-ttu-id="ebcf4-140">끝점이 기본값과 다른 경우 Microsoft Azure에 연결할 때 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebcf4-141">-프로필</span><span class="sxs-lookup"><span data-stu-id="ebcf4-141">-Profile</span></span>
<span data-ttu-id="ebcf4-142">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ebcf4-143">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ebcf4-144">-구독</span><span class="sxs-lookup"><span data-stu-id="ebcf4-144">-Subscription</span></span>
<span data-ttu-id="ebcf4-145">구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-145">Specifies a subscription.</span></span>
<span data-ttu-id="ebcf4-146">이 cmdlet은이 매개 변수에서 지정 하는 구독에 대 한 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebcf4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebcf4-147">CommonParameters</span></span>
<span data-ttu-id="ebcf4-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebcf4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebcf4-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebcf4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebcf4-150">입력</span><span class="sxs-lookup"><span data-stu-id="ebcf4-150">INPUTS</span></span>

## <span data-ttu-id="ebcf4-151">출력</span><span class="sxs-lookup"><span data-stu-id="ebcf4-151">OUTPUTS</span></span>

## <span data-ttu-id="ebcf4-152">상속자</span><span class="sxs-lookup"><span data-stu-id="ebcf4-152">NOTES</span></span>

## <span data-ttu-id="ebcf4-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebcf4-153">RELATED LINKS</span></span>

[<span data-ttu-id="ebcf4-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ebcf4-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="ebcf4-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="ebcf4-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="ebcf4-156">새로운 AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ebcf4-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="ebcf4-157">중지-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ebcf4-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="ebcf4-158">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ebcf4-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


