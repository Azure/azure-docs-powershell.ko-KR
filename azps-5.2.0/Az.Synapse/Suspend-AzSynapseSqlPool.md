---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366178"
---
# <span data-ttu-id="7d985-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7d985-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="7d985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d985-102">SYNOPSIS</span></span>
<span data-ttu-id="7d985-103">Synapse Analytics SQL 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7d985-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d985-104">SYNTAX</span></span>

### <span data-ttu-id="7d985-105">SuspendByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d985-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d985-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d985-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d985-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d985-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d985-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d985-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d985-109">설명</span><span class="sxs-lookup"><span data-stu-id="7d985-109">DESCRIPTION</span></span>
<span data-ttu-id="7d985-110">**Suspend-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7d985-111">예제</span><span class="sxs-lookup"><span data-stu-id="7d985-111">EXAMPLES</span></span>

### <span data-ttu-id="7d985-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d985-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="7d985-113">이 명령은 활성 Azure Synapse Analytics SQL 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7d985-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d985-114">PARAMETERS</span></span>

### <span data-ttu-id="7d985-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d985-115">-AsJob</span></span>
<span data-ttu-id="7d985-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7d985-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d985-117">-DefaultProfile</span></span>
<span data-ttu-id="7d985-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d985-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d985-119">-InputObject</span></span>
<span data-ttu-id="7d985-120">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7d985-121">-Name</span></span>
<span data-ttu-id="7d985-122">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d985-123">-PassThru</span></span>
<span data-ttu-id="7d985-124">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7d985-125">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-125">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d985-126">-ResourceGroupName</span></span>
<span data-ttu-id="7d985-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d985-128">-ResourceId</span></span>
<span data-ttu-id="7d985-129">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7d985-130">-WorkspaceName</span></span>
<span data-ttu-id="7d985-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7d985-132">-WorkspaceObject</span></span>
<span data-ttu-id="7d985-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d985-134">-Confirm</span></span>
<span data-ttu-id="7d985-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d985-136">-WhatIf</span></span>
<span data-ttu-id="7d985-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7d985-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d985-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d985-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d985-139">CommonParameters</span></span>
<span data-ttu-id="7d985-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d985-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d985-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d985-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d985-142">입력</span><span class="sxs-lookup"><span data-stu-id="7d985-142">INPUTS</span></span>

### <span data-ttu-id="7d985-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d985-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7d985-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7d985-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7d985-145">출력</span><span class="sxs-lookup"><span data-stu-id="7d985-145">OUTPUTS</span></span>

### <span data-ttu-id="7d985-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7d985-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7d985-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d985-147">NOTES</span></span>

## <span data-ttu-id="7d985-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d985-148">RELATED LINKS</span></span>
