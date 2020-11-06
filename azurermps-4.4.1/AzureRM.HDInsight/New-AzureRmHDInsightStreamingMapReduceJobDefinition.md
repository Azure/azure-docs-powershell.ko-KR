---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 526f2005f1c6594128af7e259e2ccb0aa296a71b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536396"
---
# <span data-ttu-id="e8dfb-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e8dfb-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="e8dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="e8dfb-103">스트리밍 MapReduce 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8dfb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8dfb-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8dfb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e8dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="e8dfb-106">**AzureRmHDInsightStreamingMapReduceJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용할 스트리밍 MapReduce 작업 개체를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e8dfb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e8dfb-107">EXAMPLES</span></span>

### <span data-ttu-id="e8dfb-108">예제 1: 스트리밍 MapReduce 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="e8dfb-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="e8dfb-109">이 명령은 스트리밍 MapReduce 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="e8dfb-110">변수</span><span class="sxs-lookup"><span data-stu-id="e8dfb-110">PARAMETERS</span></span>

### <span data-ttu-id="e8dfb-111">-인수</span><span class="sxs-lookup"><span data-stu-id="e8dfb-111">-Arguments</span></span>
<span data-ttu-id="e8dfb-112">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="e8dfb-113">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e8dfb-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8dfb-114">-CommandEnvironment</span></span>
<span data-ttu-id="e8dfb-115">작업을 작업자 노드에서 실행할 때 설정할 명령줄 환경 변수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="e8dfb-116">-정의</span><span class="sxs-lookup"><span data-stu-id="e8dfb-116">-Defines</span></span>
<span data-ttu-id="e8dfb-117">작업이 실행 될 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="e8dfb-118">-파일</span><span class="sxs-lookup"><span data-stu-id="e8dfb-118">-File</span></span>
<span data-ttu-id="e8dfb-119">실행할 쿼리를 포함 하는 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-119">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="e8dfb-120">*쿼리* 매개 변수 대신이 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-120">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="e8dfb-121">-파일</span><span class="sxs-lookup"><span data-stu-id="e8dfb-121">-Files</span></span>
<span data-ttu-id="e8dfb-122">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-122">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="e8dfb-123">-InputPath</span><span class="sxs-lookup"><span data-stu-id="e8dfb-123">-InputPath</span></span>
<span data-ttu-id="e8dfb-124">입력 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-124">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="e8dfb-125">-Mapper</span><span class="sxs-lookup"><span data-stu-id="e8dfb-125">-Mapper</span></span>
<span data-ttu-id="e8dfb-126">매퍼 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-126">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="e8dfb-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e8dfb-127">-OutputPath</span></span>
<span data-ttu-id="e8dfb-128">작업 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-128">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="e8dfb-129">-Reducer</span><span class="sxs-lookup"><span data-stu-id="e8dfb-129">-Reducer</span></span>
<span data-ttu-id="e8dfb-130">Reducer 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-130">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="e8dfb-131">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e8dfb-131">-StatusFolder</span></span>
<span data-ttu-id="e8dfb-132">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-132">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="e8dfb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8dfb-133">-DefaultProfile</span></span>
<span data-ttu-id="e8dfb-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8dfb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8dfb-135">CommonParameters</span></span>
<span data-ttu-id="e8dfb-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8dfb-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8dfb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8dfb-138">입력</span><span class="sxs-lookup"><span data-stu-id="e8dfb-138">INPUTS</span></span>

## <span data-ttu-id="e8dfb-139">출력</span><span class="sxs-lookup"><span data-stu-id="e8dfb-139">OUTPUTS</span></span>

### <span data-ttu-id="e8dfb-140">AzureHDInsightStreamingMapReduceJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="e8dfb-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="e8dfb-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e8dfb-141">NOTES</span></span>

## <span data-ttu-id="e8dfb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8dfb-142">RELATED LINKS</span></span>

[<span data-ttu-id="e8dfb-143">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="e8dfb-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


