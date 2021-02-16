---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: dc7f69ef29d7e5396ad57346380decc672f83db5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185881"
---
# <span data-ttu-id="e6e56-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e56-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="e6e56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e56-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e56-103">클러스터에서 작업 목록을 가져온 후 역순으로 나열하거나 특정 작업을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="e6e56-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6e56-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6e56-105">설명</span><span class="sxs-lookup"><span data-stu-id="e6e56-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e56-106">**Get-AzHDInsightJob** cmdlet은 지정된 Azure HDInsight 클러스터에 대한 최근 작업을 시간순으로 되돌리며, 가장 최근 작업은 목록 맨 위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="e6e56-107">*JobId* 매개 변수를 제공하여 특정 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="e6e56-108">예제</span><span class="sxs-lookup"><span data-stu-id="e6e56-108">EXAMPLES</span></span>

### <span data-ttu-id="e6e56-109">예제 1: 지정된 Azure HDInsight 클러스터에 대한 최근 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="e6e56-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="e6e56-110">이 명령은 your-hadoop-001이라는 클러스터에 대한 모든 최근 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e6e56-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6e56-111">PARAMETERS</span></span>

### <span data-ttu-id="e6e56-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e6e56-112">-ClusterName</span></span>
<span data-ttu-id="e6e56-113">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e6e56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e56-114">-DefaultProfile</span></span>
<span data-ttu-id="e6e56-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e6e56-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6e56-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e6e56-116">-HttpCredential</span></span>
<span data-ttu-id="e6e56-117">클러스터에 대한 클러스터 로그인(HTTP) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e56-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="e6e56-118">-JobId</span></span>
<span data-ttu-id="e6e56-119">얻을 작업의 작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e56-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="e6e56-120">-NumOfJobs</span></span>
<span data-ttu-id="e6e56-121">검색할 작업 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e56-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6e56-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e6e56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e56-124">CommonParameters</span></span>
<span data-ttu-id="e6e56-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e56-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6e56-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e56-127">입력</span><span class="sxs-lookup"><span data-stu-id="e6e56-127">INPUTS</span></span>

### <span data-ttu-id="e6e56-128">없음</span><span class="sxs-lookup"><span data-stu-id="e6e56-128">None</span></span>

## <span data-ttu-id="e6e56-129">출력</span><span class="sxs-lookup"><span data-stu-id="e6e56-129">OUTPUTS</span></span>

### <span data-ttu-id="e6e56-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e56-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="e6e56-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6e56-131">NOTES</span></span>

## <span data-ttu-id="e6e56-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6e56-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6e56-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e6e56-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="e6e56-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e56-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="e6e56-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e56-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="e6e56-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e6e56-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


