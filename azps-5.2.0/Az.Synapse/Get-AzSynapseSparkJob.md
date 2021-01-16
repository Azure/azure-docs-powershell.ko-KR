---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339110"
---
# <span data-ttu-id="8aa70-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="8aa70-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="8aa70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa70-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa70-103">Synapse Analytics Spark 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="8aa70-104">구문</span><span class="sxs-lookup"><span data-stu-id="8aa70-104">SYNTAX</span></span>

### <span data-ttu-id="8aa70-105">GetSparkJobsByIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8aa70-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa70-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8aa70-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8aa70-107">설명</span><span class="sxs-lookup"><span data-stu-id="8aa70-107">DESCRIPTION</span></span>
<span data-ttu-id="8aa70-108">**Get-AzSynapseSparkJob** cmdlet은 Azure Synapse Analytics Spark 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="8aa70-109">작업을 지정하지 않으면 이 cmdlet은 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="8aa70-110">예제</span><span class="sxs-lookup"><span data-stu-id="8aa70-110">EXAMPLES</span></span>

### <span data-ttu-id="8aa70-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8aa70-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="8aa70-112">이 명령은 Spark 풀에서 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="8aa70-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8aa70-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="8aa70-114">이 명령은 지정된 ID를 사용하여 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="8aa70-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="8aa70-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="8aa70-116">이 명령은 지정된 애플리케이션 ID를 사용하여 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="8aa70-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="8aa70-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="8aa70-118">이 명령은 파이프라인을 통해 Spark 풀의 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="8aa70-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aa70-119">PARAMETERS</span></span>

### <span data-ttu-id="8aa70-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8aa70-120">-ApplicationId</span></span>
<span data-ttu-id="8aa70-121">세션의 애플리케이션 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="8aa70-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa70-122">-DefaultProfile</span></span>
<span data-ttu-id="8aa70-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aa70-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="8aa70-124">-LivyId</span></span>
<span data-ttu-id="8aa70-125">Spark 작업의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa70-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8aa70-126">-Name</span></span>
<span data-ttu-id="8aa70-127">Spark 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="8aa70-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8aa70-128">-SparkPoolName</span></span>
<span data-ttu-id="8aa70-129">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa70-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="8aa70-130">-SparkPoolObject</span></span>
<span data-ttu-id="8aa70-131">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa70-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8aa70-132">-WorkspaceName</span></span>
<span data-ttu-id="8aa70-133">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa70-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa70-134">CommonParameters</span></span>
<span data-ttu-id="8aa70-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa70-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa70-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8aa70-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa70-137">입력</span><span class="sxs-lookup"><span data-stu-id="8aa70-137">INPUTS</span></span>

### <span data-ttu-id="8aa70-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8aa70-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="8aa70-139">출력</span><span class="sxs-lookup"><span data-stu-id="8aa70-139">OUTPUTS</span></span>

### <span data-ttu-id="8aa70-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="8aa70-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="8aa70-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8aa70-141">NOTES</span></span>

## <span data-ttu-id="8aa70-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8aa70-142">RELATED LINKS</span></span>