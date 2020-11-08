---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049059"
---
# <span data-ttu-id="2aa39-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2aa39-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="2aa39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aa39-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa39-103">스트리밍 MapReduce 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="2aa39-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2aa39-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2aa39-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2aa39-105">DESCRIPTION</span></span>
<span data-ttu-id="2aa39-106">**AzHDInsightStreamingMapReduceJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용할 스트리밍 MapReduce 작업 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2aa39-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2aa39-107">EXAMPLES</span></span>

### <span data-ttu-id="2aa39-108">예제 1: 스트리밍 MapReduce 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="2aa39-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="2aa39-109">이 명령은 스트리밍 MapReduce 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="2aa39-110">변수</span><span class="sxs-lookup"><span data-stu-id="2aa39-110">PARAMETERS</span></span>

### <span data-ttu-id="2aa39-111">-인수</span><span class="sxs-lookup"><span data-stu-id="2aa39-111">-Arguments</span></span>
<span data-ttu-id="2aa39-112">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="2aa39-113">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="2aa39-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="2aa39-114">-CommandEnvironment</span></span>
<span data-ttu-id="2aa39-115">작업을 작업자 노드에서 실행할 때 설정할 명령줄 환경 변수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="2aa39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa39-116">-DefaultProfile</span></span>
<span data-ttu-id="2aa39-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2aa39-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aa39-118">-정의</span><span class="sxs-lookup"><span data-stu-id="2aa39-118">-Defines</span></span>
<span data-ttu-id="2aa39-119">작업이 실행 될 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="2aa39-120">-파일</span><span class="sxs-lookup"><span data-stu-id="2aa39-120">-File</span></span>
<span data-ttu-id="2aa39-121">실행할 쿼리를 포함 하는 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="2aa39-122">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="2aa39-123">-파일</span><span class="sxs-lookup"><span data-stu-id="2aa39-123">-Files</span></span>
<span data-ttu-id="2aa39-124">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="2aa39-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="2aa39-125">-InputPath</span></span>
<span data-ttu-id="2aa39-126">입력 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="2aa39-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="2aa39-127">-Mapper</span></span>
<span data-ttu-id="2aa39-128">매퍼 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="2aa39-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="2aa39-129">-OutputPath</span></span>
<span data-ttu-id="2aa39-130">작업 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="2aa39-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="2aa39-131">-Reducer</span></span>
<span data-ttu-id="2aa39-132">Reducer 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="2aa39-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="2aa39-133">-StatusFolder</span></span>
<span data-ttu-id="2aa39-134">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="2aa39-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa39-135">CommonParameters</span></span>
<span data-ttu-id="2aa39-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2aa39-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa39-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa39-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa39-138">입력</span><span class="sxs-lookup"><span data-stu-id="2aa39-138">INPUTS</span></span>

### <span data-ttu-id="2aa39-139">않아야</span><span class="sxs-lookup"><span data-stu-id="2aa39-139">None</span></span>

## <span data-ttu-id="2aa39-140">출력</span><span class="sxs-lookup"><span data-stu-id="2aa39-140">OUTPUTS</span></span>

### <span data-ttu-id="2aa39-141">AzureHDInsightStreamingMapReduceJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="2aa39-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="2aa39-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2aa39-142">NOTES</span></span>

## <span data-ttu-id="2aa39-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2aa39-143">RELATED LINKS</span></span>

[<span data-ttu-id="2aa39-144">시작-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2aa39-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


