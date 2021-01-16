---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: 80d615f5a2a26869d748f652feeaa8909aca30d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383069"
---
# <span data-ttu-id="38d9b-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="38d9b-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="38d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="38d9b-103">Synapse Analytics 풀의 존재를 SQL.</span><span class="sxs-lookup"><span data-stu-id="38d9b-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="38d9b-104">구문</span><span class="sxs-lookup"><span data-stu-id="38d9b-104">SYNTAX</span></span>

### <span data-ttu-id="38d9b-105">TestByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="38d9b-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38d9b-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38d9b-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38d9b-107">설명</span><span class="sxs-lookup"><span data-stu-id="38d9b-107">DESCRIPTION</span></span>
<span data-ttu-id="38d9b-108">**Test-AzSynapseSqlPool** cmdlet은 Synapse Analytics 풀의 존재를 SQL 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="38d9b-109">예제</span><span class="sxs-lookup"><span data-stu-id="38d9b-109">EXAMPLES</span></span>

### <span data-ttu-id="38d9b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="38d9b-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="38d9b-111">이 명령은 지정된 풀의 존재 SQL 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="38d9b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d9b-112">PARAMETERS</span></span>

### <span data-ttu-id="38d9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d9b-113">-DefaultProfile</span></span>
<span data-ttu-id="38d9b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d9b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="38d9b-115">-Name</span></span>
<span data-ttu-id="38d9b-116">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-116">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d9b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d9b-117">-ResourceGroupName</span></span>
<span data-ttu-id="38d9b-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-118">Resource group name.</span></span>

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

### <span data-ttu-id="38d9b-119">-Version</span><span class="sxs-lookup"><span data-stu-id="38d9b-119">-Version</span></span>
<span data-ttu-id="38d9b-120">Synapse SQL 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="38d9b-121">예를 들어 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="38d9b-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38d9b-122">-WorkspaceName</span></span>
<span data-ttu-id="38d9b-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="38d9b-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="38d9b-124">-WorkspaceObject</span></span>
<span data-ttu-id="38d9b-125">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="38d9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d9b-126">CommonParameters</span></span>
<span data-ttu-id="38d9b-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38d9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d9b-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38d9b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d9b-129">입력</span><span class="sxs-lookup"><span data-stu-id="38d9b-129">INPUTS</span></span>

### <span data-ttu-id="38d9b-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="38d9b-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="38d9b-131">출력</span><span class="sxs-lookup"><span data-stu-id="38d9b-131">OUTPUTS</span></span>

### <span data-ttu-id="38d9b-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="38d9b-132">System.Object</span></span>
## <span data-ttu-id="38d9b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38d9b-133">NOTES</span></span>

## <span data-ttu-id="38d9b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38d9b-134">RELATED LINKS</span></span>
