---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A1DFA523-B532-4902-838D-74C8CA97A335
online version: ''
schema: 2.0.0
ms.openlocfilehash: f85d12100eb5b2b093eea252ac308e8a45cf1c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046434"
---
# <span data-ttu-id="cc783-101">Revoke-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cc783-101">Revoke-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="cc783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc783-102">SYNOPSIS</span></span>
<span data-ttu-id="cc783-103">클러스터에 대 한 HTTP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-103">Disables HTTP access to a cluster.</span></span>

## <span data-ttu-id="cc783-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc783-104">SYNTAX</span></span>

```
Revoke-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 [-IgnoreSslErrors <Boolean>] [-Endpoint <Uri>] -Location <String> -Name <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cc783-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cc783-105">DESCRIPTION</span></span>
<span data-ttu-id="cc783-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="cc783-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="cc783-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="cc783-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="cc783-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="cc783-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="cc783-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="cc783-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="cc783-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cc783-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="cc783-112">**AzureHDInsightHttpServicesAccess** CMDLET은 ODBC, Ambari, Oozie 및 WebHCatalog 웹 서비스에 대 한 클러스터에 대 한 HTTP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-112">The **Revoke-AzureHDInsightHttpServicesAccess** cmdlet disables HTTP access to a cluster for ODBC, Ambari, Oozie and WebHCatalog web services.</span></span>

## <span data-ttu-id="cc783-113">예제의</span><span class="sxs-lookup"><span data-stu-id="cc783-113">EXAMPLES</span></span>

## <span data-ttu-id="cc783-114">변수</span><span class="sxs-lookup"><span data-stu-id="cc783-114">PARAMETERS</span></span>

### <span data-ttu-id="cc783-115">-인증서</span><span class="sxs-lookup"><span data-stu-id="cc783-115">-Certificate</span></span>
<span data-ttu-id="cc783-116">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="cc783-117">-끝점</span><span class="sxs-lookup"><span data-stu-id="cc783-117">-Endpoint</span></span>
<span data-ttu-id="cc783-118">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-118">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="cc783-119">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-119">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="cc783-120">-HostedService</span><span class="sxs-lookup"><span data-stu-id="cc783-120">-HostedService</span></span>
<span data-ttu-id="cc783-121">기본 네임 스페이스를 사용 하지 않으려는 경우 HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-121">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

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

### <span data-ttu-id="cc783-122">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="cc783-122">-IgnoreSslErrors</span></span>
<span data-ttu-id="cc783-123">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-123">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="cc783-124">-위치</span><span class="sxs-lookup"><span data-stu-id="cc783-124">-Location</span></span>
<span data-ttu-id="cc783-125">HDInsight 클러스터가 있는 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-125">Specifies the region in which an HDInsight cluster is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc783-126">-이름</span><span class="sxs-lookup"><span data-stu-id="cc783-126">-Name</span></span>
<span data-ttu-id="cc783-127">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-127">Specifies the name of a cluster.</span></span>
<span data-ttu-id="cc783-128">이 cmdlet은이 매개 변수에서 지정 하는 클러스터에 대 한 HTTP 액세스를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-128">This cmdlet disables HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc783-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="cc783-129">-Profile</span></span>
<span data-ttu-id="cc783-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc783-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc783-132">-구독</span><span class="sxs-lookup"><span data-stu-id="cc783-132">-Subscription</span></span>
<span data-ttu-id="cc783-133">해지할 HDInsight 클러스터를 포함 하는 구독 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-133">Specifies the subscription account that contains the HDInsight cluster to revoke.</span></span>

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

### <span data-ttu-id="cc783-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc783-134">CommonParameters</span></span>
<span data-ttu-id="cc783-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc783-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc783-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc783-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc783-137">입력</span><span class="sxs-lookup"><span data-stu-id="cc783-137">INPUTS</span></span>

## <span data-ttu-id="cc783-138">출력</span><span class="sxs-lookup"><span data-stu-id="cc783-138">OUTPUTS</span></span>

## <span data-ttu-id="cc783-139">상속자</span><span class="sxs-lookup"><span data-stu-id="cc783-139">NOTES</span></span>

## <span data-ttu-id="cc783-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc783-140">RELATED LINKS</span></span>

[<span data-ttu-id="cc783-141">부여-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cc783-141">Grant-AzureHDInsightHttpServicesAccess</span></span>](./Grant-AzureHDInsightHttpServicesAccess.md)


