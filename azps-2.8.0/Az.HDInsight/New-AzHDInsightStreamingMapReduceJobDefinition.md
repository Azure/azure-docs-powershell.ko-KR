---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 8fae0a8da7024ed49ee3d69a658431377b4f780f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689805"
---
# <span data-ttu-id="4ff69-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4ff69-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="4ff69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ff69-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff69-103">스트리밍 MapReduce 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="4ff69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ff69-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ff69-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4ff69-105">DESCRIPTION</span></span>
<span data-ttu-id="4ff69-106">**AzHDInsightStreamingMapReduceJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용할 스트리밍 MapReduce 작업 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4ff69-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4ff69-107">EXAMPLES</span></span>

### <span data-ttu-id="4ff69-108">예제 1: 스트리밍 MapReduce 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="4ff69-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="4ff69-109">이 명령은 스트리밍 MapReduce 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="4ff69-110">변수</span><span class="sxs-lookup"><span data-stu-id="4ff69-110">PARAMETERS</span></span>

### <span data-ttu-id="4ff69-111">-인수</span><span class="sxs-lookup"><span data-stu-id="4ff69-111">-Arguments</span></span>
<span data-ttu-id="4ff69-112">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="4ff69-113">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="4ff69-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="4ff69-114">-CommandEnvironment</span></span>
<span data-ttu-id="4ff69-115">작업을 작업자 노드에서 실행할 때 설정할 명령줄 환경 변수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="4ff69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff69-116">-DefaultProfile</span></span>
<span data-ttu-id="4ff69-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4ff69-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ff69-118">-정의</span><span class="sxs-lookup"><span data-stu-id="4ff69-118">-Defines</span></span>
<span data-ttu-id="4ff69-119">작업이 실행 될 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="4ff69-120">-파일</span><span class="sxs-lookup"><span data-stu-id="4ff69-120">-File</span></span>
<span data-ttu-id="4ff69-121">실행할 쿼리를 포함 하는 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="4ff69-122">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="4ff69-123">-파일</span><span class="sxs-lookup"><span data-stu-id="4ff69-123">-Files</span></span>
<span data-ttu-id="4ff69-124">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="4ff69-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="4ff69-125">-InputPath</span></span>
<span data-ttu-id="4ff69-126">입력 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="4ff69-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="4ff69-127">-Mapper</span></span>
<span data-ttu-id="4ff69-128">매퍼 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="4ff69-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="4ff69-129">-OutputPath</span></span>
<span data-ttu-id="4ff69-130">작업 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="4ff69-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="4ff69-131">-Reducer</span></span>
<span data-ttu-id="4ff69-132">Reducer 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="4ff69-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="4ff69-133">-StatusFolder</span></span>
<span data-ttu-id="4ff69-134">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="4ff69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff69-135">CommonParameters</span></span>
<span data-ttu-id="4ff69-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ff69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff69-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ff69-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff69-138">입력</span><span class="sxs-lookup"><span data-stu-id="4ff69-138">INPUTS</span></span>

### <span data-ttu-id="4ff69-139">않아야</span><span class="sxs-lookup"><span data-stu-id="4ff69-139">None</span></span>

## <span data-ttu-id="4ff69-140">출력</span><span class="sxs-lookup"><span data-stu-id="4ff69-140">OUTPUTS</span></span>

### <span data-ttu-id="4ff69-141">AzureHDInsightStreamingMapReduceJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="4ff69-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="4ff69-142">상속자</span><span class="sxs-lookup"><span data-stu-id="4ff69-142">NOTES</span></span>

## <span data-ttu-id="4ff69-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ff69-143">RELATED LINKS</span></span>

[<span data-ttu-id="4ff69-144">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="4ff69-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

