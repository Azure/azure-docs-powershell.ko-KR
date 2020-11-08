---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 7D73D37B-17EE-4FF8-9A21-D2014D5417D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa779907648ca8e8e1288394d562c86b6102d9ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046476"
---
# <span data-ttu-id="ba751-101">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ba751-101">Remove-AzureHDInsightCluster</span></span>

## <span data-ttu-id="ba751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba751-102">SYNOPSIS</span></span>
<span data-ttu-id="ba751-103">구독에서 HDInsight 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-103">Deletes an HDInsight cluster from a subscription.</span></span>

## <span data-ttu-id="ba751-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba751-104">SYNTAX</span></span>

```
Remove-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Name <String> [-Subscription <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba751-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba751-105">DESCRIPTION</span></span>
<span data-ttu-id="ba751-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ba751-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ba751-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba751-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ba751-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ba751-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ba751-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ba751-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ba751-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ba751-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ba751-112">**AzureHDInsightCluster** cmdlet은 지정 된 HDInsight 서비스 클러스터를 구독에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-112">The **Remove-AzureHDInsightCluster** cmdlet deletes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="ba751-113">또한이 작업은 클러스터의 Hadoop 분산 파일 시스템 (HDFS)에 저장 된 모든 데이터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-113">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="ba751-114">연결 된 Azure 저장소 계정에 저장 된 데이터는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-114">Data stored in the associated Azure Storage account is not deleted.</span></span>

## <span data-ttu-id="ba751-115">예제의</span><span class="sxs-lookup"><span data-stu-id="ba751-115">EXAMPLES</span></span>

### <span data-ttu-id="ba751-116">예제 1: 클러스터 제거</span><span class="sxs-lookup"><span data-stu-id="ba751-116">Example 1: Remove a cluster</span></span>
```
PS C:\>Remove-AzureHDInsightCluster -Name "HDICluster"
```

<span data-ttu-id="ba751-117">이 명령은 HDICluster 이라는 HDInsight 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-117">This command deletes the HDInsight cluster named HDICluster.</span></span>

## <span data-ttu-id="ba751-118">변수</span><span class="sxs-lookup"><span data-stu-id="ba751-118">PARAMETERS</span></span>

### <span data-ttu-id="ba751-119">-인증서</span><span class="sxs-lookup"><span data-stu-id="ba751-119">-Certificate</span></span>
<span data-ttu-id="ba751-120">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-120">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="ba751-121">-끝점</span><span class="sxs-lookup"><span data-stu-id="ba751-121">-Endpoint</span></span>
<span data-ttu-id="ba751-122">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-122">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="ba751-123">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-123">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="ba751-124">-HostedService</span><span class="sxs-lookup"><span data-stu-id="ba751-124">-HostedService</span></span>
<span data-ttu-id="ba751-125">기본 네임 스페이스를 사용 하지 않으려는 경우 HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-125">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="ba751-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="ba751-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="ba751-127">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="ba751-128">-이름</span><span class="sxs-lookup"><span data-stu-id="ba751-128">-Name</span></span>
<span data-ttu-id="ba751-129">제거할 HDInsight 클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-129">Specifies the name of the HDInsight cluster to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba751-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="ba751-130">-Profile</span></span>
<span data-ttu-id="ba751-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba751-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba751-133">-구독</span><span class="sxs-lookup"><span data-stu-id="ba751-133">-Subscription</span></span>
<span data-ttu-id="ba751-134">제거할 HDInsight 클러스터를 포함 하는 구독 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-134">Specifies the subscription account that contains the HDInsight cluster to remove.</span></span>

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

### <span data-ttu-id="ba751-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba751-135">CommonParameters</span></span>
<span data-ttu-id="ba751-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba751-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba751-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba751-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba751-138">입력</span><span class="sxs-lookup"><span data-stu-id="ba751-138">INPUTS</span></span>

## <span data-ttu-id="ba751-139">출력</span><span class="sxs-lookup"><span data-stu-id="ba751-139">OUTPUTS</span></span>

## <span data-ttu-id="ba751-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ba751-140">NOTES</span></span>

## <span data-ttu-id="ba751-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba751-141">RELATED LINKS</span></span>

[<span data-ttu-id="ba751-142">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ba751-142">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="ba751-143">새로운 AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ba751-143">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="ba751-144">-AzureHDInsightCluster 사용</span><span class="sxs-lookup"><span data-stu-id="ba751-144">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


