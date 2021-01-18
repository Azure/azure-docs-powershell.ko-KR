---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 4f9fe1ef3ab16812553eb6ea22909ce37bd5ee69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492940"
---
# <span data-ttu-id="245fa-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="245fa-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="245fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="245fa-102">SYNOPSIS</span></span>
<span data-ttu-id="245fa-103">Streaming MapReduce 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="245fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="245fa-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="245fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="245fa-105">DESCRIPTION</span></span>
<span data-ttu-id="245fa-106">**New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet은 Azure HDInsight 클러스터와 함께 사용할 스트리밍 MapReduce 작업 개체를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="245fa-107">예제</span><span class="sxs-lookup"><span data-stu-id="245fa-107">EXAMPLES</span></span>

### <span data-ttu-id="245fa-108">예제 1: 스트리밍 MapReduce 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="245fa-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="245fa-109">이 명령은 스트리밍 MapReduce 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="245fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="245fa-110">PARAMETERS</span></span>

### <span data-ttu-id="245fa-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="245fa-111">-Arguments</span></span>
<span data-ttu-id="245fa-112">작업의 인수 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="245fa-113">인수는 각 태스크에 명령줄 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="245fa-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="245fa-114">-CommandEnvironment</span></span>
<span data-ttu-id="245fa-115">작업이 작업 노드에서 실행될 때 설정할 명령줄 환경 변수의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245fa-116">-DefaultProfile</span></span>
<span data-ttu-id="245fa-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="245fa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="245fa-118">-Defines</span><span class="sxs-lookup"><span data-stu-id="245fa-118">-Defines</span></span>
<span data-ttu-id="245fa-119">작업이 실행되는 경우 설정할 Hadoop 구성 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-120">-File</span><span class="sxs-lookup"><span data-stu-id="245fa-120">-File</span></span>
<span data-ttu-id="245fa-121">실행할 쿼리가 포함된 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="245fa-122">쿼리 매개 변수 대신 이 매개 변수를 사용할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="245fa-123">-Files</span><span class="sxs-lookup"><span data-stu-id="245fa-123">-Files</span></span>
<span data-ttu-id="245fa-124">Hive 작업과 연결된 파일 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="245fa-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="245fa-125">-InputPath</span></span>
<span data-ttu-id="245fa-126">입력 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-126">Specifies the path to the input files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="245fa-127">-Mapper</span></span>
<span data-ttu-id="245fa-128">Mapper 파일 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="245fa-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="245fa-129">-OutputPath</span></span>
<span data-ttu-id="245fa-130">작업 출력에 대한 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="245fa-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="245fa-131">-Reducer</span></span>
<span data-ttu-id="245fa-132">Reducer 파일 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="245fa-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="245fa-133">-StatusFolder</span></span>
<span data-ttu-id="245fa-134">작업의 표준 출력 및 오류 출력이 포함된 폴더의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="245fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245fa-135">CommonParameters</span></span>
<span data-ttu-id="245fa-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="245fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245fa-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="245fa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245fa-138">입력</span><span class="sxs-lookup"><span data-stu-id="245fa-138">INPUTS</span></span>

### <span data-ttu-id="245fa-139">없음</span><span class="sxs-lookup"><span data-stu-id="245fa-139">None</span></span>

## <span data-ttu-id="245fa-140">출력</span><span class="sxs-lookup"><span data-stu-id="245fa-140">OUTPUTS</span></span>

### <span data-ttu-id="245fa-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="245fa-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="245fa-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="245fa-142">NOTES</span></span>

## <span data-ttu-id="245fa-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="245fa-143">RELATED LINKS</span></span>

[<span data-ttu-id="245fa-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="245fa-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


