---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204181"
---
# <span data-ttu-id="dcfed-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="dcfed-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="dcfed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcfed-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfed-103">Synapse Analytics Spark 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="dcfed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dcfed-104">SYNTAX</span></span>

### <span data-ttu-id="dcfed-105">RunSparkJobParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="dcfed-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcfed-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcfed-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcfed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dcfed-107">DESCRIPTION</span></span>
<span data-ttu-id="dcfed-108">**AzSynapseSparkJob** Cmdlet은 Synapse Analytics Spark 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="dcfed-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dcfed-109">EXAMPLES</span></span>

### <span data-ttu-id="dcfed-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dcfed-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="dcfed-111">이 명령은 Synapse Analytics Spark 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="dcfed-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="dcfed-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="dcfed-113">이 명령은 Synapse Analytics Spark .NET 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="dcfed-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="dcfed-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="dcfed-115">이 명령은 Synapse Analytics PySpark job을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="dcfed-116">변수</span><span class="sxs-lookup"><span data-stu-id="dcfed-116">PARAMETERS</span></span>

### <span data-ttu-id="dcfed-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="dcfed-117">-CommandLineArgument</span></span>
<span data-ttu-id="dcfed-118">작업에 대 한 선택적 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-118">Optional arguments to the job.</span></span> <span data-ttu-id="dcfed-119">예: "--이터레이션 1만--timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="dcfed-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

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

### <span data-ttu-id="dcfed-120">-구성</span><span class="sxs-lookup"><span data-stu-id="dcfed-120">-Configuration</span></span>
<span data-ttu-id="dcfed-121">Spark 구성 속성</span><span class="sxs-lookup"><span data-stu-id="dcfed-121">Spark configuration properties.</span></span>

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

### <span data-ttu-id="dcfed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfed-122">-DefaultProfile</span></span>
<span data-ttu-id="dcfed-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcfed-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="dcfed-124">-ExecutorCount</span></span>
<span data-ttu-id="dcfed-125">작업에 대해 지정 된 Spark 풀에 할당할 실행자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="dcfed-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="dcfed-126">-ExecutorSize</span></span>
<span data-ttu-id="dcfed-127">작업에 대해 지정 된 Spark 풀에 할당 된 실행자에 사용 되는 코어 및 메모리의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="dcfed-128">-언어</span><span class="sxs-lookup"><span data-stu-id="dcfed-128">-Language</span></span>
<span data-ttu-id="dcfed-129">제출할 작업의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-129">Language of the job to submit.</span></span>

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

### <span data-ttu-id="dcfed-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="dcfed-130">-MainClassName</span></span>
<span data-ttu-id="dcfed-131">정규화 된 식별자 또는 기본 정의 파일에 있는 기본 클래스입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="dcfed-132">Spark 및 .NET Spark 작업에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="dcfed-133">예를 들어 "SparkPi"</span><span class="sxs-lookup"><span data-stu-id="dcfed-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

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

### <span data-ttu-id="dcfed-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="dcfed-134">-MainDefinitionFile</span></span>
<span data-ttu-id="dcfed-135">작업에 사용 되는 기본 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-135">The main file used for the job.</span></span>
<span data-ttu-id="dcfed-136">예: " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="dcfed-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

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

### <span data-ttu-id="dcfed-137">-이름</span><span class="sxs-lookup"><span data-stu-id="dcfed-137">-Name</span></span>
<span data-ttu-id="dcfed-138">Spark 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-138">Name of Spark job.</span></span>

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

### <span data-ttu-id="dcfed-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="dcfed-139">-ReferenceFile</span></span>
<span data-ttu-id="dcfed-140">기본 정의 파일에서 참조에 사용 되는 추가 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="dcfed-141">쉼표로 구분 된 저장소 URI 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="dcfed-142">예: " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="dcfed-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="dcfed-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="dcfed-143">-SparkPoolName</span></span>
<span data-ttu-id="dcfed-144">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-144">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="dcfed-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="dcfed-145">-SparkPoolObject</span></span>
<span data-ttu-id="dcfed-146">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-146">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dcfed-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dcfed-147">-WorkspaceName</span></span>
<span data-ttu-id="dcfed-148">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-148">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dcfed-149">-확인</span><span class="sxs-lookup"><span data-stu-id="dcfed-149">-Confirm</span></span>
<span data-ttu-id="dcfed-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcfed-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcfed-151">-WhatIf</span></span>
<span data-ttu-id="dcfed-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcfed-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcfed-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfed-154">CommonParameters</span></span>
<span data-ttu-id="dcfed-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcfed-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcfed-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dcfed-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfed-157">입력</span><span class="sxs-lookup"><span data-stu-id="dcfed-157">INPUTS</span></span>

### <span data-ttu-id="dcfed-158">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="dcfed-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="dcfed-159">출력</span><span class="sxs-lookup"><span data-stu-id="dcfed-159">OUTPUTS</span></span>

### <span data-ttu-id="dcfed-160">Synapse. PSSynapseSparkJob/.</span><span class="sxs-lookup"><span data-stu-id="dcfed-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="dcfed-161">상속자</span><span class="sxs-lookup"><span data-stu-id="dcfed-161">NOTES</span></span>

## <span data-ttu-id="dcfed-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcfed-162">RELATED LINKS</span></span>
