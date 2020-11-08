---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045832"
---
# <span data-ttu-id="9930a-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9930a-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="9930a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9930a-102">SYNOPSIS</span></span>
<span data-ttu-id="9930a-103">HDInsight 작업의 완료 또는 실패를 세계가 귀하 하 고 작업 진행 상황을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="9930a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9930a-104">SYNTAX</span></span>

### <span data-ttu-id="9930a-105">HDInsight 클러스터의 jobDetails 기록 가져오기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9930a-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9930a-106">HDInsight 클러스터 (특정 구독 자격 증명 포함)의 jobDetails 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="9930a-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9930a-107">HDInsight 클러스터에서 JobId를 사용 하 여 작업 대기</span><span class="sxs-lookup"><span data-stu-id="9930a-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9930a-108">HDInsight 클러스터에서 작업을 사용 하 여 작업 대기</span><span class="sxs-lookup"><span data-stu-id="9930a-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9930a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9930a-109">DESCRIPTION</span></span>
<span data-ttu-id="9930a-110">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="9930a-111">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="9930a-112">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="9930a-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="9930a-113">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="9930a-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="9930a-114">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="9930a-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="9930a-115">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9930a-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="9930a-116">**AzureHDInsightJob** Cmdlet은 Azure HDInsight 작업의 완료 또는 실패를 세계가 귀하 하 고 작업의 진행률을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="9930a-117">예제의</span><span class="sxs-lookup"><span data-stu-id="9930a-117">EXAMPLES</span></span>

### <span data-ttu-id="9930a-118">예제 1: 작업 실행 및 완료 될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="9930a-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="9930a-119">첫 번째 명령은 현재 Azure 구독 ID를 가져온 다음 $SubId 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="9930a-120">두 번째 명령은 지정 된 클러스터를 가져온 다음 $ClusterName 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="9930a-121">세 번째 명령은 **새 AzureHDInsightMapReduceJobDefinition** cmdlet을 사용 하 여 MapReduce 작업 정의를 만든 다음이를 $WordCountJob 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="9930a-122">네 번째 명령은 여러 cmdlet을 순서 대로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="9930a-123">파이프라인 연산자를 사용 하 여 $WordCountJob를 **AzureHDInsightJob** cmdlet에 전달 하 여 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="9930a-124">작업이 완료 될 때까지 3600 초 동안 **AzureHDInsightJob** cmdlet에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="9930a-125">작업이 완료 되 면 명령에서 **AzureHDInsightJobOutput** cmdlet을 사용 하 여 작업 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="9930a-126">변수</span><span class="sxs-lookup"><span data-stu-id="9930a-126">PARAMETERS</span></span>

### <span data-ttu-id="9930a-127">-인증서</span><span class="sxs-lookup"><span data-stu-id="9930a-127">-Certificate</span></span>
<span data-ttu-id="9930a-128">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-129">-클러스터</span><span class="sxs-lookup"><span data-stu-id="9930a-129">-Cluster</span></span>
<span data-ttu-id="9930a-130">클러스터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-130">Specifies a cluster.</span></span>
<span data-ttu-id="9930a-131">이 cmdlet은이 매개 변수에서 지정 하는 클러스터에 대 한 작업을 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="9930a-132">-Credential</span></span>
<span data-ttu-id="9930a-133">클러스터에 대 한 직접 HTTP 액세스에 사용할 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="9930a-134">*구독* 매개 변수 대신이 매개 변수를 지정 하 여 클러스터에 대 한 액세스를 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-135">-끝점</span><span class="sxs-lookup"><span data-stu-id="9930a-135">-Endpoint</span></span>
<span data-ttu-id="9930a-136">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="9930a-137">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="9930a-138">-HostedService</span></span>
<span data-ttu-id="9930a-139">HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="9930a-140">이 매개 변수를 지정 하지 않으면 기본 네임 스페이스가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="9930a-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="9930a-142">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-143">-작업</span><span class="sxs-lookup"><span data-stu-id="9930a-143">-Job</span></span>
<span data-ttu-id="9930a-144">Azure HDInsight 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="9930a-145">-JobId</span></span>
<span data-ttu-id="9930a-146">대기할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-147">-프로필</span><span class="sxs-lookup"><span data-stu-id="9930a-147">-Profile</span></span>
<span data-ttu-id="9930a-148">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9930a-149">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9930a-150">-구독</span><span class="sxs-lookup"><span data-stu-id="9930a-150">-Subscription</span></span>
<span data-ttu-id="9930a-151">구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-151">Specifies a subscription.</span></span>
<span data-ttu-id="9930a-152">이 cmdlet은이 매개 변수에서 지정 하는 구독에 대 한 작업을 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="9930a-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="9930a-154">대기 작업의 제한 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="9930a-155">작업이 완료 되기 전에 시간 제한이 만료 되는 경우 cmdlet이 실행을 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9930a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9930a-156">CommonParameters</span></span>
<span data-ttu-id="9930a-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9930a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9930a-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9930a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9930a-159">입력</span><span class="sxs-lookup"><span data-stu-id="9930a-159">INPUTS</span></span>

## <span data-ttu-id="9930a-160">출력</span><span class="sxs-lookup"><span data-stu-id="9930a-160">OUTPUTS</span></span>

## <span data-ttu-id="9930a-161">상속자</span><span class="sxs-lookup"><span data-stu-id="9930a-161">NOTES</span></span>

## <span data-ttu-id="9930a-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9930a-162">RELATED LINKS</span></span>

[<span data-ttu-id="9930a-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9930a-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="9930a-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="9930a-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="9930a-165">시작-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9930a-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="9930a-166">중지-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9930a-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


