---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: b2ba2144eccd3069453daa1ada15527539400c22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215369"
---
# <span data-ttu-id="a3f79-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a3f79-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="a3f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3f79-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f79-103">클러스터의 작업 목록을 가져와 그 순서 대로 역순으로 나열 하거나 특정 작업을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="a3f79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3f79-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3f79-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a3f79-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f79-106">**AzHDInsightJob** cmdlet은 지정 된 Azure HDInsight 클러스터에 대 한 최근 작업을 목록의 맨 위에 가장 최근 작업으로 표시 되는 순서 대로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="a3f79-107">*JobId* 매개 변수를 제공 하 여 특정 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="a3f79-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a3f79-108">EXAMPLES</span></span>

### <span data-ttu-id="a3f79-109">예제 1: 지정 된 Azure HDInsight 클러스터에 대 한 최근 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="a3f79-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
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

<span data-ttu-id="a3f79-110">이 명령은-hadoop-001 이라는 클러스터에 대 한 최근 작업을 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a3f79-111">변수</span><span class="sxs-lookup"><span data-stu-id="a3f79-111">PARAMETERS</span></span>

### <span data-ttu-id="a3f79-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a3f79-112">-ClusterName</span></span>
<span data-ttu-id="a3f79-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a3f79-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f79-114">-DefaultProfile</span></span>
<span data-ttu-id="a3f79-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a3f79-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3f79-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a3f79-116">-HttpCredential</span></span>
<span data-ttu-id="a3f79-117">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="a3f79-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="a3f79-118">-JobId</span></span>
<span data-ttu-id="a3f79-119">가져올 작업의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="a3f79-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="a3f79-120">-NumOfJobs</span></span>
<span data-ttu-id="a3f79-121">검색할 작업의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="a3f79-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f79-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3f79-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a3f79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f79-124">CommonParameters</span></span>
<span data-ttu-id="a3f79-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3f79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f79-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f79-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f79-127">입력</span><span class="sxs-lookup"><span data-stu-id="a3f79-127">INPUTS</span></span>

### <span data-ttu-id="a3f79-128">않아야</span><span class="sxs-lookup"><span data-stu-id="a3f79-128">None</span></span>

## <span data-ttu-id="a3f79-129">출력</span><span class="sxs-lookup"><span data-stu-id="a3f79-129">OUTPUTS</span></span>

### <span data-ttu-id="a3f79-130">AzureHDInsightJob의. m m.</span><span class="sxs-lookup"><span data-stu-id="a3f79-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="a3f79-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a3f79-131">NOTES</span></span>

## <span data-ttu-id="a3f79-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3f79-132">RELATED LINKS</span></span>

[<span data-ttu-id="a3f79-133">새로운 AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a3f79-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="a3f79-134">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a3f79-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="a3f79-135">중지-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a3f79-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="a3f79-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a3f79-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


