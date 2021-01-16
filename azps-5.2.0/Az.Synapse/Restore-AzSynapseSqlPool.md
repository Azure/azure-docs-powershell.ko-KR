---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 7fbc6cedf039cca33d0a30b39a21f9cdcb350b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333789"
---
# <span data-ttu-id="9ba95-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9ba95-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9ba95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba95-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba95-103">Synapse Analytics 풀을 SQL 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9ba95-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ba95-104">SYNTAX</span></span>

### <span data-ttu-id="9ba95-105">RestoreFromBackupIdByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9ba95-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba95-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba95-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba95-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba95-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba95-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba95-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba95-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba95-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba95-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ba95-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ba95-115">설명</span><span class="sxs-lookup"><span data-stu-id="9ba95-115">DESCRIPTION</span></span>
<span data-ttu-id="9ba95-116">**Restore-AzSynapseSqlPool** cmdlet은 모든 SQL 풀의 백업 또는 복원 지점에서 Azure Synapse Analytics SQL 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="9ba95-117">복원된 SQL 풀은 새 풀로 SQL 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="9ba95-118">예제</span><span class="sxs-lookup"><span data-stu-id="9ba95-118">EXAMPLES</span></span>

### <span data-ttu-id="9ba95-119">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ba95-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="9ba95-120">이 명령은 이 구독의 모든 SQL 백업에서 복원하여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="9ba95-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="9ba95-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="9ba95-122">이 명령은 이전 SQL 복구하거나 복사하기 위해 이 구독의 모든 SQL 풀에서 복원 지점을 활용하여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="9ba95-123">예제 3</span><span class="sxs-lookup"><span data-stu-id="9ba95-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="9ba95-124">이 명령은 리소스 ID를 SQL 구독의 모든 SQL 백업에서 복원하여 Azure Synapse Analytics 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="9ba95-125">예제 4</span><span class="sxs-lookup"><span data-stu-id="9ba95-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="9ba95-126">이 명령은 리소스 ID를 사용하여 이전 SQL 복구하거나 복사하기 위해 이 구독의 모든 SQL 풀에서 복원 지점을 활용하여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="9ba95-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ba95-127">PARAMETERS</span></span>

### <span data-ttu-id="9ba95-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ba95-128">-AsJob</span></span>
<span data-ttu-id="9ba95-129">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9ba95-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ba95-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba95-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="9ba95-131">bakcup의 리소스 그룹 SQL 만들 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-131">The resource group name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="9ba95-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="9ba95-132">-BackupResourceId</span></span>
<span data-ttu-id="9ba95-133">복원할 SQL 백업의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-133">The resource identifier of backup SQL pool object to restore from.</span></span>

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

### <span data-ttu-id="9ba95-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9ba95-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="9ba95-135">만들 풀 개체의 SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-135">The name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="9ba95-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9ba95-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="9ba95-137">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ba95-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ba95-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="9ba95-139">bakcup의 Synapse 작업 SQL 만들 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

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

### <span data-ttu-id="9ba95-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba95-140">-DefaultProfile</span></span>
<span data-ttu-id="9ba95-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ba95-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="9ba95-142">-FromBackup</span></span>
<span data-ttu-id="9ba95-143">이 구독의 모든 SQL 백업에서 복원하도록 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

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

### <span data-ttu-id="9ba95-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9ba95-144">-FromRestorePoint</span></span>
<span data-ttu-id="9ba95-145">이전 상태의 복구 또는 복사를 위해 이 SQL 풀에서 복원 지점을 활용하도록 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

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

### <span data-ttu-id="9ba95-146">-Name</span><span class="sxs-lookup"><span data-stu-id="9ba95-146">-Name</span></span>
<span data-ttu-id="9ba95-147">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="9ba95-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="9ba95-148">-PerformanceLevel</span></span>
<span data-ttu-id="9ba95-149">SQL 풀에 할당할 SQL 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="9ba95-150">예를 들어 DW2000c입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-150">For example, DW2000c.</span></span>

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

### <span data-ttu-id="9ba95-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba95-151">-ResourceGroupName</span></span>
<span data-ttu-id="9ba95-152">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-152">Resource group name.</span></span>

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

### <span data-ttu-id="9ba95-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="9ba95-153">-RestorePoint</span></span>
<span data-ttu-id="9ba95-154">복원할 스냅숏 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-154">Snapshot time to restore.</span></span>

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

### <span data-ttu-id="9ba95-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba95-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="9ba95-156">만들 원본 SQL 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-156">The resource group name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="9ba95-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9ba95-157">-SourceResourceId</span></span>
<span data-ttu-id="9ba95-158">만들 풀 SQL 원본의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="9ba95-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9ba95-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="9ba95-160">만들 SQL 원본 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-160">The name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="9ba95-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9ba95-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="9ba95-162">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-162">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ba95-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ba95-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="9ba95-164">만들 풀 개체에 대한 원본 SQL 작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="9ba95-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ba95-165">-Tag</span></span>
<span data-ttu-id="9ba95-166">리소스와 연결된 태그의 문자열 사전 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="9ba95-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9ba95-167">-WorkspaceName</span></span>
<span data-ttu-id="9ba95-168">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-168">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9ba95-169">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9ba95-169">-WorkspaceObject</span></span>
<span data-ttu-id="9ba95-170">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-170">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9ba95-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ba95-171">-Confirm</span></span>
<span data-ttu-id="9ba95-172">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba95-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba95-173">-WhatIf</span></span>
<span data-ttu-id="9ba95-174">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9ba95-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ba95-175">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba95-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba95-176">CommonParameters</span></span>
<span data-ttu-id="9ba95-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba95-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba95-178">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ba95-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba95-179">입력</span><span class="sxs-lookup"><span data-stu-id="9ba95-179">INPUTS</span></span>

### <span data-ttu-id="9ba95-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ba95-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9ba95-181">출력</span><span class="sxs-lookup"><span data-stu-id="9ba95-181">OUTPUTS</span></span>

### <span data-ttu-id="9ba95-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9ba95-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9ba95-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ba95-183">NOTES</span></span>

## <span data-ttu-id="9ba95-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ba95-184">RELATED LINKS</span></span>
