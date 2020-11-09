---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309814"
---
# <span data-ttu-id="7c6f2-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="7c6f2-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="7c6f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6f2-103">Synapse Analytics Spark 세션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="7c6f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c6f2-104">SYNTAX</span></span>

### <span data-ttu-id="7c6f2-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c6f2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c6f2-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c6f2-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c6f2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c6f2-107">DESCRIPTION</span></span>
<span data-ttu-id="7c6f2-108">**AzSynapseSparkSession** Cmdlet은 Azure Synapse Analytics Spark 세션에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="7c6f2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7c6f2-109">EXAMPLES</span></span>

### <span data-ttu-id="7c6f2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c6f2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="7c6f2-111">이 명령은 지정 된 Spark 풀 아래에 있는 모든 Spark 세션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="7c6f2-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c6f2-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="7c6f2-113">이 명령은 지정 된 livy ID의 Spark 세션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="7c6f2-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="7c6f2-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="7c6f2-115">이 명령은 파이프라인을 통해 지정 된 Spark 풀의 모든 Spark 세션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="7c6f2-116">변수</span><span class="sxs-lookup"><span data-stu-id="7c6f2-116">PARAMETERS</span></span>

### <span data-ttu-id="7c6f2-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7c6f2-117">-ApplicationId</span></span>
<span data-ttu-id="7c6f2-118">세션의 응용 프로그램 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="7c6f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6f2-119">-DefaultProfile</span></span>
<span data-ttu-id="7c6f2-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c6f2-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="7c6f2-121">-LivyId</span></span>
<span data-ttu-id="7c6f2-122">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="7c6f2-123">-이름</span><span class="sxs-lookup"><span data-stu-id="7c6f2-123">-Name</span></span>
<span data-ttu-id="7c6f2-124">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="7c6f2-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="7c6f2-125">-SparkPoolName</span></span>
<span data-ttu-id="7c6f2-126">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="7c6f2-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="7c6f2-127">-SparkPoolObject</span></span>
<span data-ttu-id="7c6f2-128">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7c6f2-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c6f2-129">-WorkspaceName</span></span>
<span data-ttu-id="7c6f2-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7c6f2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6f2-131">CommonParameters</span></span>
<span data-ttu-id="7c6f2-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6f2-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6f2-134">입력</span><span class="sxs-lookup"><span data-stu-id="7c6f2-134">INPUTS</span></span>

### <span data-ttu-id="7c6f2-135">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="7c6f2-136">출력</span><span class="sxs-lookup"><span data-stu-id="7c6f2-136">OUTPUTS</span></span>

### <span data-ttu-id="7c6f2-137">Synapse. PSSynapseSparkSession/.</span><span class="sxs-lookup"><span data-stu-id="7c6f2-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="7c6f2-138">상속자</span><span class="sxs-lookup"><span data-stu-id="7c6f2-138">NOTES</span></span>

## <span data-ttu-id="7c6f2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c6f2-139">RELATED LINKS</span></span>
