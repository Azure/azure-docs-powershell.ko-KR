---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349221"
---
# <span data-ttu-id="4c587-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4c587-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="4c587-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c587-102">SYNOPSIS</span></span>
<span data-ttu-id="4c587-103">Synapse Analytics Spark 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4c587-104">구문</span><span class="sxs-lookup"><span data-stu-id="4c587-104">SYNTAX</span></span>

### <span data-ttu-id="4c587-105">RunSparkJobParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4c587-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c587-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c587-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c587-107">설명</span><span class="sxs-lookup"><span data-stu-id="4c587-107">DESCRIPTION</span></span>
<span data-ttu-id="4c587-108">**Submit-AzSynapseSparkJob** cmdlet은 Synapse Analytics Spark 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4c587-109">예제</span><span class="sxs-lookup"><span data-stu-id="4c587-109">EXAMPLES</span></span>

### <span data-ttu-id="4c587-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4c587-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4c587-111">이 명령은 Synapse Analytics Spark 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="4c587-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="4c587-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4c587-113">이 명령은 Synapse Analytics Spark .NET 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="4c587-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="4c587-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="4c587-115">이 명령은 Synapse Analytics PySpark 작업을 제출합니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="4c587-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c587-116">PARAMETERS</span></span>

### <span data-ttu-id="4c587-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="4c587-117">-CommandLineArgument</span></span>
<span data-ttu-id="4c587-118">작업의 선택적 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-118">Optional arguments to the job.</span></span> <span data-ttu-id="4c587-119">예: "--iteration 10000 --timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="4c587-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="4c587-120">-Configuration</span><span class="sxs-lookup"><span data-stu-id="4c587-120">-Configuration</span></span>
<span data-ttu-id="4c587-121">Spark 구성 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="4c587-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c587-122">-DefaultProfile</span></span>
<span data-ttu-id="4c587-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c587-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="4c587-124">-ExecutorCount</span></span>
<span data-ttu-id="4c587-125">작업의 지정된 Spark 풀에 할당할 실행기 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="4c587-126">-ExecutorSize</span></span>
<span data-ttu-id="4c587-127">작업의 지정된 Spark 풀에 할당된 실행기에 사용할 코어 및 메모리의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-128">-Language</span><span class="sxs-lookup"><span data-stu-id="4c587-128">-Language</span></span>
<span data-ttu-id="4c587-129">제출할 작업의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="4c587-130">-MainClassName</span></span>
<span data-ttu-id="4c587-131">기본 정의 파일에 있는 기본 클래스 또는 정식 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="4c587-132">Spark 및 .NET Spark 작업에서 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="4c587-133">예: "org.apache.spark.examples.SparkPi"</span><span class="sxs-lookup"><span data-stu-id="4c587-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4c587-134">-MainDefinitionFile</span></span>
<span data-ttu-id="4c587-135">작업에서 사용되는 기본 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-135">The main file used for the job.</span></span>
<span data-ttu-id="4c587-136">예: abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="4c587-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="4c587-137">-Name</span><span class="sxs-lookup"><span data-stu-id="4c587-137">-Name</span></span>
<span data-ttu-id="4c587-138">Spark 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="4c587-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="4c587-139">-ReferenceFile</span></span>
<span data-ttu-id="4c587-140">기본 정의 파일의 참조에 사용되는 추가 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="4c587-141">콤마로 구분된 저장소 URI 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="4c587-142">예: " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="4c587-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="4c587-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4c587-143">-SparkPoolName</span></span>
<span data-ttu-id="4c587-144">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="4c587-145">-SparkPoolObject</span></span>
<span data-ttu-id="4c587-146">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4c587-147">-WorkspaceName</span></span>
<span data-ttu-id="4c587-148">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c587-149">-Confirm</span></span>
<span data-ttu-id="4c587-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c587-151">-WhatIf</span></span>
<span data-ttu-id="4c587-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4c587-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c587-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c587-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c587-154">CommonParameters</span></span>
<span data-ttu-id="4c587-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4c587-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c587-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c587-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c587-157">입력</span><span class="sxs-lookup"><span data-stu-id="4c587-157">INPUTS</span></span>

### <span data-ttu-id="4c587-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="4c587-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="4c587-159">출력</span><span class="sxs-lookup"><span data-stu-id="4c587-159">OUTPUTS</span></span>

### <span data-ttu-id="4c587-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4c587-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="4c587-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4c587-161">NOTES</span></span>

## <span data-ttu-id="4c587-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c587-162">RELATED LINKS</span></span>
