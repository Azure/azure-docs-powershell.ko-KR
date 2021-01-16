---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ceeb33615748b7cf11c13441399bbae6a934a56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383363"
---
# <span data-ttu-id="5bc09-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5bc09-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="5bc09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc09-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc09-103">Synapse Analytics 풀 복원 SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="5bc09-104">구문</span><span class="sxs-lookup"><span data-stu-id="5bc09-104">SYNTAX</span></span>

### <span data-ttu-id="5bc09-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5bc09-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc09-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc09-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bc09-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc09-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc09-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc09-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bc09-109">설명</span><span class="sxs-lookup"><span data-stu-id="5bc09-109">DESCRIPTION</span></span>
<span data-ttu-id="5bc09-110">**Remove-AzSynapseSqlPoolRestorePoint** cmdlet은 풀 복원 지점에서 Azure Synapse Analytics SQL 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="5bc09-111">예제</span><span class="sxs-lookup"><span data-stu-id="5bc09-111">EXAMPLES</span></span>

### <span data-ttu-id="5bc09-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bc09-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="5bc09-113">이 명령은 Azure Synapse Analytics SQL 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="5bc09-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="5bc09-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="5bc09-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="5bc09-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="5bc09-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="5bc09-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="5bc09-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="5bc09-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="5bc09-119">이 명령은 지정된 리소스 ID를 SQL Azure Synapse Analytics 풀 복원 지점을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="5bc09-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bc09-120">PARAMETERS</span></span>

### <span data-ttu-id="5bc09-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bc09-121">-AsJob</span></span>
<span data-ttu-id="5bc09-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5bc09-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bc09-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc09-123">-DefaultProfile</span></span>
<span data-ttu-id="5bc09-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bc09-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5bc09-125">-Force</span></span>
<span data-ttu-id="5bc09-126">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5bc09-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bc09-127">-InputObject</span></span>
<span data-ttu-id="5bc09-128">SQL 복원 지점 생성 시간 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5bc09-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bc09-129">-PassThru</span></span>
<span data-ttu-id="5bc09-130">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="5bc09-131">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5bc09-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc09-132">-ResourceGroupName</span></span>
<span data-ttu-id="5bc09-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-133">Resource group name.</span></span>

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

### <span data-ttu-id="5bc09-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bc09-134">-ResourceId</span></span>
<span data-ttu-id="5bc09-135">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="5bc09-136">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="5bc09-136">-RestorePointCreationDate</span></span>
<span data-ttu-id="5bc09-137">복원 지점 만들기 SQL 시 힙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-137">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc09-138">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="5bc09-138">-SqlPoolName</span></span>
<span data-ttu-id="5bc09-139">Synapse Sql 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-139">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="5bc09-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="5bc09-140">-SqlPoolObject</span></span>
<span data-ttu-id="5bc09-141">일반적으로 파이프라인을 통해 전달되는 Sql 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5bc09-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5bc09-142">-WorkspaceName</span></span>
<span data-ttu-id="5bc09-143">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5bc09-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bc09-144">-Confirm</span></span>
<span data-ttu-id="5bc09-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bc09-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc09-146">-WhatIf</span></span>
<span data-ttu-id="5bc09-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5bc09-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bc09-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bc09-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc09-149">CommonParameters</span></span>
<span data-ttu-id="5bc09-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc09-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc09-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5bc09-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc09-152">입력</span><span class="sxs-lookup"><span data-stu-id="5bc09-152">INPUTS</span></span>

### <span data-ttu-id="5bc09-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5bc09-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5bc09-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5bc09-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="5bc09-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5bc09-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="5bc09-156">System.String</span><span class="sxs-lookup"><span data-stu-id="5bc09-156">System.String</span></span>

## <span data-ttu-id="5bc09-157">출력</span><span class="sxs-lookup"><span data-stu-id="5bc09-157">OUTPUTS</span></span>

### <span data-ttu-id="5bc09-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bc09-158">System.Boolean</span></span>

## <span data-ttu-id="5bc09-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bc09-159">NOTES</span></span>

## <span data-ttu-id="5bc09-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bc09-160">RELATED LINKS</span></span>
