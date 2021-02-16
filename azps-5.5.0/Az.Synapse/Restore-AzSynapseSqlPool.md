---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: fd83b97a7b95760d0ee2ce88295ed14c98a43ab3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182689"
---
# <span data-ttu-id="c28cd-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c28cd-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="c28cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c28cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c28cd-103">Synapse Analytics 풀을 SQL 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c28cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="c28cd-104">SYNTAX</span></span>

### <span data-ttu-id="c28cd-105">RestoreFromBackupIdByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c28cd-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c28cd-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c28cd-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c28cd-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c28cd-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c28cd-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c28cd-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c28cd-109">설명</span><span class="sxs-lookup"><span data-stu-id="c28cd-109">DESCRIPTION</span></span>
<span data-ttu-id="c28cd-110">**Restore-AzSynapseSqlPool** cmdlet은 모든 SQL 풀의 백업 또는 복원 지점에서 Azure Synapse Analytics SQL 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="c28cd-111">복원된 SQL 풀은 새 풀로 SQL 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="c28cd-112">예제</span><span class="sxs-lookup"><span data-stu-id="c28cd-112">EXAMPLES</span></span>

### <span data-ttu-id="c28cd-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c28cd-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="c28cd-114">이 명령은 이 구독의 모든 SQL 백업에서 복원하여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="c28cd-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="c28cd-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="c28cd-116">이 명령은 이전 SQL 복구하거나 복사하기 위해 이 구독의 모든 SQL 풀에서 복원 지점을 활용하여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="c28cd-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="c28cd-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="c28cd-118">이 명령은 리소스 ID를 SQL 구독의 모든 SQL 백업에서 복원하여 Azure Synapse Analytics 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="c28cd-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="c28cd-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="c28cd-120">이 명령은 리소스 ID를 사용하여 이전 SQL 복구하거나 복사하기 위해 이 구독의 모든 SQL 풀에서 복원 지점을 활용하여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="c28cd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c28cd-121">PARAMETERS</span></span>

### <span data-ttu-id="c28cd-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c28cd-122">-AsJob</span></span>
<span data-ttu-id="c28cd-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c28cd-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c28cd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28cd-124">-DefaultProfile</span></span>
<span data-ttu-id="c28cd-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c28cd-126">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="c28cd-126">-FromBackup</span></span>
<span data-ttu-id="c28cd-127">이 구독의 모든 SQL 백업에서 복원하도록 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28cd-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c28cd-128">-FromRestorePoint</span></span>
<span data-ttu-id="c28cd-129">이전 상태의 복구 또는 복사를 위해 이 SQL 풀에서 복원 지점을 활용하도록 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28cd-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c28cd-130">-Name</span></span>
<span data-ttu-id="c28cd-131">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetSqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28cd-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="c28cd-132">-PerformanceLevel</span></span>
<span data-ttu-id="c28cd-133">SQL 풀에 할당할 SQL 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="c28cd-134">예를 들어 DW2000c입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28cd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28cd-135">-ResourceGroupName</span></span>
<span data-ttu-id="c28cd-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28cd-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c28cd-137">-ResourceId</span></span>
<span data-ttu-id="c28cd-138">복원할 데이터베이스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-138">The resource ID of the database to restore.</span></span>

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

### <span data-ttu-id="c28cd-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="c28cd-139">-RestorePoint</span></span>
<span data-ttu-id="c28cd-140">복원할 스냅숏 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-140">Snapshot time to restore.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases: PointInTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28cd-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c28cd-141">-WorkspaceName</span></span>
<span data-ttu-id="c28cd-142">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28cd-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c28cd-143">-WorkspaceObject</span></span>
<span data-ttu-id="c28cd-144">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c28cd-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c28cd-145">-Confirm</span></span>
<span data-ttu-id="c28cd-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28cd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28cd-147">-WhatIf</span></span>
<span data-ttu-id="c28cd-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c28cd-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c28cd-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28cd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28cd-150">CommonParameters</span></span>
<span data-ttu-id="c28cd-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c28cd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28cd-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c28cd-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28cd-153">입력</span><span class="sxs-lookup"><span data-stu-id="c28cd-153">INPUTS</span></span>

### <span data-ttu-id="c28cd-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c28cd-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c28cd-155">출력</span><span class="sxs-lookup"><span data-stu-id="c28cd-155">OUTPUTS</span></span>

### <span data-ttu-id="c28cd-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c28cd-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c28cd-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c28cd-157">NOTES</span></span>

## <span data-ttu-id="c28cd-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c28cd-158">RELATED LINKS</span></span>
