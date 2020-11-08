---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045764"
---
# <span data-ttu-id="c971e-101">Stop-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c971e-101">Stop-AzureHDInsightJob</span></span>

## <span data-ttu-id="c971e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c971e-102">SYNOPSIS</span></span>
<span data-ttu-id="c971e-103">HDInsight 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-103">Stops an HDInsight job.</span></span>

## <span data-ttu-id="c971e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c971e-104">SYNTAX</span></span>

### <span data-ttu-id="c971e-105">HDInsight 클러스터에서 jobDetails 시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c971e-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c971e-106">HDInsight 클러스터 (특정 구독 자격 증명 포함)에서 jobDetails 시작</span><span class="sxs-lookup"><span data-stu-id="c971e-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c971e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c971e-107">DESCRIPTION</span></span>
<span data-ttu-id="c971e-108">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="c971e-109">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="c971e-110">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="c971e-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="c971e-111">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="c971e-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="c971e-112">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="c971e-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="c971e-113">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c971e-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="c971e-114">**AzureHDInsightJob** cmdlet은 지정 된 클러스터에서 Azure HDInsight 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-114">The **Stop-AzureHDInsightJob** cmdlet stops an Azure HDInsight job on the specified cluster.</span></span>

## <span data-ttu-id="c971e-115">예제의</span><span class="sxs-lookup"><span data-stu-id="c971e-115">EXAMPLES</span></span>

## <span data-ttu-id="c971e-116">변수</span><span class="sxs-lookup"><span data-stu-id="c971e-116">PARAMETERS</span></span>

### <span data-ttu-id="c971e-117">-인증서</span><span class="sxs-lookup"><span data-stu-id="c971e-117">-Certificate</span></span>
<span data-ttu-id="c971e-118">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="c971e-119">-클러스터</span><span class="sxs-lookup"><span data-stu-id="c971e-119">-Cluster</span></span>
<span data-ttu-id="c971e-120">클러스터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-120">Specifies a cluster.</span></span>
<span data-ttu-id="c971e-121">이 cmdlet은이 매개 변수에서 지정 하는 클러스터에서 실행 되는 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-121">This cmdlet stops a job that runs on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c971e-122">-Credential</span><span class="sxs-lookup"><span data-stu-id="c971e-122">-Credential</span></span>
<span data-ttu-id="c971e-123">클러스터에 대 한 직접 HTTP 액세스에 사용할 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="c971e-124">*구독* 매개 변수 대신이 매개 변수를 지정 하 여 클러스터에 대 한 액세스를 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

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

### <span data-ttu-id="c971e-125">-끝점</span><span class="sxs-lookup"><span data-stu-id="c971e-125">-Endpoint</span></span>
<span data-ttu-id="c971e-126">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="c971e-127">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="c971e-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="c971e-128">-HostedService</span></span>
<span data-ttu-id="c971e-129">기본 네임 스페이스를 사용 하지 않으려는 경우 HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="c971e-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="c971e-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="c971e-131">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="c971e-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="c971e-132">-JobId</span></span>
<span data-ttu-id="c971e-133">중지할 HDInsight 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-133">Specifies the ID of the HDInsight job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c971e-134">-프로필</span><span class="sxs-lookup"><span data-stu-id="c971e-134">-Profile</span></span>
<span data-ttu-id="c971e-135">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c971e-136">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c971e-137">-구독</span><span class="sxs-lookup"><span data-stu-id="c971e-137">-Subscription</span></span>
<span data-ttu-id="c971e-138">구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-138">Specifies a subscription.</span></span>
<span data-ttu-id="c971e-139">이 cmdlet은이 매개 변수에서 지정 하는 구독에 대 한 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-139">This cmdlet stops a job for the subscription that this parameter specifies.</span></span>

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

### <span data-ttu-id="c971e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c971e-140">CommonParameters</span></span>
<span data-ttu-id="c971e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c971e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c971e-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c971e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c971e-143">입력</span><span class="sxs-lookup"><span data-stu-id="c971e-143">INPUTS</span></span>

## <span data-ttu-id="c971e-144">출력</span><span class="sxs-lookup"><span data-stu-id="c971e-144">OUTPUTS</span></span>

## <span data-ttu-id="c971e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c971e-145">NOTES</span></span>

## <span data-ttu-id="c971e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c971e-146">RELATED LINKS</span></span>

[<span data-ttu-id="c971e-147">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c971e-147">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="c971e-148">시작-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c971e-148">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="c971e-149">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c971e-149">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


