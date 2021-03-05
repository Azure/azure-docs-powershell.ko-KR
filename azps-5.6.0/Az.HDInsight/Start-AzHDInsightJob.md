---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 316ac2671fe60271ad0d994855189071e3da2b95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964715"
---
# <span data-ttu-id="0b177-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0b177-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="0b177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b177-102">SYNOPSIS</span></span>
<span data-ttu-id="0b177-103">지정된 클러스터에서 정의된 Azure HDInsight 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="0b177-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b177-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b177-105">설명</span><span class="sxs-lookup"><span data-stu-id="0b177-105">DESCRIPTION</span></span>
<span data-ttu-id="0b177-106">**Start-AzHDInsightJob** cmdlet은 지정된 클러스터에서 정의된 Azure HDInsight 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="0b177-107">MapReduce 작업, 스트리밍 MapReduce 작업, Hive 작업 또는 Pig 작업일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="0b177-108">예제</span><span class="sxs-lookup"><span data-stu-id="0b177-108">EXAMPLES</span></span>

### <span data-ttu-id="0b177-109">예제 1: 지정된 클러스터에서 작업 시작</span><span class="sxs-lookup"><span data-stu-id="0b177-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="0b177-110">이 명령은 your-hadoop-001이라는 클러스터에서 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0b177-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0b177-111">PARAMETERS</span></span>

### <span data-ttu-id="0b177-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0b177-112">-ClusterName</span></span>
<span data-ttu-id="0b177-113">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0b177-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b177-114">-DefaultProfile</span></span>
<span data-ttu-id="0b177-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0b177-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b177-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0b177-116">-HttpCredential</span></span>
<span data-ttu-id="0b177-117">클러스터에 대한 HTTP(클러스터 로그인) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="0b177-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="0b177-118">-JobDefinition</span></span>
<span data-ttu-id="0b177-119">Azure HDInsight 클러스터에서 시작할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="0b177-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b177-120">-ResourceGroupName</span></span>
<span data-ttu-id="0b177-121">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0b177-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b177-122">CommonParameters</span></span>
<span data-ttu-id="0b177-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b177-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b177-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b177-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b177-125">입력</span><span class="sxs-lookup"><span data-stu-id="0b177-125">INPUTS</span></span>

### <span data-ttu-id="0b177-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0b177-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="0b177-127">출력</span><span class="sxs-lookup"><span data-stu-id="0b177-127">OUTPUTS</span></span>

### <span data-ttu-id="0b177-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0b177-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="0b177-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b177-129">NOTES</span></span>

## <span data-ttu-id="0b177-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b177-130">RELATED LINKS</span></span>

[<span data-ttu-id="0b177-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0b177-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="0b177-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0b177-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="0b177-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0b177-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="0b177-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0b177-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


