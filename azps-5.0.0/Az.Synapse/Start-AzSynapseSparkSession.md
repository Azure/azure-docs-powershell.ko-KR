---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217958"
---
# <span data-ttu-id="f4227-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="f4227-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="f4227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4227-102">SYNOPSIS</span></span>
<span data-ttu-id="f4227-103">Synapse Analytics Spark 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="f4227-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4227-104">SYNTAX</span></span>

### <span data-ttu-id="f4227-105">CreateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f4227-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4227-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4227-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4227-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f4227-107">DESCRIPTION</span></span>
<span data-ttu-id="f4227-108">**AzSynapseSparkSession** Cmdlet은 Synapse Analytics Spark 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="f4227-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f4227-109">EXAMPLES</span></span>

### <span data-ttu-id="f4227-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4227-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="f4227-111">이 명령은 Azure Synapse Analytics Spark 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="f4227-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f4227-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="f4227-113">이 명령은 파이프라인을 통해 Azure Synapse Analytics Spark 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="f4227-114">변수</span><span class="sxs-lookup"><span data-stu-id="f4227-114">PARAMETERS</span></span>

### <span data-ttu-id="f4227-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4227-115">-AsJob</span></span>
<span data-ttu-id="f4227-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f4227-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4227-117">-구성</span><span class="sxs-lookup"><span data-stu-id="f4227-117">-Configuration</span></span>
<span data-ttu-id="f4227-118">Spark 구성 속성</span><span class="sxs-lookup"><span data-stu-id="f4227-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="f4227-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4227-119">-DefaultProfile</span></span>
<span data-ttu-id="f4227-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4227-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="f4227-121">-ExecutorCount</span></span>
<span data-ttu-id="f4227-122">작업에 대해 지정 된 Spark 풀에 할당할 실행자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="f4227-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="f4227-123">-ExecutorSize</span></span>
<span data-ttu-id="f4227-124">작업에 대해 지정 된 Spark 풀에 할당 된 실행자에 사용 되는 코어 및 메모리의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="f4227-125">-언어</span><span class="sxs-lookup"><span data-stu-id="f4227-125">-Language</span></span>
<span data-ttu-id="f4227-126">실행 코드의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-126">Language of the execution code.</span></span>

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

### <span data-ttu-id="f4227-127">-이름</span><span class="sxs-lookup"><span data-stu-id="f4227-127">-Name</span></span>
<span data-ttu-id="f4227-128">Spark 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="f4227-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="f4227-129">-ReferenceFile</span></span>
<span data-ttu-id="f4227-130">기본 정의 파일에서 참조에 사용 되는 추가 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="f4227-131">쉼표로 구분 된 저장소 URI 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="f4227-132">예: " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="f4227-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

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

### <span data-ttu-id="f4227-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f4227-133">-SparkPoolName</span></span>
<span data-ttu-id="f4227-134">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-134">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f4227-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="f4227-135">-SparkPoolObject</span></span>
<span data-ttu-id="f4227-136">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-136">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f4227-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f4227-137">-WorkspaceName</span></span>
<span data-ttu-id="f4227-138">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f4227-139">-확인</span><span class="sxs-lookup"><span data-stu-id="f4227-139">-Confirm</span></span>
<span data-ttu-id="f4227-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4227-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4227-141">-WhatIf</span></span>
<span data-ttu-id="f4227-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4227-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4227-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4227-144">CommonParameters</span></span>
<span data-ttu-id="f4227-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4227-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4227-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4227-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4227-147">입력</span><span class="sxs-lookup"><span data-stu-id="f4227-147">INPUTS</span></span>

### <span data-ttu-id="f4227-148">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="f4227-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="f4227-149">출력</span><span class="sxs-lookup"><span data-stu-id="f4227-149">OUTPUTS</span></span>

### <span data-ttu-id="f4227-150">Synapse. PSSynapseSparkSession/.</span><span class="sxs-lookup"><span data-stu-id="f4227-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="f4227-151">상속자</span><span class="sxs-lookup"><span data-stu-id="f4227-151">NOTES</span></span>

## <span data-ttu-id="f4227-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4227-152">RELATED LINKS</span></span>
