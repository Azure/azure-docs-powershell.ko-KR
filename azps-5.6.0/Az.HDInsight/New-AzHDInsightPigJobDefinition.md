---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: abe1a0eaa03d498e151a58d5970f85be088e489e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984643"
---
# <span data-ttu-id="65866-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="65866-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="65866-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65866-102">SYNOPSIS</span></span>
<span data-ttu-id="65866-103">Pig 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65866-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="65866-104">구문</span><span class="sxs-lookup"><span data-stu-id="65866-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65866-105">설명</span><span class="sxs-lookup"><span data-stu-id="65866-105">DESCRIPTION</span></span>
<span data-ttu-id="65866-106">**New-AzHDInsightPigJobDefinition** cmdlet은 Azure HDInsight 클러스터와 함께 사용할 Pig 작업 개체를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="65866-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="65866-107">예제</span><span class="sxs-lookup"><span data-stu-id="65866-107">EXAMPLES</span></span>

### <span data-ttu-id="65866-108">예제 1: Pig 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="65866-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="65866-109">이 명령은 Pig 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65866-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="65866-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65866-110">PARAMETERS</span></span>

### <span data-ttu-id="65866-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="65866-111">-Arguments</span></span>
<span data-ttu-id="65866-112">작업의 인수 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65866-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="65866-113">인수는 각 작업에 명령줄 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="65866-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65866-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65866-114">-DefaultProfile</span></span>
<span data-ttu-id="65866-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="65866-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65866-116">-File</span><span class="sxs-lookup"><span data-stu-id="65866-116">-File</span></span>
<span data-ttu-id="65866-117">실행할 쿼리가 포함된 파일에 대한 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65866-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="65866-118">클러스터와 연결된 저장소 계정에서 파일을 사용할 수 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65866-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="65866-119">쿼리 매개 변수 대신 이 매개 변수를 *사용할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65866-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="65866-120">-Files</span><span class="sxs-lookup"><span data-stu-id="65866-120">-Files</span></span>
<span data-ttu-id="65866-121">Hive 작업과 연결된 파일 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65866-121">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65866-122">-쿼리</span><span class="sxs-lookup"><span data-stu-id="65866-122">-Query</span></span>
<span data-ttu-id="65866-123">Pig 쿼리를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65866-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="65866-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="65866-124">-StatusFolder</span></span>
<span data-ttu-id="65866-125">작업의 표준 출력 및 오류 출력이 포함된 폴더의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65866-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="65866-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65866-126">CommonParameters</span></span>
<span data-ttu-id="65866-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65866-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65866-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65866-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65866-129">입력</span><span class="sxs-lookup"><span data-stu-id="65866-129">INPUTS</span></span>

### <span data-ttu-id="65866-130">없음</span><span class="sxs-lookup"><span data-stu-id="65866-130">None</span></span>

## <span data-ttu-id="65866-131">출력</span><span class="sxs-lookup"><span data-stu-id="65866-131">OUTPUTS</span></span>

### <span data-ttu-id="65866-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="65866-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="65866-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65866-133">NOTES</span></span>

## <span data-ttu-id="65866-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65866-134">RELATED LINKS</span></span>

[<span data-ttu-id="65866-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="65866-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


