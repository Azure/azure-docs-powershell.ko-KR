---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 4d8ece03cc5c1a96d73bcde79aef76c8f329b38a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216968"
---
# <span data-ttu-id="fd70c-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fd70c-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="fd70c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd70c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd70c-103">Azure SQL 관리 인스턴스 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="fd70c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd70c-104">SYNTAX</span></span>

### <span data-ttu-id="fd70c-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd70c-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd70c-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="fd70c-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd70c-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="fd70c-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd70c-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="fd70c-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd70c-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="fd70c-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd70c-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="fd70c-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd70c-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="fd70c-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd70c-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="fd70c-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd70c-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fd70c-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd70c-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fd70c-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd70c-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="fd70c-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd70c-116">LongTermRetentionBackupRestoreParameter</span><span class="sxs-lookup"><span data-stu-id="fd70c-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd70c-117">설명은</span><span class="sxs-lookup"><span data-stu-id="fd70c-117">DESCRIPTION</span></span>
<span data-ttu-id="fd70c-118">**Restore-AzSqlInstanceDatabase** cmdlet은 지역 중복 백업, 라이브 데이터베이스의 특정 시점 또는 장기 보존 백업에서 인스턴스 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="fd70c-119">복원 된 데이터베이스는 새 인스턴스 데이터베이스로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="fd70c-120">예제의</span><span class="sxs-lookup"><span data-stu-id="fd70c-120">EXAMPLES</span></span>

### <span data-ttu-id="fd70c-121">예제 1: 지정 된 시점에서 인스턴스 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="fd70c-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="fd70c-122">이 명령은 지정 된 특정 시점 백업에서 인스턴스 데이터베이스 Database01를 Database01_restored 라는 인스턴스 데이터베이스로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="fd70c-123">예제 2: 다른 리소스 그룹의 특정 시점에서 다른 인스턴스로 인스턴스 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="fd70c-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="fd70c-124">이 명령은 managedInstance1에서 리소스 그룹 ResourceGroup02의 인스턴스 데이터베이스 Database01를 지정 된 특정 시점 백업에서 ResourceGroup01 인스턴스에 있는 인스턴스 Database01_restored 데이터베이스 ($ managedInstance2)로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="fd70c-125">예제 3: 인스턴스 데이터베이스 Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="fd70c-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="fd70c-126">첫 번째 명령은 Database01 이라는 데이터베이스에 대 한 지역 중복 백업을 가져온 다음이를 $GeoBackup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="fd70c-127">두 번째 명령은 $GeoBackup의 백업을 Database01_restored 라는 인스턴스 데이터베이스로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="fd70c-128">예제 4: 지정 된 시점에서 삭제 한 인스턴스 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="fd70c-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="fd70c-129">첫 번째 명령은 ' managedInstance1 ' 인스턴스에서 ' DB1 ' 이라는 삭제 된 인스턴스 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="fd70c-130">두 번째 명령은 지정 된 특정 시점 백업에서 Database01_restored 이라는 인스턴스 데이터베이스로 페치된 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="fd70c-131">예제 5: 삭제 된 인스턴스 데이터베이스를 지정 된 시점에서 복원</span><span class="sxs-lookup"><span data-stu-id="fd70c-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="fd70c-132">첫 번째 명령은 ' managedInstance1 ' 인스턴스에서 ' DB1 ' 이라는 삭제 된 인스턴스 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="fd70c-133">두 번째 명령은 지정 된 특정 시점 백업에서 입력 개체를 사용 하 여 이름이 Database01_restored 인 인스턴스 데이터베이스로 페치된 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="fd70c-134">예제 6: LTR 백업에서 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="fd70c-134">Example 6: Restore a database from LTR backup.</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -FromLongTermRetentionBackup -ResourceId /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManagedInstances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000 -TargetInstanceDatabaseName restoreTarget -TargetInstanceName testInstance -TargetResourceGroupName testResourceGroup


Location                          : southeastasia
Tags                              :
Collation                         : SQL_Latin1_General_CP1_CI_AS
Status                            : Online
RestorePointInTime                :
DefaultSecondaryLocation          : northeurope
CatalogCollation                  :
CreateMode                        :
StorageContainerUri               :
StorageContainerSasToken          :
SourceDatabaseId                  :
FailoverGroupId                   :
RecoverableDatabaseId             :
RestorableDroppedDatabaseId       :
LongTermRetentionBackupResourceId :
ResourceGroupName                 : testResourceGroup
ManagedInstanceName               : testInstance
Name                              : restoreTarget
CreationDate                      : 3/4/2020 8:12:56 AM
EarliestRestorePoint              : 3/4/2020 8:14:29 AM
Id                                : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/managedInstances/testInstance/databases/restoreTarget
```

<span data-ttu-id="fd70c-135">지정 된 리소스 ID (Get-AzSqlInstanceDatabaseLongTermRetentionBackup를 실행 하 여 찾을 수 있음)로 LTR 백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="fd70c-136">변수</span><span class="sxs-lookup"><span data-stu-id="fd70c-136">PARAMETERS</span></span>

### <span data-ttu-id="fd70c-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd70c-137">-AsJob</span></span>
<span data-ttu-id="fd70c-138">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fd70c-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd70c-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd70c-139">-DefaultProfile</span></span>
<span data-ttu-id="fd70c-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fd70c-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="fd70c-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="fd70c-141">-DeletionDate</span></span>
<span data-ttu-id="fd70c-142">삭제 된 데이터베이스의 삭제 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-142">The deletion date of deleted database.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="fd70c-143">-FromGeoBackup</span></span>
<span data-ttu-id="fd70c-144">지역 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-144">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fd70c-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="fd70c-146">장기 보존 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-146">Restore from a Long Term Retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="fd70c-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="fd70c-148">지정 시간 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-148">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-149">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="fd70c-149">-GeoBackupObject</span></span>
<span data-ttu-id="fd70c-150">복원할 복구 가능한 인스턴스 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="fd70c-150">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-151">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd70c-151">-InputObject</span></span>
<span data-ttu-id="fd70c-152">복원할 인스턴스 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="fd70c-152">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-153">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fd70c-153">-InstanceName</span></span>
<span data-ttu-id="fd70c-154">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-154">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-155">-이름</span><span class="sxs-lookup"><span data-stu-id="fd70c-155">-Name</span></span>
<span data-ttu-id="fd70c-156">복원할 인스턴스 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-156">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName, SourceInstanceDatabaseName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-157">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="fd70c-157">-PointInTime</span></span>
<span data-ttu-id="fd70c-158">데이터베이스를 복원할 시점을 지정 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-158">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd70c-159">-ResourceGroupName</span></span>
<span data-ttu-id="fd70c-160">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd70c-161">-ResourceId</span></span>
<span data-ttu-id="fd70c-162">복원할 인스턴스 데이터베이스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-162">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fd70c-163">-SubscriptionId</span></span>
<span data-ttu-id="fd70c-164">원본 구독 id입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-164">Source subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, LongTermRetentionBackupRestoreParameter
Aliases: SourceSubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-165">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fd70c-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="fd70c-166">복원할 대상 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-166">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="fd70c-167">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="fd70c-167">-TargetInstanceName</span></span>
<span data-ttu-id="fd70c-168">복원할 대상 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="fd70c-169">지정 하지 않으면 대상 인스턴스가 원본 인스턴스와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-169">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd70c-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="fd70c-171">복원할 대상 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="fd70c-172">지정 하지 않으면 대상 리소스 그룹이 원본 리소스 그룹과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-172">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd70c-173">-확인</span><span class="sxs-lookup"><span data-stu-id="fd70c-173">-Confirm</span></span>
<span data-ttu-id="fd70c-174">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd70c-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd70c-175">-WhatIf</span></span>
<span data-ttu-id="fd70c-176">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd70c-177">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd70c-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd70c-178">CommonParameters</span></span>
<span data-ttu-id="fd70c-179">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd70c-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd70c-180">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fd70c-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd70c-181">입력</span><span class="sxs-lookup"><span data-stu-id="fd70c-181">INPUTS</span></span>

### <span data-ttu-id="fd70c-182">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="fd70c-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="fd70c-183">AzureSqlRecoverableManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="fd70c-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="fd70c-184">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd70c-184">System.String</span></span>

## <span data-ttu-id="fd70c-185">출력</span><span class="sxs-lookup"><span data-stu-id="fd70c-185">OUTPUTS</span></span>

### <span data-ttu-id="fd70c-186">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="fd70c-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="fd70c-187">상속자</span><span class="sxs-lookup"><span data-stu-id="fd70c-187">NOTES</span></span>

## <span data-ttu-id="fd70c-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd70c-188">RELATED LINKS</span></span>
