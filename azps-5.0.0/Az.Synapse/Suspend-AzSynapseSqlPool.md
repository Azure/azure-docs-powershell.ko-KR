---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215163"
---
# <span data-ttu-id="ff048-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ff048-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="ff048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff048-102">SYNOPSIS</span></span>
<span data-ttu-id="ff048-103">Synapse Analytics SQL 풀을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ff048-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff048-104">SYNTAX</span></span>

### <span data-ttu-id="ff048-105">SuspendByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff048-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff048-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff048-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff048-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff048-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff048-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff048-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff048-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ff048-109">DESCRIPTION</span></span>
<span data-ttu-id="ff048-110">**AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ff048-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ff048-111">EXAMPLES</span></span>

### <span data-ttu-id="ff048-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff048-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="ff048-113">이 명령은 활성 Azure Synapse Analytics SQL 풀을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="ff048-114">변수</span><span class="sxs-lookup"><span data-stu-id="ff048-114">PARAMETERS</span></span>

### <span data-ttu-id="ff048-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff048-115">-AsJob</span></span>
<span data-ttu-id="ff048-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ff048-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff048-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff048-117">-DefaultProfile</span></span>
<span data-ttu-id="ff048-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff048-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff048-119">-InputObject</span></span>
<span data-ttu-id="ff048-120">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ff048-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ff048-121">-Name</span></span>
<span data-ttu-id="ff048-122">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="ff048-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff048-123">-PassThru</span></span>
<span data-ttu-id="ff048-124">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ff048-125">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ff048-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff048-126">-ResourceGroupName</span></span>
<span data-ttu-id="ff048-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-127">Resource group name.</span></span>

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

### <span data-ttu-id="ff048-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff048-128">-ResourceId</span></span>
<span data-ttu-id="ff048-129">Synapse SQL 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="ff048-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff048-130">-WorkspaceName</span></span>
<span data-ttu-id="ff048-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ff048-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ff048-132">-WorkspaceObject</span></span>
<span data-ttu-id="ff048-133">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ff048-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ff048-134">-Confirm</span></span>
<span data-ttu-id="ff048-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff048-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff048-136">-WhatIf</span></span>
<span data-ttu-id="ff048-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff048-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff048-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff048-139">CommonParameters</span></span>
<span data-ttu-id="ff048-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff048-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff048-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ff048-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff048-142">입력</span><span class="sxs-lookup"><span data-stu-id="ff048-142">INPUTS</span></span>

### <span data-ttu-id="ff048-143">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="ff048-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ff048-144">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="ff048-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ff048-145">출력</span><span class="sxs-lookup"><span data-stu-id="ff048-145">OUTPUTS</span></span>

### <span data-ttu-id="ff048-146">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="ff048-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ff048-147">상속자</span><span class="sxs-lookup"><span data-stu-id="ff048-147">NOTES</span></span>

## <span data-ttu-id="ff048-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff048-148">RELATED LINKS</span></span>
