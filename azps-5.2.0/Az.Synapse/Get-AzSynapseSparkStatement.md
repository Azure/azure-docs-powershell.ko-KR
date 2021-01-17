---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359444"
---
# <span data-ttu-id="1b5be-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="1b5be-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="1b5be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b5be-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5be-103">Synapse Analytics Spark 문을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="1b5be-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b5be-104">SYNTAX</span></span>

### <span data-ttu-id="1b5be-105">GetSparkStatementsByIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1b5be-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b5be-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b5be-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b5be-107">설명</span><span class="sxs-lookup"><span data-stu-id="1b5be-107">DESCRIPTION</span></span>
<span data-ttu-id="1b5be-108">**Get-AzSynapseSparkStatement** cmdlet은 Azure Synapse Analytics Spark 문에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="1b5be-109">예제</span><span class="sxs-lookup"><span data-stu-id="1b5be-109">EXAMPLES</span></span>

### <span data-ttu-id="1b5be-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1b5be-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="1b5be-111">이 명령은 Spark 세션에서 모든 Spark 문을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="1b5be-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="1b5be-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="1b5be-113">이 명령은 지정된 livy ID를 사용하여 Spark 문을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="1b5be-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="1b5be-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="1b5be-115">이 명령은 파이프라인을 통해 Spark 세션에서 모든 Spark 문을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="1b5be-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b5be-116">PARAMETERS</span></span>

### <span data-ttu-id="1b5be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5be-117">-DefaultProfile</span></span>
<span data-ttu-id="1b5be-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b5be-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="1b5be-119">-LivyId</span></span>
<span data-ttu-id="1b5be-120">Spark 문의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="1b5be-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="1b5be-121">-SessionId</span></span>
<span data-ttu-id="1b5be-122">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5be-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="1b5be-123">-SessionObject</span></span>
<span data-ttu-id="1b5be-124">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5be-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="1b5be-125">-SparkPoolName</span></span>
<span data-ttu-id="1b5be-126">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5be-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1b5be-127">-WorkspaceName</span></span>
<span data-ttu-id="1b5be-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5be-129">CommonParameters</span></span>
<span data-ttu-id="1b5be-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b5be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5be-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b5be-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5be-132">입력</span><span class="sxs-lookup"><span data-stu-id="1b5be-132">INPUTS</span></span>

### <span data-ttu-id="1b5be-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="1b5be-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="1b5be-134">출력</span><span class="sxs-lookup"><span data-stu-id="1b5be-134">OUTPUTS</span></span>

### <span data-ttu-id="1b5be-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="1b5be-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="1b5be-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b5be-136">NOTES</span></span>

## <span data-ttu-id="1b5be-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b5be-137">RELATED LINKS</span></span>
