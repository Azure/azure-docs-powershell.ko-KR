---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 325DE85D-B9CB-4584-8C61-DA417736ABBF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55992408c1376c9456157387456b114c292b44c2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046351"
---
# <span data-ttu-id="b07da-101">Get-AzureHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="b07da-101">Get-AzureHDInsightProperties</span></span>

## <span data-ttu-id="b07da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b07da-102">SYNOPSIS</span></span>
<span data-ttu-id="b07da-103">HDInsight 서비스와 관련 된 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-103">Gets properties specific to an HDInsight service.</span></span>

## <span data-ttu-id="b07da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b07da-104">SYNTAX</span></span>

```
Get-AzureHDInsightProperties [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] [-Locations] [-Subscription <String>] [-Versions] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b07da-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b07da-105">DESCRIPTION</span></span>
<span data-ttu-id="b07da-106">이 버전의 Azure PowerShell HDInsight는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="b07da-107">이러한 cmdlet은 2017 년 1 월 1 일에 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="b07da-108">최신 버전의 Azure PowerShell HDInsight를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="b07da-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="b07da-109">새 HDInsight를 사용 하 여 클러스터를 만드는 방법에 대 한 자세한 내용은 [HDInsight에서 Azure PowerShell ()을 사용 하 여 Linux 기반 클러스터 만들기](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) 를 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="b07da-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="b07da-110">Azure PowerShell 및 기타 접근 방법을 사용 하 여 작업을 제출 하는 방법에 대 한 자세한 내용은 [HDInsight에서 Hadoop 작업 제출](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ()을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="b07da-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="b07da-111">Azure PowerShell HDInsight에 대 한 참조 정보는 [Azure Hdinsight cmdlet](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ()을 참조 하세요 https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b07da-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="b07da-112">**AzureHDInsightProperties** cmdlet은 사용 가능한 azure 지역 목록, HDInsight 클러스터 버전, 사용 가능한 계산 용량 등 azure HDInsight 서비스와 관련 된 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-112">The **Get-AzureHDInsightProperties** cmdlet gets properties specific to an Azure HDInsight service, such as a list of available Azure regions, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="b07da-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b07da-113">EXAMPLES</span></span>

### <span data-ttu-id="b07da-114">예제 1: 구독에 대 한 HDInsight 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b07da-114">Example 1: Get HDInsight properties for a subscription</span></span>
```
PS C:\>$SubName = Get-AzureSubscription -Current | %{ $_.SubscriptionName }
PS C:\> Get-AzureHDInsightProperties -Subscription $SubName
```

<span data-ttu-id="b07da-115">첫 번째 명령은 현재 Azure 구독 이름을 가져온 다음 $SubName 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-115">The first command gets the name of the current Azure subscription, and then stores it in the $SubName variable.</span></span>

<span data-ttu-id="b07da-116">두 번째 명령은 $SubName 구독에 대 한 HDInsight 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-116">The second command gets the HDInsight properties for the subscription in $SubName.</span></span>

## <span data-ttu-id="b07da-117">변수</span><span class="sxs-lookup"><span data-stu-id="b07da-117">PARAMETERS</span></span>

### <span data-ttu-id="b07da-118">-인증서</span><span class="sxs-lookup"><span data-stu-id="b07da-118">-Certificate</span></span>
<span data-ttu-id="b07da-119">Azure 구독에 대 한 관리 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-119">Specifies the management certificate for an Azure subscription.</span></span>

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

### <span data-ttu-id="b07da-120">-끝점</span><span class="sxs-lookup"><span data-stu-id="b07da-120">-Endpoint</span></span>
<span data-ttu-id="b07da-121">Azure에 연결 하는 데 사용할 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-121">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="b07da-122">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 끝점을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-122">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

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

### <span data-ttu-id="b07da-123">-HostedService</span><span class="sxs-lookup"><span data-stu-id="b07da-123">-HostedService</span></span>
<span data-ttu-id="b07da-124">HDInsight 서비스의 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-124">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="b07da-125">이 매개 변수를 지정 하지 않으면이 cmdlet은 기본 네임 스페이스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-125">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

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

### <span data-ttu-id="b07da-126">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="b07da-126">-IgnoreSslErrors</span></span>
<span data-ttu-id="b07da-127">SSL (Secure Sockets Layer) 오류가 무시 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-127">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

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

### <span data-ttu-id="b07da-128">-위치</span><span class="sxs-lookup"><span data-stu-id="b07da-128">-Locations</span></span>
<span data-ttu-id="b07da-129">이 cmdlet이 HDInsight 서비스를 사용할 수 있는 Azure 지역 목록을 가져와 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-129">Indicates that this cmdlet gets the list of Azure regions where the HDInsight service is available.</span></span>

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

### <span data-ttu-id="b07da-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="b07da-130">-Profile</span></span>
<span data-ttu-id="b07da-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b07da-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b07da-133">-구독</span><span class="sxs-lookup"><span data-stu-id="b07da-133">-Subscription</span></span>
<span data-ttu-id="b07da-134">가져올 HDInsight 속성이 포함 된 구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-134">Specifies the subscription that contains the HDInsight properties to get.</span></span>

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

### <span data-ttu-id="b07da-135">-버전</span><span class="sxs-lookup"><span data-stu-id="b07da-135">-Versions</span></span>
<span data-ttu-id="b07da-136">이 cmdlet이 구독에 대 한 서비스에서 사용할 수 있는 HDInsight 클러스터 버전 목록을 가져오기 위해 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-136">Indicates that this cmdlet gets the list of HDInsight cluster versions that are available in the service for a subscription.</span></span>

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

### <span data-ttu-id="b07da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07da-137">CommonParameters</span></span>
<span data-ttu-id="b07da-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b07da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07da-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07da-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07da-140">입력</span><span class="sxs-lookup"><span data-stu-id="b07da-140">INPUTS</span></span>

## <span data-ttu-id="b07da-141">출력</span><span class="sxs-lookup"><span data-stu-id="b07da-141">OUTPUTS</span></span>

## <span data-ttu-id="b07da-142">상속자</span><span class="sxs-lookup"><span data-stu-id="b07da-142">NOTES</span></span>

## <span data-ttu-id="b07da-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b07da-143">RELATED LINKS</span></span>

