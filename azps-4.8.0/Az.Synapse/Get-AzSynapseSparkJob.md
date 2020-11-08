---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213165"
---
# <span data-ttu-id="4d78b-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4d78b-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="4d78b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d78b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d78b-103">Synapse Analytics Spark 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="4d78b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d78b-104">SYNTAX</span></span>

### <span data-ttu-id="4d78b-105">GetSparkJobsByIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d78b-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d78b-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d78b-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d78b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d78b-107">DESCRIPTION</span></span>
<span data-ttu-id="4d78b-108">**AzSynapseSparkJob** Cmdlet은 Azure Synapse Analytics Spark 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="4d78b-109">작업을 지정 하지 않으면이 cmdlet은 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="4d78b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4d78b-110">EXAMPLES</span></span>

### <span data-ttu-id="4d78b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d78b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="4d78b-112">이 명령은 Spark 풀 아래에 있는 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="4d78b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4d78b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="4d78b-114">이 명령은 지정 된 ID의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="4d78b-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="4d78b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="4d78b-116">이 명령은 지정 된 응용 프로그램 ID를 갖는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="4d78b-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="4d78b-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="4d78b-118">이 명령은 파이프라인을 통해 Spark 풀 아래에 있는 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="4d78b-119">변수</span><span class="sxs-lookup"><span data-stu-id="4d78b-119">PARAMETERS</span></span>

### <span data-ttu-id="4d78b-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4d78b-120">-ApplicationId</span></span>
<span data-ttu-id="4d78b-121">세션의 응용 프로그램 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="4d78b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d78b-122">-DefaultProfile</span></span>
<span data-ttu-id="4d78b-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d78b-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="4d78b-124">-LivyId</span></span>
<span data-ttu-id="4d78b-125">Spark 작업의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="4d78b-126">-이름</span><span class="sxs-lookup"><span data-stu-id="4d78b-126">-Name</span></span>
<span data-ttu-id="4d78b-127">Spark 작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="4d78b-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4d78b-128">-SparkPoolName</span></span>
<span data-ttu-id="4d78b-129">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="4d78b-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="4d78b-130">-SparkPoolObject</span></span>
<span data-ttu-id="4d78b-131">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4d78b-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d78b-132">-WorkspaceName</span></span>
<span data-ttu-id="4d78b-133">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4d78b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d78b-134">CommonParameters</span></span>
<span data-ttu-id="4d78b-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d78b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d78b-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d78b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d78b-137">입력</span><span class="sxs-lookup"><span data-stu-id="4d78b-137">INPUTS</span></span>

### <span data-ttu-id="4d78b-138">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="4d78b-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="4d78b-139">출력</span><span class="sxs-lookup"><span data-stu-id="4d78b-139">OUTPUTS</span></span>

### <span data-ttu-id="4d78b-140">Synapse. PSSynapseSparkJob/.</span><span class="sxs-lookup"><span data-stu-id="4d78b-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="4d78b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4d78b-141">NOTES</span></span>

## <span data-ttu-id="4d78b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d78b-142">RELATED LINKS</span></span>
