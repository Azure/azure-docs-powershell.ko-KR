---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: cb7abd3c54d263ae9516344237588ecf9a1297ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011248"
---
# <span data-ttu-id="ab797-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ab797-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="ab797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab797-102">SYNOPSIS</span></span>
<span data-ttu-id="ab797-103">Synapse Analytics Spark 풀의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ab797-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab797-104">SYNTAX</span></span>

### <span data-ttu-id="ab797-105">TestByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab797-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab797-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab797-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab797-107">설명</span><span class="sxs-lookup"><span data-stu-id="ab797-107">DESCRIPTION</span></span>
<span data-ttu-id="ab797-108">**Test-AzSynapseSparkPool** cmdlet은 Synapse Analytics Spark 풀의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ab797-109">예제</span><span class="sxs-lookup"><span data-stu-id="ab797-109">EXAMPLES</span></span>

### <span data-ttu-id="ab797-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab797-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="ab797-111">이 명령은 지정된 Spark 풀의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="ab797-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ab797-112">PARAMETERS</span></span>

### <span data-ttu-id="ab797-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab797-113">-DefaultProfile</span></span>
<span data-ttu-id="ab797-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab797-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ab797-115">-Name</span></span>
<span data-ttu-id="ab797-116">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="ab797-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab797-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab797-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab797-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ab797-119">-WorkspaceName</span></span>
<span data-ttu-id="ab797-120">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab797-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ab797-121">-WorkspaceObject</span></span>
<span data-ttu-id="ab797-122">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab797-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab797-123">CommonParameters</span></span>
<span data-ttu-id="ab797-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab797-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab797-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab797-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab797-126">입력</span><span class="sxs-lookup"><span data-stu-id="ab797-126">INPUTS</span></span>

### <span data-ttu-id="ab797-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab797-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ab797-128">출력</span><span class="sxs-lookup"><span data-stu-id="ab797-128">OUTPUTS</span></span>

### <span data-ttu-id="ab797-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="ab797-129">System.Object</span></span>
## <span data-ttu-id="ab797-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab797-130">NOTES</span></span>

## <span data-ttu-id="ab797-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab797-131">RELATED LINKS</span></span>
