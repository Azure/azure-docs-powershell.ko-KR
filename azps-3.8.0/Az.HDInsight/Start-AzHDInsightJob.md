---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878505"
---
# <span data-ttu-id="85a69-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85a69-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="85a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a69-102">SYNOPSIS</span></span>
<span data-ttu-id="85a69-103">지정 된 클러스터에서 정의 된 Azure HDInsight 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="85a69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85a69-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85a69-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85a69-105">DESCRIPTION</span></span>
<span data-ttu-id="85a69-106">**AzHDInsightJob** cmdlet은 지정 된 클러스터에서 정의 된 Azure HDInsight 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="85a69-107">이는 MapReduce job, 스트리밍 MapReduce 작업, 하이브 작업 또는 문 돼지 job 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="85a69-108">예제의</span><span class="sxs-lookup"><span data-stu-id="85a69-108">EXAMPLES</span></span>

### <span data-ttu-id="85a69-109">예제 1: 지정 된 클러스터에서 작업 시작</span><span class="sxs-lookup"><span data-stu-id="85a69-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="85a69-110">이 명령은-hadoop-001 이라는 클러스터에서 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="85a69-111">변수</span><span class="sxs-lookup"><span data-stu-id="85a69-111">PARAMETERS</span></span>

### <span data-ttu-id="85a69-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="85a69-112">-ClusterName</span></span>
<span data-ttu-id="85a69-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a69-114">-DefaultProfile</span></span>
<span data-ttu-id="85a69-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="85a69-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a69-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="85a69-116">-HttpCredential</span></span>
<span data-ttu-id="85a69-117">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a69-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="85a69-118">-JobDefinition</span></span>
<span data-ttu-id="85a69-119">Azure HDInsight 클러스터에서 시작할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85a69-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a69-120">-ResourceGroupName</span></span>
<span data-ttu-id="85a69-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-121">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a69-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a69-122">CommonParameters</span></span>
<span data-ttu-id="85a69-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85a69-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a69-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a69-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a69-125">입력</span><span class="sxs-lookup"><span data-stu-id="85a69-125">INPUTS</span></span>

### <span data-ttu-id="85a69-126">AzureHDInsightJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="85a69-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="85a69-127">출력</span><span class="sxs-lookup"><span data-stu-id="85a69-127">OUTPUTS</span></span>

### <span data-ttu-id="85a69-128">AzureHDInsightJob의. m m.</span><span class="sxs-lookup"><span data-stu-id="85a69-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="85a69-129">상속자</span><span class="sxs-lookup"><span data-stu-id="85a69-129">NOTES</span></span>

## <span data-ttu-id="85a69-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85a69-130">RELATED LINKS</span></span>

[<span data-ttu-id="85a69-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85a69-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="85a69-132">새로운 AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="85a69-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="85a69-133">중지-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85a69-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="85a69-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85a69-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


