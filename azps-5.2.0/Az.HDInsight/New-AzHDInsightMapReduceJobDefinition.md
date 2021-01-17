---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 45278426ee25337bd484a46b533c72f49dbe9586
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322965"
---
# <span data-ttu-id="f8fca-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f8fca-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="f8fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8fca-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fca-103">MapReduce 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="f8fca-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8fca-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8fca-105">설명</span><span class="sxs-lookup"><span data-stu-id="f8fca-105">DESCRIPTION</span></span>
<span data-ttu-id="f8fca-106">**New-AzHDInsightMapReduceJobDefinition** cmdlet은 Azure HDInsight 클러스터에서 사용할 새 MapReduce 작업을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f8fca-107">예제</span><span class="sxs-lookup"><span data-stu-id="f8fca-107">EXAMPLES</span></span>

### <span data-ttu-id="f8fca-108">예제 1: MapReduce 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="f8fca-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f8fca-109">이 명령은 MapReduce 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="f8fca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8fca-110">PARAMETERS</span></span>

### <span data-ttu-id="f8fca-111">-Arguments</span><span class="sxs-lookup"><span data-stu-id="f8fca-111">-Arguments</span></span>
<span data-ttu-id="f8fca-112">작업의 인수 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="f8fca-113">인수는 각 태스크에 명령줄 인수로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="f8fca-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="f8fca-114">-ClassName</span></span>
<span data-ttu-id="f8fca-115">JAR 파일의 작업 클래스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="f8fca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fca-116">-DefaultProfile</span></span>
<span data-ttu-id="f8fca-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f8fca-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8fca-118">-Defines</span><span class="sxs-lookup"><span data-stu-id="f8fca-118">-Defines</span></span>
<span data-ttu-id="f8fca-119">작업이 실행되는 경우 설정할 Hadoop 구성 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="f8fca-120">-Files</span><span class="sxs-lookup"><span data-stu-id="f8fca-120">-Files</span></span>
<span data-ttu-id="f8fca-121">Hive 작업과 연결된 파일 컬렉션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="f8fca-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="f8fca-122">-JarFile</span></span>
<span data-ttu-id="f8fca-123">작업에서 사용할 JAR 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="f8fca-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="f8fca-124">-JobName</span></span>
<span data-ttu-id="f8fca-125">작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="f8fca-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="f8fca-126">-LibJars</span></span>
<span data-ttu-id="f8fca-127">작업의 lib JARS를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="f8fca-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f8fca-128">-StatusFolder</span></span>
<span data-ttu-id="f8fca-129">작업의 표준 출력 및 오류 출력이 포함된 폴더의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="f8fca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fca-130">CommonParameters</span></span>
<span data-ttu-id="f8fca-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8fca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fca-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f8fca-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fca-133">입력</span><span class="sxs-lookup"><span data-stu-id="f8fca-133">INPUTS</span></span>

### <span data-ttu-id="f8fca-134">없음</span><span class="sxs-lookup"><span data-stu-id="f8fca-134">None</span></span>

## <span data-ttu-id="f8fca-135">출력</span><span class="sxs-lookup"><span data-stu-id="f8fca-135">OUTPUTS</span></span>

### <span data-ttu-id="f8fca-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f8fca-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="f8fca-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8fca-137">NOTES</span></span>

## <span data-ttu-id="f8fca-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8fca-138">RELATED LINKS</span></span>

[<span data-ttu-id="f8fca-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f8fca-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


