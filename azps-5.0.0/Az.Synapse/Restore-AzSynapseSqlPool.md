---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 2dae942470dba8a36258ffb8c813e08c664f2e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309401"
---
# <span data-ttu-id="6f9f2-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6f9f2-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="6f9f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f9f2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9f2-103">Synapse Analytics SQL 풀을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6f9f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f9f2-104">SYNTAX</span></span>

### <span data-ttu-id="6f9f2-105">RestoreFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-105">RestoreFromBackupIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f9f2-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f9f2-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9f2-115">설명은</span><span class="sxs-lookup"><span data-stu-id="6f9f2-115">DESCRIPTION</span></span>
<span data-ttu-id="6f9f2-116">**Restore-AzSynapseSqlPool** CMDLET은 sql 풀의 백업 또는 복원 시점에서 Azure SYNAPSE Analytics SQL 풀을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="6f9f2-117">복원 된 SQL 풀은 새 SQL 풀로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="6f9f2-118">예제의</span><span class="sxs-lookup"><span data-stu-id="6f9f2-118">EXAMPLES</span></span>

### <span data-ttu-id="6f9f2-119">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f9f2-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="6f9f2-120">이 명령은이 구독에 있는 모든 SQL 풀의 최신 백업에서 복원 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="6f9f2-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="6f9f2-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="6f9f2-122">이 명령은이 구독의 모든 SQL 풀에서 복원 지점을 활용 하 여 이전 상태에서 복구 하거나 복사 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="6f9f2-123">예제 3</span><span class="sxs-lookup"><span data-stu-id="6f9f2-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="6f9f2-124">이 명령은 리소스 ID를 사용 하 여이 구독에 있는 모든 SQL 풀의 가장 최근 백업에서 복원 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="6f9f2-125">예제 4</span><span class="sxs-lookup"><span data-stu-id="6f9f2-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="6f9f2-126">이 명령은 리소스 ID를 사용 하 여 이전 상태에서 복구 하거나 복사 하기 위해이 구독에 있는 모든 SQL 풀의 복원 지점을 활용 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="6f9f2-127">변수</span><span class="sxs-lookup"><span data-stu-id="6f9f2-127">PARAMETERS</span></span>

### <span data-ttu-id="6f9f2-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f9f2-128">-AsJob</span></span>
<span data-ttu-id="6f9f2-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6f9f2-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f9f2-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="6f9f2-131">만들 bakcup SQL 풀 개체의 자원 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9f2-132">-BackupResourceId</span></span>
<span data-ttu-id="6f9f2-133">복원할 백업 SQL 풀 개체의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="6f9f2-135">만들 bakcup SQL 풀 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-136">-Backupsqlpoo...</span><span class="sxs-lookup"><span data-stu-id="6f9f2-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="6f9f2-137">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="6f9f2-139">Synapse에서 만들 bakcup SQL 풀 개체의 작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9f2-140">-DefaultProfile</span></span>
<span data-ttu-id="6f9f2-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f9f2-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="6f9f2-142">-FromBackup</span></span>
<span data-ttu-id="6f9f2-143">이 구독에 있는 모든 SQL 풀의 최신 백업에서 복원을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6f9f2-144">-FromRestorePoint</span></span>
<span data-ttu-id="6f9f2-145">이 구독에서 모든 SQL 풀의 복원 지점을 활용 하 여 이전 상태에서 복구 하거나 복사 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-146">-이름</span><span class="sxs-lookup"><span data-stu-id="6f9f2-146">-Name</span></span>
<span data-ttu-id="6f9f2-147">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="6f9f2-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="6f9f2-148">-PerformanceLevel</span></span>
<span data-ttu-id="6f9f2-149">SQL 풀에 할당할 SQL 서비스 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="6f9f2-150">예를 DW2000c.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-151">-ResourceGroupName</span></span>
<span data-ttu-id="6f9f2-152">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="6f9f2-153">-RestorePoint</span></span>
<span data-ttu-id="6f9f2-154">스냅숏 복원 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="6f9f2-156">만들 원본 SQL 풀 개체의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9f2-157">-SourceResourceId</span></span>
<span data-ttu-id="6f9f2-158">만들 원본 SQL 풀 개체의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="6f9f2-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="6f9f2-160">만들 원본 SQL 풀 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="6f9f2-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="6f9f2-162">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="6f9f2-164">Synapse 작업 영역에서 만들 원본 SQL 풀 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-165">태그</span><span class="sxs-lookup"><span data-stu-id="6f9f2-165">-Tag</span></span>
<span data-ttu-id="6f9f2-166">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-166">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f9f2-167">-WorkspaceName</span></span>
<span data-ttu-id="6f9f2-168">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6f9f2-169">-WorkspaceObject</span></span>
<span data-ttu-id="6f9f2-170">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9f2-171">-확인</span><span class="sxs-lookup"><span data-stu-id="6f9f2-171">-Confirm</span></span>
<span data-ttu-id="6f9f2-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f9f2-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9f2-173">-WhatIf</span></span>
<span data-ttu-id="6f9f2-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f9f2-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f9f2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9f2-176">CommonParameters</span></span>
<span data-ttu-id="6f9f2-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9f2-178">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9f2-179">입력</span><span class="sxs-lookup"><span data-stu-id="6f9f2-179">INPUTS</span></span>

### <span data-ttu-id="6f9f2-180">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6f9f2-181">출력</span><span class="sxs-lookup"><span data-stu-id="6f9f2-181">OUTPUTS</span></span>

### <span data-ttu-id="6f9f2-182">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="6f9f2-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6f9f2-183">상속자</span><span class="sxs-lookup"><span data-stu-id="6f9f2-183">NOTES</span></span>

## <span data-ttu-id="6f9f2-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f9f2-184">RELATED LINKS</span></span>
