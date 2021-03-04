---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: d0249098c8414a38adecc4112449174496656b78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011275"
---
# <span data-ttu-id="e290a-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e290a-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e290a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e290a-102">SYNOPSIS</span></span>
<span data-ttu-id="e290a-103">Synapse Analytics SQL 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e290a-104">구문</span><span class="sxs-lookup"><span data-stu-id="e290a-104">SYNTAX</span></span>

### <span data-ttu-id="e290a-105">suspendByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e290a-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e290a-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e290a-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e290a-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e290a-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e290a-108">suspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e290a-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e290a-109">설명</span><span class="sxs-lookup"><span data-stu-id="e290a-109">DESCRIPTION</span></span>
<span data-ttu-id="e290a-110">**Suspend-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e290a-111">예제</span><span class="sxs-lookup"><span data-stu-id="e290a-111">EXAMPLES</span></span>

### <span data-ttu-id="e290a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e290a-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e290a-113">이 명령은 활성 Azure Synapse Analytics SQL 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e290a-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e290a-114">PARAMETERS</span></span>

### <span data-ttu-id="e290a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e290a-115">-AsJob</span></span>
<span data-ttu-id="e290a-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e290a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e290a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e290a-117">-DefaultProfile</span></span>
<span data-ttu-id="e290a-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e290a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e290a-119">-InputObject</span></span>
<span data-ttu-id="e290a-120">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e290a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e290a-121">-Name</span></span>
<span data-ttu-id="e290a-122">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e290a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e290a-123">-PassThru</span></span>
<span data-ttu-id="e290a-124">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e290a-125">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e290a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e290a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e290a-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-127">Resource group name.</span></span>

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

### <span data-ttu-id="e290a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e290a-128">-ResourceId</span></span>
<span data-ttu-id="e290a-129">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="e290a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e290a-130">-WorkspaceName</span></span>
<span data-ttu-id="e290a-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e290a-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e290a-132">-WorkspaceObject</span></span>
<span data-ttu-id="e290a-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e290a-134">-확인</span><span class="sxs-lookup"><span data-stu-id="e290a-134">-Confirm</span></span>
<span data-ttu-id="e290a-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e290a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e290a-136">-WhatIf</span></span>
<span data-ttu-id="e290a-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e290a-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e290a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e290a-139">CommonParameters</span></span>
<span data-ttu-id="e290a-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e290a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e290a-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e290a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e290a-142">입력</span><span class="sxs-lookup"><span data-stu-id="e290a-142">INPUTS</span></span>

### <span data-ttu-id="e290a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e290a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e290a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e290a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e290a-145">출력</span><span class="sxs-lookup"><span data-stu-id="e290a-145">OUTPUTS</span></span>

### <span data-ttu-id="e290a-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e290a-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e290a-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e290a-147">NOTES</span></span>

## <span data-ttu-id="e290a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e290a-148">RELATED LINKS</span></span>
