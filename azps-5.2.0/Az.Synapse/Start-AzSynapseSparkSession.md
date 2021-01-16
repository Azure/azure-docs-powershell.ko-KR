---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335541"
---
# <span data-ttu-id="c6a06-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c6a06-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="c6a06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a06-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a06-103">Synapse Analytics Spark 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="c6a06-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6a06-104">SYNTAX</span></span>

### <span data-ttu-id="c6a06-105">CreateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c6a06-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6a06-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6a06-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6a06-107">설명</span><span class="sxs-lookup"><span data-stu-id="c6a06-107">DESCRIPTION</span></span>
<span data-ttu-id="c6a06-108">**Start-AzSynapseSparkSession** cmdlet은 Synapse Analytics Spark 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="c6a06-109">예제</span><span class="sxs-lookup"><span data-stu-id="c6a06-109">EXAMPLES</span></span>

### <span data-ttu-id="c6a06-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6a06-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="c6a06-111">이 명령은 Azure Synapse Analytics Spark 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="c6a06-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c6a06-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="c6a06-113">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="c6a06-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6a06-114">PARAMETERS</span></span>

### <span data-ttu-id="c6a06-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6a06-115">-AsJob</span></span>
<span data-ttu-id="c6a06-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c6a06-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a06-117">-Configuration</span><span class="sxs-lookup"><span data-stu-id="c6a06-117">-Configuration</span></span>
<span data-ttu-id="c6a06-118">Spark 구성 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="c6a06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a06-119">-DefaultProfile</span></span>
<span data-ttu-id="c6a06-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6a06-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="c6a06-121">-ExecutorCount</span></span>
<span data-ttu-id="c6a06-122">작업의 지정된 Spark 풀에 할당할 실행기 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="c6a06-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="c6a06-123">-ExecutorSize</span></span>
<span data-ttu-id="c6a06-124">작업의 지정된 Spark 풀에 할당된 실행기에 사용할 코어 및 메모리의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="c6a06-125">-Language</span><span class="sxs-lookup"><span data-stu-id="c6a06-125">-Language</span></span>
<span data-ttu-id="c6a06-126">실행 코드의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a06-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c6a06-127">-Name</span></span>
<span data-ttu-id="c6a06-128">Spark 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="c6a06-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="c6a06-129">-ReferenceFile</span></span>
<span data-ttu-id="c6a06-130">기본 정의 파일의 참조에 사용되는 추가 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="c6a06-131">콤마로 구분된 저장소 URI 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="c6a06-132">예: " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="c6a06-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="c6a06-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c6a06-133">-SparkPoolName</span></span>
<span data-ttu-id="c6a06-134">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a06-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="c6a06-135">-SparkPoolObject</span></span>
<span data-ttu-id="c6a06-136">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a06-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c6a06-137">-WorkspaceName</span></span>
<span data-ttu-id="c6a06-138">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a06-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6a06-139">-Confirm</span></span>
<span data-ttu-id="c6a06-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6a06-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6a06-141">-WhatIf</span></span>
<span data-ttu-id="c6a06-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c6a06-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6a06-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6a06-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a06-144">CommonParameters</span></span>
<span data-ttu-id="c6a06-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6a06-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a06-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6a06-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a06-147">입력</span><span class="sxs-lookup"><span data-stu-id="c6a06-147">INPUTS</span></span>

### <span data-ttu-id="c6a06-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c6a06-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c6a06-149">출력</span><span class="sxs-lookup"><span data-stu-id="c6a06-149">OUTPUTS</span></span>

### <span data-ttu-id="c6a06-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c6a06-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c6a06-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6a06-151">NOTES</span></span>

## <span data-ttu-id="c6a06-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6a06-152">RELATED LINKS</span></span>
