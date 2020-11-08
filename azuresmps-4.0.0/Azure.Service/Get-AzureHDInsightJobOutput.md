---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045640"
---
# <span data-ttu-id="383f2-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="383f2-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="383f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="383f2-102">SYNOPSIS</span></span>
<span data-ttu-id="383f2-103">작업에 대 한 로그 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="383f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="383f2-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="383f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="383f2-105">DESCRIPTION</span></span>
<span data-ttu-id="383f2-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="383f2-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="383f2-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="383f2-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="383f2-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell을 사용 하 여](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/)Linux 기반 클러스터 만들기를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="383f2-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="383f2-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출을](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="383f2-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="383f2-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure HDInsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="383f2-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="383f2-112">**AzureHDInsightJobOutput** cmdlet은 클러스터와 연결 된 저장소 계정의 작업에 대 한 로그 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="383f2-113">표준 출력, 표준 오류, 작업 로그, 작업 로그 요약 등 다양 한 유형의 작업 로그를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="383f2-114">예제의</span><span class="sxs-lookup"><span data-stu-id="383f2-114">EXAMPLES</span></span>

### <span data-ttu-id="383f2-115">예제 1: 작업 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="383f2-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="383f2-116">첫 번째 명령은 현재 구독의 ID를 가져온 다음 $SubId 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="383f2-117">두 번째 명령은 $Clustername 변수에 이름 MyCluster를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="383f2-118">세 번째 명령은 MapReduce 작업 정의를 만든 다음 $WordCountJob 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="383f2-119">이 명령은 $WordCountJob 작업을 **AzureHDInsightJob** cmdlet에 전달 하 여 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="383f2-120">또한 **AzureHDInsightJob** cmdlet에 $WordCountJob를 전달 하 여 작업이 완료 될 때까지 기다린 후 **AzureHDInsightJobOutput** 를 사용 하 여 작업 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="383f2-121">변수</span><span class="sxs-lookup"><span data-stu-id="383f2-121">PARAMETERS</span></span>

### <span data-ttu-id="383f2-122">-인증서</span><span class="sxs-lookup"><span data-stu-id="383f2-122">-Certificate</span></span>
<span data-ttu-id="383f2-123">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383f2-124">-클러스터</span><span class="sxs-lookup"><span data-stu-id="383f2-124">-Cluster</span></span>
<span data-ttu-id="383f2-125">클러스터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-125">Specifies a cluster.</span></span>
<span data-ttu-id="383f2-126">이 cmdlet은이 매개 변수에서 지정 하는 클러스터의 작업 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="383f2-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="383f2-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="383f2-128">이 cmdlet이 작업에 대 한 작업 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

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

### <span data-ttu-id="383f2-129">-끝점</span><span class="sxs-lookup"><span data-stu-id="383f2-129">-Endpoint</span></span>
<span data-ttu-id="383f2-130">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="383f2-131">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383f2-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="383f2-132">-HostedService</span></span>
<span data-ttu-id="383f2-133">기본 네임 스페이스를 사용 하지 않으려는 경우 HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383f2-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="383f2-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="383f2-135">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383f2-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="383f2-136">-JobId</span></span>
<span data-ttu-id="383f2-137">가져올 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="383f2-138">-프로필</span><span class="sxs-lookup"><span data-stu-id="383f2-138">-Profile</span></span>
<span data-ttu-id="383f2-139">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="383f2-140">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="383f2-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="383f2-141">-StandardError</span></span>
<span data-ttu-id="383f2-142">이 cmdlet이 작업의 StdErr 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

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

### <span data-ttu-id="383f2-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="383f2-143">-StandardOutput</span></span>
<span data-ttu-id="383f2-144">이 cmdlet이 작업의 SdtOut 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

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

### <span data-ttu-id="383f2-145">-구독</span><span class="sxs-lookup"><span data-stu-id="383f2-145">-Subscription</span></span>
<span data-ttu-id="383f2-146">가져올 HDInsight 클러스터가 포함 된 구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383f2-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="383f2-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="383f2-148">작업 로그를 저장할 로컬 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383f2-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="383f2-149">-TaskSummary</span></span>
<span data-ttu-id="383f2-150">이 cmdlet이 작업 로그 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-150">Indicates that this cmdlets gets the task log summary.</span></span>

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

### <span data-ttu-id="383f2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383f2-151">CommonParameters</span></span>
<span data-ttu-id="383f2-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="383f2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383f2-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="383f2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383f2-154">입력</span><span class="sxs-lookup"><span data-stu-id="383f2-154">INPUTS</span></span>

## <span data-ttu-id="383f2-155">출력</span><span class="sxs-lookup"><span data-stu-id="383f2-155">OUTPUTS</span></span>

## <span data-ttu-id="383f2-156">상속자</span><span class="sxs-lookup"><span data-stu-id="383f2-156">NOTES</span></span>

## <span data-ttu-id="383f2-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="383f2-157">RELATED LINKS</span></span>

[<span data-ttu-id="383f2-158">새로운 AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="383f2-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="383f2-159">시작-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="383f2-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="383f2-160">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="383f2-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
