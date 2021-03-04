---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 298077ced1b7cb308bae4a8a5d27e13893c4b4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999166"
---
# <span data-ttu-id="53a6e-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="53a6e-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="53a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="53a6e-103">Synapse Analytics SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="53a6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="53a6e-104">SYNTAX</span></span>

### <span data-ttu-id="53a6e-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="53a6e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53a6e-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53a6e-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a6e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53a6e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53a6e-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53a6e-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a6e-109">설명</span><span class="sxs-lookup"><span data-stu-id="53a6e-109">DESCRIPTION</span></span>
<span data-ttu-id="53a6e-110">**Remove-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="53a6e-111">예제</span><span class="sxs-lookup"><span data-stu-id="53a6e-111">EXAMPLES</span></span>

### <span data-ttu-id="53a6e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="53a6e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="53a6e-113">이 명령은 Azure Synapse Analytics SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="53a6e-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="53a6e-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="53a6e-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="53a6e-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="53a6e-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="53a6e-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="53a6e-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="53a6e-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="53a6e-119">이 명령은 지정된 리소스 ID가 SQL Azure Synapse Analytics SQL 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="53a6e-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="53a6e-120">PARAMETERS</span></span>

### <span data-ttu-id="53a6e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53a6e-121">-AsJob</span></span>
<span data-ttu-id="53a6e-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="53a6e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53a6e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a6e-123">-DefaultProfile</span></span>
<span data-ttu-id="53a6e-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53a6e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="53a6e-125">-Force</span></span>
<span data-ttu-id="53a6e-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="53a6e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53a6e-127">-InputObject</span></span>
<span data-ttu-id="53a6e-128">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="53a6e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="53a6e-129">-Name</span></span>
<span data-ttu-id="53a6e-130">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="53a6e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53a6e-131">-PassThru</span></span>
<span data-ttu-id="53a6e-132">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="53a6e-133">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="53a6e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a6e-134">-ResourceGroupName</span></span>
<span data-ttu-id="53a6e-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-135">Resource group name.</span></span>

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

### <span data-ttu-id="53a6e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53a6e-136">-ResourceId</span></span>
<span data-ttu-id="53a6e-137">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="53a6e-138">-Version</span><span class="sxs-lookup"><span data-stu-id="53a6e-138">-Version</span></span>
<span data-ttu-id="53a6e-139">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="53a6e-140">예를 들어 2 또는 3.</span><span class="sxs-lookup"><span data-stu-id="53a6e-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="53a6e-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53a6e-141">-WorkspaceName</span></span>
<span data-ttu-id="53a6e-142">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="53a6e-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53a6e-143">-WorkspaceObject</span></span>
<span data-ttu-id="53a6e-144">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="53a6e-145">-확인</span><span class="sxs-lookup"><span data-stu-id="53a6e-145">-Confirm</span></span>
<span data-ttu-id="53a6e-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a6e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a6e-147">-WhatIf</span></span>
<span data-ttu-id="53a6e-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a6e-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a6e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a6e-150">CommonParameters</span></span>
<span data-ttu-id="53a6e-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53a6e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a6e-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53a6e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a6e-153">입력</span><span class="sxs-lookup"><span data-stu-id="53a6e-153">INPUTS</span></span>

### <span data-ttu-id="53a6e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="53a6e-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="53a6e-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="53a6e-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="53a6e-156">System.String</span><span class="sxs-lookup"><span data-stu-id="53a6e-156">System.String</span></span>

## <span data-ttu-id="53a6e-157">출력</span><span class="sxs-lookup"><span data-stu-id="53a6e-157">OUTPUTS</span></span>

### <span data-ttu-id="53a6e-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="53a6e-158">System.Boolean</span></span>

## <span data-ttu-id="53a6e-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53a6e-159">NOTES</span></span>

## <span data-ttu-id="53a6e-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53a6e-160">RELATED LINKS</span></span>
