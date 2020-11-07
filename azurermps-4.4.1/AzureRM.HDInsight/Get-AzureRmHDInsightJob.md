---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: e3cfd7978ecd7f8395a0c499d3d194f133960a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703115"
---
# <span data-ttu-id="49b9b-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="49b9b-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="49b9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="49b9b-103">클러스터의 작업 목록을 가져와 그 순서 대로 역순으로 나열 하거나 특정 작업을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49b9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49b9b-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49b9b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="49b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="49b9b-106">**AzureRmHDInsightJob** cmdlet은 지정 된 Azure HDInsight 클러스터에 대 한 최근 작업을 목록의 맨 위에 가장 최근 작업으로 표시 되는 순서 대로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="49b9b-107">*JobId* 매개 변수를 제공 하 여 특정 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="49b9b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="49b9b-108">EXAMPLES</span></span>

### <span data-ttu-id="49b9b-109">예제 1: 지정 된 Azure HDInsight 클러스터에 대 한 최근 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="49b9b-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="49b9b-110">이 명령은-hadoop-001 이라는 클러스터에 대 한 최근 작업을 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="49b9b-111">변수</span><span class="sxs-lookup"><span data-stu-id="49b9b-111">PARAMETERS</span></span>

### <span data-ttu-id="49b9b-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="49b9b-112">-ClusterName</span></span>
<span data-ttu-id="49b9b-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="49b9b-114">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="49b9b-114">-HttpCredential</span></span>
<span data-ttu-id="49b9b-115">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-115">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="49b9b-116">-JobId</span><span class="sxs-lookup"><span data-stu-id="49b9b-116">-JobId</span></span>
<span data-ttu-id="49b9b-117">가져올 작업의 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-117">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="49b9b-118">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="49b9b-118">-NumOfJobs</span></span>
<span data-ttu-id="49b9b-119">검색할 작업의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-119">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="49b9b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b9b-120">-ResourceGroupName</span></span>
<span data-ttu-id="49b9b-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="49b9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b9b-122">-DefaultProfile</span></span>
<span data-ttu-id="49b9b-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b9b-124">CommonParameters</span></span>
<span data-ttu-id="49b9b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49b9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b9b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b9b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b9b-127">입력</span><span class="sxs-lookup"><span data-stu-id="49b9b-127">INPUTS</span></span>

## <span data-ttu-id="49b9b-128">출력</span><span class="sxs-lookup"><span data-stu-id="49b9b-128">OUTPUTS</span></span>

### <span data-ttu-id="49b9b-129">AzureHDInsightJob의. m m.</span><span class="sxs-lookup"><span data-stu-id="49b9b-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="49b9b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="49b9b-130">NOTES</span></span>

## <span data-ttu-id="49b9b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49b9b-131">RELATED LINKS</span></span>

[<span data-ttu-id="49b9b-132">새로운 AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="49b9b-132">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="49b9b-133">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="49b9b-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="49b9b-134">중지-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="49b9b-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="49b9b-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="49b9b-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


