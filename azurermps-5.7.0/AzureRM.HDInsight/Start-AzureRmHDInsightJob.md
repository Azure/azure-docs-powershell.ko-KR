---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 8c3e0f01472469be856d69c1a87f8eb5185f2012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536803"
---
# <span data-ttu-id="8f64b-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8f64b-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="8f64b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f64b-102">SYNOPSIS</span></span>
<span data-ttu-id="8f64b-103">지정 된 클러스터에서 정의 된 Azure HDInsight 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f64b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f64b-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f64b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8f64b-105">DESCRIPTION</span></span>
<span data-ttu-id="8f64b-106">**AzureRMHDInsightJob** cmdlet은 지정 된 클러스터에서 정의 된 Azure HDInsight 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="8f64b-107">이는 MapReduce job, 스트리밍 MapReduce 작업, 하이브 작업 또는 문 돼지 job 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="8f64b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8f64b-108">EXAMPLES</span></span>

### <span data-ttu-id="8f64b-109">예제 1: 지정 된 클러스터에서 작업 시작</span><span class="sxs-lookup"><span data-stu-id="8f64b-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8f64b-110">이 명령은-hadoop-001 이라는 클러스터에서 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8f64b-111">변수</span><span class="sxs-lookup"><span data-stu-id="8f64b-111">PARAMETERS</span></span>

### <span data-ttu-id="8f64b-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8f64b-112">-ClusterName</span></span>
<span data-ttu-id="8f64b-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f64b-114">-DefaultProfile</span></span>
<span data-ttu-id="8f64b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8f64b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64b-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="8f64b-116">-HttpCredential</span></span>
<span data-ttu-id="8f64b-117">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64b-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="8f64b-118">-JobDefinition</span></span>
<span data-ttu-id="8f64b-119">Azure HDInsight 클러스터에서 시작할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f64b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f64b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f64b-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f64b-122">CommonParameters</span></span>
<span data-ttu-id="8f64b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f64b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f64b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f64b-125">입력</span><span class="sxs-lookup"><span data-stu-id="8f64b-125">INPUTS</span></span>

### <span data-ttu-id="8f64b-126">AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8f64b-126">AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="8f64b-127">' JobDefinition ' 매개 변수는 파이프라인에서 ' AzureHDInsightJobDefinition ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f64b-127">Parameter 'JobDefinition' accepts value of type 'AzureHDInsightJobDefinition' from the pipeline</span></span>

## <span data-ttu-id="8f64b-128">출력</span><span class="sxs-lookup"><span data-stu-id="8f64b-128">OUTPUTS</span></span>

### <span data-ttu-id="8f64b-129">AzureHDInsightJob의. m m.</span><span class="sxs-lookup"><span data-stu-id="8f64b-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="8f64b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="8f64b-130">NOTES</span></span>

## <span data-ttu-id="8f64b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f64b-131">RELATED LINKS</span></span>

[<span data-ttu-id="8f64b-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8f64b-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="8f64b-133">새로운 AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8f64b-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="8f64b-134">중지-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8f64b-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="8f64b-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8f64b-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


