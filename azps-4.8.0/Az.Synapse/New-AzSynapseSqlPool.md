---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214674"
---
# <span data-ttu-id="731f8-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="731f8-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="731f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="731f8-102">SYNOPSIS</span></span>
<span data-ttu-id="731f8-103">Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="731f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="731f8-104">SYNTAX</span></span>

### <span data-ttu-id="731f8-105">CreateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="731f8-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731f8-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731f8-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731f8-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="731f8-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="731f8-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731f8-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="731f8-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="731f8-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731f8-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="731f8-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="731f8-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="731f8-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="731f8-117">설명은</span><span class="sxs-lookup"><span data-stu-id="731f8-117">DESCRIPTION</span></span>
<span data-ttu-id="731f8-118">**AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="731f8-119">예제의</span><span class="sxs-lookup"><span data-stu-id="731f8-119">EXAMPLES</span></span>

### <span data-ttu-id="731f8-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="731f8-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="731f8-121">이 명령은 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="731f8-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="731f8-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="731f8-123">이 명령은이 구독에 있는 모든 SQL 풀의 최신 백업에서 복원 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="731f8-124">예제 3</span><span class="sxs-lookup"><span data-stu-id="731f8-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="731f8-125">이 명령은이 구독의 모든 SQL 풀에서 복원 지점을 활용 하 여 이전 상태에서 복구 하거나 복사 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="731f8-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="731f8-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="731f8-127">이 명령은 리소스 ID를 사용 하 여이 구독에 있는 모든 SQL 풀의 가장 최근 백업에서 복원 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="731f8-128">예제 5</span><span class="sxs-lookup"><span data-stu-id="731f8-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="731f8-129">이 명령은 리소스 ID를 사용 하 여 이전 상태에서 복구 하거나 복사 하기 위해이 구독에 있는 모든 SQL 풀의 복원 지점을 활용 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="731f8-130">변수</span><span class="sxs-lookup"><span data-stu-id="731f8-130">PARAMETERS</span></span>

### <span data-ttu-id="731f8-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="731f8-131">-AsJob</span></span>
<span data-ttu-id="731f8-132">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="731f8-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="731f8-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731f8-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="731f8-134">만들 bakcup SQL 풀 개체의 자원 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="731f8-135">-BackupResourceId</span></span>
<span data-ttu-id="731f8-136">복원할 백업 SQL 풀 개체의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="731f8-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="731f8-138">만들 bakcup SQL 풀 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-139">-Backupsqlpoo...</span><span class="sxs-lookup"><span data-stu-id="731f8-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="731f8-140">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="731f8-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="731f8-142">Synapse에서 만들 bakcup SQL 풀 개체의 작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-143">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="731f8-143">-Collation</span></span>
<span data-ttu-id="731f8-144">데이터 정렬은 데이터를 정렬 및 비교 하는 규칙을 정의 하 고 SQL 풀을 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="731f8-145">기본 데이터 정렬은 SQL_Latin1_General_CP1_CI_AS입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731f8-146">-DefaultProfile</span></span>
<span data-ttu-id="731f8-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="731f8-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="731f8-148">-FromBackup</span></span>
<span data-ttu-id="731f8-149">이 구독에 있는 모든 SQL 풀의 최신 백업에서 복원을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="731f8-150">-FromRestorePoint</span></span>
<span data-ttu-id="731f8-151">이 구독에서 모든 SQL 풀의 복원 지점을 활용 하 여 이전 상태에서 복구 하거나 복사 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-152">-이름</span><span class="sxs-lookup"><span data-stu-id="731f8-152">-Name</span></span>
<span data-ttu-id="731f8-153">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="731f8-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="731f8-154">-PerformanceLevel</span></span>
<span data-ttu-id="731f8-155">SQL 풀에 할당할 SQL 서비스 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="731f8-156">예를 DW2000c.</span><span class="sxs-lookup"><span data-stu-id="731f8-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731f8-157">-ResourceGroupName</span></span>
<span data-ttu-id="731f8-158">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="731f8-159">-RestorePoint</span></span>
<span data-ttu-id="731f8-160">스냅숏 복원 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="731f8-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="731f8-162">만들 원본 SQL 풀 개체의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="731f8-163">-SourceResourceId</span></span>
<span data-ttu-id="731f8-164">만들 원본 SQL 풀 개체의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="731f8-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="731f8-166">만들 원본 SQL 풀 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="731f8-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="731f8-168">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="731f8-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="731f8-170">Synapse 작업 영역에서 만들 원본 SQL 풀 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-171">태그</span><span class="sxs-lookup"><span data-stu-id="731f8-171">-Tag</span></span>
<span data-ttu-id="731f8-172">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="731f8-173">-버전</span><span class="sxs-lookup"><span data-stu-id="731f8-173">-Version</span></span>
<span data-ttu-id="731f8-174">Synapse SQL 풀의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="731f8-175">예를 들면 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-175">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="731f8-176">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="731f8-176">-WorkspaceName</span></span>
<span data-ttu-id="731f8-177">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-178">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="731f8-178">-WorkspaceObject</span></span>
<span data-ttu-id="731f8-179">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="731f8-180">-확인</span><span class="sxs-lookup"><span data-stu-id="731f8-180">-Confirm</span></span>
<span data-ttu-id="731f8-181">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="731f8-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="731f8-182">-WhatIf</span></span>
<span data-ttu-id="731f8-183">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="731f8-184">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="731f8-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731f8-185">CommonParameters</span></span>
<span data-ttu-id="731f8-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="731f8-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731f8-187">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="731f8-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731f8-188">입력</span><span class="sxs-lookup"><span data-stu-id="731f8-188">INPUTS</span></span>

### <span data-ttu-id="731f8-189">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="731f8-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="731f8-190">출력</span><span class="sxs-lookup"><span data-stu-id="731f8-190">OUTPUTS</span></span>

### <span data-ttu-id="731f8-191">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="731f8-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="731f8-192">상속자</span><span class="sxs-lookup"><span data-stu-id="731f8-192">NOTES</span></span>

## <span data-ttu-id="731f8-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="731f8-193">RELATED LINKS</span></span>
