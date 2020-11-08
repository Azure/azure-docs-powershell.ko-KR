---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204684"
---
# <span data-ttu-id="db278-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="db278-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="db278-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db278-102">SYNOPSIS</span></span>
<span data-ttu-id="db278-103">Synapse Analytics Spark 문을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db278-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="db278-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db278-104">SYNTAX</span></span>

### <span data-ttu-id="db278-105">GetSparkStatementsByIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="db278-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db278-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db278-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db278-107">설명은</span><span class="sxs-lookup"><span data-stu-id="db278-107">DESCRIPTION</span></span>
<span data-ttu-id="db278-108">**AzSynapseSparkStatement** Cmdlet은 Azure Synapse Analytics Spark 문에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db278-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="db278-109">예제의</span><span class="sxs-lookup"><span data-stu-id="db278-109">EXAMPLES</span></span>

### <span data-ttu-id="db278-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="db278-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="db278-111">이 명령은 Spark 세션 아래에 있는 모든 Spark 문을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db278-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="db278-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="db278-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="db278-113">이 명령은 지정 된 livy ID의 Spark 문을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db278-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="db278-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="db278-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="db278-115">이 명령은 파이프라인을 통해 Spark 세션 아래에 있는 모든 Spark 문을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db278-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="db278-116">변수</span><span class="sxs-lookup"><span data-stu-id="db278-116">PARAMETERS</span></span>

### <span data-ttu-id="db278-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db278-117">-DefaultProfile</span></span>
<span data-ttu-id="db278-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db278-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db278-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="db278-119">-LivyId</span></span>
<span data-ttu-id="db278-120">Spark 문의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="db278-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="db278-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="db278-121">-SessionId</span></span>
<span data-ttu-id="db278-122">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="db278-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="db278-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="db278-123">-SessionObject</span></span>
<span data-ttu-id="db278-124">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="db278-124">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="db278-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="db278-125">-SparkPoolName</span></span>
<span data-ttu-id="db278-126">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db278-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="db278-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db278-127">-WorkspaceName</span></span>
<span data-ttu-id="db278-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db278-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="db278-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db278-129">CommonParameters</span></span>
<span data-ttu-id="db278-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db278-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db278-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="db278-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db278-132">입력</span><span class="sxs-lookup"><span data-stu-id="db278-132">INPUTS</span></span>

### <span data-ttu-id="db278-133">Synapse. PSSynapseSparkSession/.</span><span class="sxs-lookup"><span data-stu-id="db278-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="db278-134">출력</span><span class="sxs-lookup"><span data-stu-id="db278-134">OUTPUTS</span></span>

### <span data-ttu-id="db278-135">Synapse. PSSynapseSparkStatement/.</span><span class="sxs-lookup"><span data-stu-id="db278-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="db278-136">상속자</span><span class="sxs-lookup"><span data-stu-id="db278-136">NOTES</span></span>

## <span data-ttu-id="db278-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db278-137">RELATED LINKS</span></span>
