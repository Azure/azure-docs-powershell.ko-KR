---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3E3C9626-7AED-4B15-93D0-0B79AD17A834
online version: ''
schema: 2.0.0
ms.openlocfilehash: de4b768dbc6c97e84bccd4c8e0ef42f6f81a5b31
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046350"
---
# <span data-ttu-id="d6470-101">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6470-101">Get-AzureHDInsightJob</span></span>

## <span data-ttu-id="d6470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6470-102">SYNOPSIS</span></span>
<span data-ttu-id="d6470-103">HDInsight 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-103">Gets HDInsight jobs.</span></span>

## <span data-ttu-id="d6470-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6470-104">SYNTAX</span></span>

### <span data-ttu-id="d6470-105">HDInsight 클러스터의 jobDetails 기록 가져오기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6470-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Get-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] [-IgnoreSslErrors <Boolean>]
 [-JobId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d6470-106">HDInsight 클러스터 (특정 구독 자격 증명 포함)의 jobDetails 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="d6470-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Get-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] [-JobId <String>] [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d6470-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d6470-107">DESCRIPTION</span></span>
<span data-ttu-id="d6470-108">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d6470-109">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d6470-110">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6470-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d6470-111">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d6470-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d6470-112">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="d6470-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d6470-113">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d6470-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d6470-114">**AzureHDInsightJob** cmdlet은 지정 된 클러스터에 대 한 최근 Azure HDInsight 작업을 가져와 그 순서의 역순으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-114">The **Get-AzureHDInsightJob** cmdlet gets recent Azure HDInsight jobs for a specified cluster and displays them in reverse chronological order.</span></span>

## <span data-ttu-id="d6470-115">예제의</span><span class="sxs-lookup"><span data-stu-id="d6470-115">EXAMPLES</span></span>

## <span data-ttu-id="d6470-116">변수</span><span class="sxs-lookup"><span data-stu-id="d6470-116">PARAMETERS</span></span>

### <span data-ttu-id="d6470-117">-인증서</span><span class="sxs-lookup"><span data-stu-id="d6470-117">-Certificate</span></span>
<span data-ttu-id="d6470-118">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-118">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="d6470-119">-클러스터</span><span class="sxs-lookup"><span data-stu-id="d6470-119">-Cluster</span></span>
<span data-ttu-id="d6470-120">클러스터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-120">Specifies a cluster.</span></span>
<span data-ttu-id="d6470-121">이 cmdlet은이 매개 변수에서 지정 하는 클러스터에서 실행 되는 HDInsight 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-121">This cmdlet gets HDInsight jobs that run on the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="d6470-122">-Credential</span><span class="sxs-lookup"><span data-stu-id="d6470-122">-Credential</span></span>
<span data-ttu-id="d6470-123">클러스터에 대 한 직접 HTTP 액세스에 사용할 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-123">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="d6470-124">*구독* 매개 변수 대신이 매개 변수를 지정 하 여 클러스터에 대 한 액세스를 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-124">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6470-125">-끝점</span><span class="sxs-lookup"><span data-stu-id="d6470-125">-Endpoint</span></span>
<span data-ttu-id="d6470-126">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-126">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="d6470-127">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-127">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="d6470-128">-HostedService</span><span class="sxs-lookup"><span data-stu-id="d6470-128">-HostedService</span></span>
<span data-ttu-id="d6470-129">기본 네임 스페이스를 사용 하지 않으려는 경우 HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-129">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="d6470-130">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="d6470-130">-IgnoreSslErrors</span></span>
<span data-ttu-id="d6470-131">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-131">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="d6470-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="d6470-132">-JobId</span></span>
<span data-ttu-id="d6470-133">가져올 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-133">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6470-134">-프로필</span><span class="sxs-lookup"><span data-stu-id="d6470-134">-Profile</span></span>
<span data-ttu-id="d6470-135">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6470-136">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6470-137">-구독</span><span class="sxs-lookup"><span data-stu-id="d6470-137">-Subscription</span></span>
<span data-ttu-id="d6470-138">가져올 HDInsight 작업을 포함 하는 구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-138">Specifies the subscription that contains the HDInsight jobs to get.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6470-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6470-139">CommonParameters</span></span>
<span data-ttu-id="d6470-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6470-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6470-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6470-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6470-142">입력</span><span class="sxs-lookup"><span data-stu-id="d6470-142">INPUTS</span></span>

## <span data-ttu-id="d6470-143">출력</span><span class="sxs-lookup"><span data-stu-id="d6470-143">OUTPUTS</span></span>

## <span data-ttu-id="d6470-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d6470-144">NOTES</span></span>

## <span data-ttu-id="d6470-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6470-145">RELATED LINKS</span></span>

[<span data-ttu-id="d6470-146">시작-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6470-146">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="d6470-147">중지-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6470-147">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="d6470-148">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d6470-148">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


