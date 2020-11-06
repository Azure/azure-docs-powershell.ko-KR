---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 3d40596b5797ca6b08b896e9ca973e491d130017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531043"
---
# <span data-ttu-id="64f46-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="64f46-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="64f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f46-102">SYNOPSIS</span></span>
<span data-ttu-id="64f46-103">MapReduce 작업 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64f46-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64f46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="64f46-105">DESCRIPTION</span></span>
<span data-ttu-id="64f46-106">**AzureRmHDInsightMapReduceJobDefinition** Cmdlet은 Azure HDInsight 클러스터와 함께 사용할 새 MapReduce 작업을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="64f46-107">예제의</span><span class="sxs-lookup"><span data-stu-id="64f46-107">EXAMPLES</span></span>

### <span data-ttu-id="64f46-108">예제 1: MapReduce 작업 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="64f46-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="64f46-109">이 명령은 MapReduce 작업 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="64f46-110">변수</span><span class="sxs-lookup"><span data-stu-id="64f46-110">PARAMETERS</span></span>

### <span data-ttu-id="64f46-111">-인수</span><span class="sxs-lookup"><span data-stu-id="64f46-111">-Arguments</span></span>
<span data-ttu-id="64f46-112">작업에 대 한 인수 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="64f46-113">인수는 각 작업에 명령줄 인수로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-113">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="64f46-114">-ClassName</span></span>
<span data-ttu-id="64f46-115">JAR 파일의 작업 클래스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-115">Specifies the job class in the JAR file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f46-116">-DefaultProfile</span></span>
<span data-ttu-id="64f46-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="64f46-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-118">-정의</span><span class="sxs-lookup"><span data-stu-id="64f46-118">-Defines</span></span>
<span data-ttu-id="64f46-119">작업이 실행 될 때 설정할 Hadoop 구성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-120">-파일</span><span class="sxs-lookup"><span data-stu-id="64f46-120">-Files</span></span>
<span data-ttu-id="64f46-121">Hive 작업과 연결 된 파일의 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-121">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="64f46-122">-JarFile</span></span>
<span data-ttu-id="64f46-123">작업에 사용할 JAR 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-123">Specifies the JAR file to use for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="64f46-124">-JobName</span></span>
<span data-ttu-id="64f46-125">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-125">Specifies the name of the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="64f46-126">-LibJars</span></span>
<span data-ttu-id="64f46-127">작업에 대 한 lib JARS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-127">Specifies the lib JARS for the job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="64f46-128">-StatusFolder</span></span>
<span data-ttu-id="64f46-129">작업에 대 한 표준 출력 및 오류 출력을 포함 하는 폴더의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f46-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f46-130">CommonParameters</span></span>
<span data-ttu-id="64f46-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f46-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f46-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f46-133">입력</span><span class="sxs-lookup"><span data-stu-id="64f46-133">INPUTS</span></span>

### <span data-ttu-id="64f46-134">않아야</span><span class="sxs-lookup"><span data-stu-id="64f46-134">None</span></span>
<span data-ttu-id="64f46-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64f46-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64f46-136">출력</span><span class="sxs-lookup"><span data-stu-id="64f46-136">OUTPUTS</span></span>

### <span data-ttu-id="64f46-137">AzureHDInsightMapReduceJobDefinition의. m m.</span><span class="sxs-lookup"><span data-stu-id="64f46-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="64f46-138">상속자</span><span class="sxs-lookup"><span data-stu-id="64f46-138">NOTES</span></span>

## <span data-ttu-id="64f46-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64f46-139">RELATED LINKS</span></span>

[<span data-ttu-id="64f46-140">시작-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="64f46-140">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


