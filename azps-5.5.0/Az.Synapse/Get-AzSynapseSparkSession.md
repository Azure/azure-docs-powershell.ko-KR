---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209053"
---
# <span data-ttu-id="460ee-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="460ee-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="460ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="460ee-102">SYNOPSIS</span></span>
<span data-ttu-id="460ee-103">Synapse Analytics Spark 세션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="460ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="460ee-104">SYNTAX</span></span>

### <span data-ttu-id="460ee-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="460ee-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="460ee-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="460ee-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="460ee-107">설명</span><span class="sxs-lookup"><span data-stu-id="460ee-107">DESCRIPTION</span></span>
<span data-ttu-id="460ee-108">**Get-AzSynapseSparkSession** cmdlet은 Azure Synapse Analytics Spark 세션에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="460ee-109">예제</span><span class="sxs-lookup"><span data-stu-id="460ee-109">EXAMPLES</span></span>

### <span data-ttu-id="460ee-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="460ee-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="460ee-111">이 명령은 지정된 Spark 풀에서 모든 Spark 세션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="460ee-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="460ee-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="460ee-113">이 명령은 지정된 livy ID를 사용하여 Spark 세션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="460ee-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="460ee-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="460ee-115">이 명령은 파이프라인을 통해 지정된 Spark 풀에서 모든 Spark 세션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="460ee-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="460ee-116">PARAMETERS</span></span>

### <span data-ttu-id="460ee-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="460ee-117">-ApplicationId</span></span>
<span data-ttu-id="460ee-118">세션의 애플리케이션 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="460ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460ee-119">-DefaultProfile</span></span>
<span data-ttu-id="460ee-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="460ee-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="460ee-121">-LivyId</span></span>
<span data-ttu-id="460ee-122">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="460ee-123">-Name</span><span class="sxs-lookup"><span data-stu-id="460ee-123">-Name</span></span>
<span data-ttu-id="460ee-124">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="460ee-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="460ee-125">-SparkPoolName</span></span>
<span data-ttu-id="460ee-126">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="460ee-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="460ee-127">-SparkPoolObject</span></span>
<span data-ttu-id="460ee-128">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="460ee-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="460ee-129">-WorkspaceName</span></span>
<span data-ttu-id="460ee-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="460ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460ee-131">CommonParameters</span></span>
<span data-ttu-id="460ee-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="460ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460ee-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="460ee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460ee-134">입력</span><span class="sxs-lookup"><span data-stu-id="460ee-134">INPUTS</span></span>

### <span data-ttu-id="460ee-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="460ee-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="460ee-136">출력</span><span class="sxs-lookup"><span data-stu-id="460ee-136">OUTPUTS</span></span>

### <span data-ttu-id="460ee-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="460ee-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="460ee-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="460ee-138">NOTES</span></span>

## <span data-ttu-id="460ee-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="460ee-139">RELATED LINKS</span></span>
