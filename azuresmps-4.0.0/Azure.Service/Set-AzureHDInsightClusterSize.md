---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 771B7CB2-88F6-4FC5-9DB0-E623D231E51A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bdbf7778ca2d7498d7f33586f7e9e50e0955c521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045962"
---
# <span data-ttu-id="8e2ff-101">Set-AzureHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="8e2ff-101">Set-AzureHDInsightClusterSize</span></span>

## <span data-ttu-id="8e2ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2ff-103">HDInsight 클러스터에 대 한 데이터 노드 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-103">Sets the number of data nodes for an HDInsight cluster.</span></span>

## <span data-ttu-id="8e2ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e2ff-104">SYNTAX</span></span>

### <span data-ttu-id="8e2ff-105">이름이 있는 노드에서 클러스터 크기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-105">Set cluster size in nodes with name.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> -Name <String> [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e2ff-106">파이프라인에서 클러스터를 사용 하 여 노드에서 클러스터 크기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-106">Set cluster size in nodes with cluster from pipeline.</span></span>
```
Set-AzureHDInsightClusterSize -ClusterSizeInNodes <Int32> [-Force] -Cluster <AzureHDInsightCluster>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8e2ff-107">이름별 클러스터 (특정 구독 자격 증명 포함)</span><span class="sxs-lookup"><span data-stu-id="8e2ff-107">Cluster By Name (with Specific Subscription Credential)</span></span>
```
Set-AzureHDInsightClusterSize [-Certificate <X509Certificate2>] [-Subscription <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8e2ff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8e2ff-108">DESCRIPTION</span></span>
<span data-ttu-id="8e2ff-109">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-109">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8e2ff-110">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-110">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8e2ff-111">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-111">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8e2ff-112">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8e2ff-112">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8e2ff-113">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8e2ff-113">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8e2ff-114">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8e2ff-114">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8e2ff-115">**AzureHDInsightClusterSize** Cmdlet은 Azure HDInsight 클러스터에 대 한 데이터 노드 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-115">The **Set-AzureHDInsightClusterSize** cmdlet sets the number of data nodes for an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8e2ff-116">예제의</span><span class="sxs-lookup"><span data-stu-id="8e2ff-116">EXAMPLES</span></span>

## <span data-ttu-id="8e2ff-117">변수</span><span class="sxs-lookup"><span data-stu-id="8e2ff-117">PARAMETERS</span></span>

### <span data-ttu-id="8e2ff-118">-인증서</span><span class="sxs-lookup"><span data-stu-id="8e2ff-118">-Certificate</span></span>
<span data-ttu-id="8e2ff-119">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-119">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ff-120">-클러스터</span><span class="sxs-lookup"><span data-stu-id="8e2ff-120">-Cluster</span></span>
<span data-ttu-id="8e2ff-121">크기를 조정할 클러스터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-121">Specifies the cluster to resize.</span></span>

```yaml
Type: AzureHDInsightCluster
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ff-122">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="8e2ff-122">-ClusterSizeInNodes</span></span>
<span data-ttu-id="8e2ff-123">클러스터에 대해 만들 데이터 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-123">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with name.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ff-124">-끝점</span><span class="sxs-lookup"><span data-stu-id="8e2ff-124">-Endpoint</span></span>
<span data-ttu-id="8e2ff-125">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-125">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="8e2ff-126">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-126">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ff-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8e2ff-127">-Force</span></span>
<span data-ttu-id="8e2ff-128">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Set cluster size in nodes with name., Set cluster size in nodes with cluster from pipeline.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ff-129">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="8e2ff-129">-IgnoreSslErrors</span></span>
<span data-ttu-id="8e2ff-130">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-130">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ff-131">-이름</span><span class="sxs-lookup"><span data-stu-id="8e2ff-131">-Name</span></span>
<span data-ttu-id="8e2ff-132">크기를 조정할 HDInsight 클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-132">Specifies the name of the HDInsight cluster to resize.</span></span>

```yaml
Type: String
Parameter Sets: Set cluster size in nodes with name.
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ff-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="8e2ff-133">-Profile</span></span>
<span data-ttu-id="8e2ff-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8e2ff-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e2ff-136">-구독</span><span class="sxs-lookup"><span data-stu-id="8e2ff-136">-Subscription</span></span>
<span data-ttu-id="8e2ff-137">구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-137">Specifies a subscription.</span></span>
<span data-ttu-id="8e2ff-138">이 cmdlet은이 매개 변수에서 지정 하는 구독에 대 한 클러스터 크기를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-138">This cmdlet sets the cluster size for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2ff-139">CommonParameters</span></span>
<span data-ttu-id="8e2ff-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2ff-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2ff-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2ff-142">입력</span><span class="sxs-lookup"><span data-stu-id="8e2ff-142">INPUTS</span></span>

## <span data-ttu-id="8e2ff-143">출력</span><span class="sxs-lookup"><span data-stu-id="8e2ff-143">OUTPUTS</span></span>

## <span data-ttu-id="8e2ff-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8e2ff-144">NOTES</span></span>

## <span data-ttu-id="8e2ff-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e2ff-145">RELATED LINKS</span></span>

