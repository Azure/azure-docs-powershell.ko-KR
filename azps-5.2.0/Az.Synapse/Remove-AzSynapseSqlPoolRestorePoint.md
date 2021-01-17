---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: e9c4c68f794b5ea0c20b0e1fe57677b329b02622
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343113"
---
# <span data-ttu-id="8cdfa-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8cdfa-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="8cdfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cdfa-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdfa-103">Synapse Analytics 풀 복원 SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="8cdfa-104">구문</span><span class="sxs-lookup"><span data-stu-id="8cdfa-104">SYNTAX</span></span>

### <span data-ttu-id="8cdfa-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8cdfa-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String> -Name <String> 
[-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cdfa-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cdfa-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -Name <String> -SqlPoolObject <PSSynapseSqlPool> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cdfa-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cdfa-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cdfa-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cdfa-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cdfa-109">설명</span><span class="sxs-lookup"><span data-stu-id="8cdfa-109">DESCRIPTION</span></span>
<span data-ttu-id="8cdfa-110">**Remove-AzSynapseSqlPoolRestorePoint** cmdlet은 풀 복원 지점에서 Azure Synapse Analytics SQL 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="8cdfa-111">예제</span><span class="sxs-lookup"><span data-stu-id="8cdfa-111">EXAMPLES</span></span>

### <span data-ttu-id="8cdfa-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8cdfa-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="8cdfa-113">이 명령은 Azure Synapse Analytics SQL 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="8cdfa-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="8cdfa-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="8cdfa-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="8cdfa-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="8cdfa-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="8cdfa-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="8cdfa-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="8cdfa-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="8cdfa-119">이 명령은 지정된 리소스 ID를 SQL Azure Synapse Analytics 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="8cdfa-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cdfa-120">PARAMETERS</span></span>

### <span data-ttu-id="8cdfa-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cdfa-121">-AsJob</span></span>
<span data-ttu-id="8cdfa-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8cdfa-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cdfa-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8cdfa-123">-Force</span></span>
<span data-ttu-id="8cdfa-124">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-124">Do not ask for confirmation.</span></span>

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


### <span data-ttu-id="8cdfa-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cdfa-125">-InputObject</span></span>
<span data-ttu-id="8cdfa-126">SQL 복원 지점 생성 시간 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-126">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdfa-127">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="8cdfa-127">-RestorePointCreationDate</span></span>
<span data-ttu-id="8cdfa-128">복원 지점 만들기 SQL 시 힙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-128">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdfa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cdfa-129">-PassThru</span></span>
<span data-ttu-id="8cdfa-130">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8cdfa-131">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8cdfa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cdfa-132">-ResourceGroupName</span></span>
<span data-ttu-id="8cdfa-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-133">Resource group name.</span></span>

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

### <span data-ttu-id="8cdfa-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cdfa-134">-ResourceId</span></span>
<span data-ttu-id="8cdfa-135">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="8cdfa-136">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="8cdfa-136">-SqlPoolName</span></span>
<span data-ttu-id="8cdfa-137">Synapse Sql 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-137">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="8cdfa-138">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="8cdfa-138">-SqlPoolObject</span></span>
<span data-ttu-id="8cdfa-139">일반적으로 파이프라인을 통해 전달되는 Sql 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-139">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdfa-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8cdfa-140">-WorkspaceName</span></span>
<span data-ttu-id="8cdfa-141">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8cdfa-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8cdfa-142">-WorkspaceObject</span></span>
<span data-ttu-id="8cdfa-143">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8cdfa-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cdfa-144">-Confirm</span></span>
<span data-ttu-id="8cdfa-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cdfa-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cdfa-146">-WhatIf</span></span>
<span data-ttu-id="8cdfa-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8cdfa-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cdfa-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cdfa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdfa-149">CommonParameters</span></span>
<span data-ttu-id="8cdfa-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdfa-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8cdfa-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdfa-152">입력</span><span class="sxs-lookup"><span data-stu-id="8cdfa-152">INPUTS</span></span>

### <span data-ttu-id="8cdfa-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8cdfa-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8cdfa-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8cdfa-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="8cdfa-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8cdfa-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="8cdfa-156">System.String</span><span class="sxs-lookup"><span data-stu-id="8cdfa-156">System.String</span></span>

## <span data-ttu-id="8cdfa-157">출력</span><span class="sxs-lookup"><span data-stu-id="8cdfa-157">OUTPUTS</span></span>

### <span data-ttu-id="8cdfa-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8cdfa-158">System.Boolean</span></span>

## <span data-ttu-id="8cdfa-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8cdfa-159">NOTES</span></span>

## <span data-ttu-id="8cdfa-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cdfa-160">RELATED LINKS</span></span>
