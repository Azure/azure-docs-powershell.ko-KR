---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361474"
---
# <span data-ttu-id="538a8-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="538a8-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="538a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="538a8-102">SYNOPSIS</span></span>
<span data-ttu-id="538a8-103">Synapse Analytics Spark 풀의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="538a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="538a8-104">SYNTAX</span></span>

### <span data-ttu-id="538a8-105">TestByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="538a8-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="538a8-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="538a8-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="538a8-107">설명</span><span class="sxs-lookup"><span data-stu-id="538a8-107">DESCRIPTION</span></span>
<span data-ttu-id="538a8-108">**Test-AzSynapseSparkPool** cmdlet은 Synapse Analytics Spark 풀의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="538a8-109">예제</span><span class="sxs-lookup"><span data-stu-id="538a8-109">EXAMPLES</span></span>

### <span data-ttu-id="538a8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="538a8-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="538a8-111">이 명령은 지정된 Spark 풀의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="538a8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="538a8-112">PARAMETERS</span></span>

### <span data-ttu-id="538a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538a8-113">-DefaultProfile</span></span>
<span data-ttu-id="538a8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="538a8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="538a8-115">-Name</span></span>
<span data-ttu-id="538a8-116">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="538a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="538a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="538a8-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-118">Resource group name.</span></span>

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

### <span data-ttu-id="538a8-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="538a8-119">-WorkspaceName</span></span>
<span data-ttu-id="538a8-120">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="538a8-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="538a8-121">-WorkspaceObject</span></span>
<span data-ttu-id="538a8-122">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="538a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538a8-123">CommonParameters</span></span>
<span data-ttu-id="538a8-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="538a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538a8-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="538a8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538a8-126">입력</span><span class="sxs-lookup"><span data-stu-id="538a8-126">INPUTS</span></span>

### <span data-ttu-id="538a8-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="538a8-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="538a8-128">출력</span><span class="sxs-lookup"><span data-stu-id="538a8-128">OUTPUTS</span></span>

### <span data-ttu-id="538a8-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="538a8-129">System.Object</span></span>
## <span data-ttu-id="538a8-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="538a8-130">NOTES</span></span>

## <span data-ttu-id="538a8-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="538a8-131">RELATED LINKS</span></span>
