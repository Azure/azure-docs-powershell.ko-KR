---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372681"
---
# <span data-ttu-id="49511-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="49511-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="49511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49511-102">SYNOPSIS</span></span>
<span data-ttu-id="49511-103">Synapse Analytics Spark 작업이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49511-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="49511-104">구문</span><span class="sxs-lookup"><span data-stu-id="49511-104">SYNTAX</span></span>

### <span data-ttu-id="49511-105">WaitSparkJobByIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="49511-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49511-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49511-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49511-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49511-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49511-108">설명</span><span class="sxs-lookup"><span data-stu-id="49511-108">DESCRIPTION</span></span>
<span data-ttu-id="49511-109">**Wait-AzSynapseSparkJob** cmdlet은 Azure Synapse Analytics 작업이 완료될 때까지 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="49511-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="49511-110">예제</span><span class="sxs-lookup"><span data-stu-id="49511-110">EXAMPLES</span></span>

### <span data-ttu-id="49511-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="49511-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="49511-112">이 명령은 지정된 ID를 사용하여 작업이 완료될 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49511-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="49511-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49511-113">PARAMETERS</span></span>

### <span data-ttu-id="49511-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49511-114">-DefaultProfile</span></span>
<span data-ttu-id="49511-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49511-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49511-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="49511-116">-LivyId</span></span>
<span data-ttu-id="49511-117">Spark 작업의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="49511-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49511-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="49511-118">-SparkJobObject</span></span>
<span data-ttu-id="49511-119">Spark 작업 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="49511-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49511-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="49511-120">-SparkPoolName</span></span>
<span data-ttu-id="49511-121">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49511-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49511-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="49511-122">-SparkPoolObject</span></span>
<span data-ttu-id="49511-123">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="49511-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49511-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="49511-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="49511-125">오류가 발생하기 전에 대기할 최대 시간입니다. 기본값은 시간 제한이 없는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="49511-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49511-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="49511-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="49511-127">작업 상태에 대한 검사 사이의 폴링 간격(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="49511-127">The polling interval between checks for the job status, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49511-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="49511-128">-WorkspaceName</span></span>
<span data-ttu-id="49511-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49511-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49511-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49511-130">CommonParameters</span></span>
<span data-ttu-id="49511-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49511-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49511-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="49511-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49511-133">입력</span><span class="sxs-lookup"><span data-stu-id="49511-133">INPUTS</span></span>

### <span data-ttu-id="49511-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="49511-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="49511-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="49511-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="49511-136">출력</span><span class="sxs-lookup"><span data-stu-id="49511-136">OUTPUTS</span></span>

### <span data-ttu-id="49511-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49511-137">System.Boolean</span></span>

## <span data-ttu-id="49511-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49511-138">NOTES</span></span>

## <span data-ttu-id="49511-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49511-139">RELATED LINKS</span></span>
