---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E3D22B03-2997-4F2C-895E-AE0993FD7C92
online version: ''
schema: 2.0.0
ms.openlocfilehash: bfd3e1f2bb5d057dec8a7bee5929ba5c67c8d53d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046498"
---
# <span data-ttu-id="a525c-101">Grant-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a525c-101">Grant-AzureHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="a525c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a525c-102">SYNOPSIS</span></span>
<span data-ttu-id="a525c-103">클러스터에 대 한 HTTP 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-103">Grants HTTP access to a cluster.</span></span>

## <span data-ttu-id="a525c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a525c-104">SYNTAX</span></span>

```
Grant-AzureHDInsightHttpServicesAccess [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Credential <PSCredential> [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a525c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a525c-105">DESCRIPTION</span></span>
<span data-ttu-id="a525c-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="a525c-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="a525c-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="a525c-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="a525c-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="a525c-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="a525c-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="a525c-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="a525c-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a525c-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="a525c-112">**AzureHDInsightHttpServicesAccess** CMDLET은 ODBC, Ambari, Oozie, 웹 서비스를 사용 하 여 Azure HDInsight 클러스터에 대 한 HTTP 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-112">The **Grant-AzureHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie, and web services.</span></span>

## <span data-ttu-id="a525c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a525c-113">EXAMPLES</span></span>

## <span data-ttu-id="a525c-114">변수</span><span class="sxs-lookup"><span data-stu-id="a525c-114">PARAMETERS</span></span>

### <span data-ttu-id="a525c-115">-인증서</span><span class="sxs-lookup"><span data-stu-id="a525c-115">-Certificate</span></span>
<span data-ttu-id="a525c-116">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-116">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="a525c-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="a525c-117">-Credential</span></span>
<span data-ttu-id="a525c-118">HTTP 액세스에 대 한 사용자 이름 및 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-118">Specifies a user name and password for HTTP access.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a525c-119">-끝점</span><span class="sxs-lookup"><span data-stu-id="a525c-119">-Endpoint</span></span>
<span data-ttu-id="a525c-120">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-120">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="a525c-121">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-121">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="a525c-122">-HostedService</span><span class="sxs-lookup"><span data-stu-id="a525c-122">-HostedService</span></span>
<span data-ttu-id="a525c-123">HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-123">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="a525c-124">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 네임 스페이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-124">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="a525c-125">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="a525c-125">-IgnoreSslErrors</span></span>
<span data-ttu-id="a525c-126">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-126">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="a525c-127">-위치</span><span class="sxs-lookup"><span data-stu-id="a525c-127">-Location</span></span>
<span data-ttu-id="a525c-128">클러스터가 있는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-128">Specifies the Azure region in which a cluster is located.</span></span>

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

### <span data-ttu-id="a525c-129">-이름</span><span class="sxs-lookup"><span data-stu-id="a525c-129">-Name</span></span>
<span data-ttu-id="a525c-130">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-130">Specifies the name of a cluster.</span></span>
<span data-ttu-id="a525c-131">이 cmdlet은이 매개 변수에서 지정 하는 클러스터에 대 한 HTTP 액세스를 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-131">This cmdlet grants HTTP access to the cluster that this parameter specifies.</span></span>

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

### <span data-ttu-id="a525c-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="a525c-132">-Profile</span></span>
<span data-ttu-id="a525c-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a525c-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a525c-135">-구독</span><span class="sxs-lookup"><span data-stu-id="a525c-135">-Subscription</span></span>
<span data-ttu-id="a525c-136">액세스를 부여할 HDInsight 클러스터가 포함 된 구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-136">Specifies the subscription that contains the HDInsight cluster to which to grant access.</span></span>

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

### <span data-ttu-id="a525c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a525c-137">CommonParameters</span></span>
<span data-ttu-id="a525c-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a525c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a525c-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a525c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a525c-140">입력</span><span class="sxs-lookup"><span data-stu-id="a525c-140">INPUTS</span></span>

## <span data-ttu-id="a525c-141">출력</span><span class="sxs-lookup"><span data-stu-id="a525c-141">OUTPUTS</span></span>

## <span data-ttu-id="a525c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a525c-142">NOTES</span></span>

## <span data-ttu-id="a525c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a525c-143">RELATED LINKS</span></span>

[<span data-ttu-id="a525c-144">철회-AzureHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a525c-144">Revoke-AzureHDInsightHttpServicesAccess</span></span>](./Revoke-AzureHDInsightHttpServicesAccess.md)


