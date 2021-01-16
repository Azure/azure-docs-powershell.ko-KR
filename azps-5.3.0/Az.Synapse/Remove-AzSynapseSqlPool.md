---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383370"
---
# <span data-ttu-id="bf53c-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bf53c-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="bf53c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf53c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf53c-103">Synapse Analytics SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bf53c-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf53c-104">SYNTAX</span></span>

### <span data-ttu-id="bf53c-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bf53c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf53c-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf53c-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf53c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf53c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf53c-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf53c-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf53c-109">설명</span><span class="sxs-lookup"><span data-stu-id="bf53c-109">DESCRIPTION</span></span>
<span data-ttu-id="bf53c-110">**Remove-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics 풀을 SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bf53c-111">예제</span><span class="sxs-lookup"><span data-stu-id="bf53c-111">EXAMPLES</span></span>

### <span data-ttu-id="bf53c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf53c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="bf53c-113">이 명령은 Azure Synapse Analytics SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="bf53c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="bf53c-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="bf53c-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="bf53c-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="bf53c-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="bf53c-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="bf53c-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="bf53c-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="bf53c-119">이 명령은 지정된 리소스 ID를 SQL Azure Synapse Analytics 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="bf53c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf53c-120">PARAMETERS</span></span>

### <span data-ttu-id="bf53c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf53c-121">-AsJob</span></span>
<span data-ttu-id="bf53c-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bf53c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf53c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf53c-123">-DefaultProfile</span></span>
<span data-ttu-id="bf53c-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf53c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="bf53c-125">-Force</span></span>
<span data-ttu-id="bf53c-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bf53c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf53c-127">-InputObject</span></span>
<span data-ttu-id="bf53c-128">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="bf53c-129">-Name</span></span>
<span data-ttu-id="bf53c-130">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf53c-131">-PassThru</span></span>
<span data-ttu-id="bf53c-132">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="bf53c-133">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bf53c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf53c-134">-ResourceGroupName</span></span>
<span data-ttu-id="bf53c-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf53c-136">-ResourceId</span></span>
<span data-ttu-id="bf53c-137">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-137">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-138">-Version</span><span class="sxs-lookup"><span data-stu-id="bf53c-138">-Version</span></span>
<span data-ttu-id="bf53c-139">Synapse SQL 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="bf53c-140">예를 들어 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="bf53c-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bf53c-141">-WorkspaceName</span></span>
<span data-ttu-id="bf53c-142">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bf53c-143">-WorkspaceObject</span></span>
<span data-ttu-id="bf53c-144">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf53c-145">-Confirm</span></span>
<span data-ttu-id="bf53c-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf53c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf53c-147">-WhatIf</span></span>
<span data-ttu-id="bf53c-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bf53c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf53c-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf53c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf53c-150">CommonParameters</span></span>
<span data-ttu-id="bf53c-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf53c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf53c-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf53c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf53c-153">입력</span><span class="sxs-lookup"><span data-stu-id="bf53c-153">INPUTS</span></span>

### <span data-ttu-id="bf53c-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf53c-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bf53c-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bf53c-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="bf53c-156">System.String</span><span class="sxs-lookup"><span data-stu-id="bf53c-156">System.String</span></span>

## <span data-ttu-id="bf53c-157">출력</span><span class="sxs-lookup"><span data-stu-id="bf53c-157">OUTPUTS</span></span>

### <span data-ttu-id="bf53c-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf53c-158">System.Boolean</span></span>

## <span data-ttu-id="bf53c-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf53c-159">NOTES</span></span>

## <span data-ttu-id="bf53c-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf53c-160">RELATED LINKS</span></span>
