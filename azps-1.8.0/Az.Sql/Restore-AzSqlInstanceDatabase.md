---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698812"
---
# <span data-ttu-id="ea2eb-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ea2eb-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="ea2eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2eb-103">Azure SQL 관리 인스턴스 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="ea2eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea2eb-104">SYNTAX</span></span>

### <span data-ttu-id="ea2eb-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea2eb-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea2eb-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ea2eb-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea2eb-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ea2eb-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea2eb-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="ea2eb-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea2eb-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ea2eb-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea2eb-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ea2eb-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea2eb-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ea2eb-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea2eb-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ea2eb-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea2eb-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="ea2eb-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea2eb-114">설명은</span><span class="sxs-lookup"><span data-stu-id="ea2eb-114">DESCRIPTION</span></span>
<span data-ttu-id="ea2eb-115">**Restore-AzSqlInstanceDatabase** cmdlet은 지역 중복 백업 또는 라이브 데이터베이스의 특정 시점에서 인스턴스 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="ea2eb-116">복원 된 데이터베이스는 새 인스턴스 데이터베이스로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="ea2eb-117">예제의</span><span class="sxs-lookup"><span data-stu-id="ea2eb-117">EXAMPLES</span></span>

### <span data-ttu-id="ea2eb-118">예제 1: 지정 된 시점에서 인스턴스 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="ea2eb-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="ea2eb-119">이 명령은 지정 된 특정 시점 백업에서 인스턴스 데이터베이스 Database01를 Database01_restored 라는 인스턴스 데이터베이스로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="ea2eb-120">예제 2: 다른 리소스 그룹의 특정 시점에서 다른 인스턴스로 인스턴스 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="ea2eb-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="ea2eb-121">이 명령은 managedInstance1에서 리소스 그룹 ResourceGroup02의 인스턴스 데이터베이스 Database01를 지정 된 특정 시점 백업에서 ResourceGroup01 인스턴스에 있는 인스턴스 Database01_restored 데이터베이스 ($ managedInstance2)로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="ea2eb-122">예제 3: 인스턴스 데이터베이스 Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="ea2eb-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="ea2eb-123">첫 번째 명령은 Database01 이라는 데이터베이스에 대 한 지역 중복 백업을 가져온 다음이를 $GeoBackup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="ea2eb-124">두 번째 명령은 $GeoBackup의 백업을 Database01_restored 라는 인스턴스 데이터베이스로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="ea2eb-125">변수</span><span class="sxs-lookup"><span data-stu-id="ea2eb-125">PARAMETERS</span></span>

### <span data-ttu-id="ea2eb-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea2eb-126">-AsJob</span></span>
<span data-ttu-id="ea2eb-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ea2eb-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea2eb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2eb-128">-DefaultProfile</span></span>
<span data-ttu-id="ea2eb-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ea2eb-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="ea2eb-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ea2eb-130">-FromGeoBackup</span></span>
<span data-ttu-id="ea2eb-131">지역 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-131">Restore from a geo backup.</span></span>

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

### <span data-ttu-id="ea2eb-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="ea2eb-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="ea2eb-133">지정 시간 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2eb-134">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="ea2eb-134">-GeoBackupObject</span></span>
<span data-ttu-id="ea2eb-135">복원할 복구 가능한 인스턴스 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="ea2eb-135">The recoverable instance database object to restore</span></span>

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

### <span data-ttu-id="ea2eb-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea2eb-136">-InputObject</span></span>
<span data-ttu-id="ea2eb-137">복원할 인스턴스 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="ea2eb-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2eb-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ea2eb-138">-InstanceName</span></span>
<span data-ttu-id="ea2eb-139">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2eb-140">-이름</span><span class="sxs-lookup"><span data-stu-id="ea2eb-140">-Name</span></span>
<span data-ttu-id="ea2eb-141">복원할 인스턴스 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2eb-142">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="ea2eb-142">-PointInTime</span></span>
<span data-ttu-id="ea2eb-143">데이터베이스를 복원할 시점을 지정 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2eb-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea2eb-144">-ResourceGroupName</span></span>
<span data-ttu-id="ea2eb-145">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2eb-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea2eb-146">-ResourceId</span></span>
<span data-ttu-id="ea2eb-147">복원할 인스턴스 데이터베이스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
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

### <span data-ttu-id="ea2eb-148">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea2eb-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="ea2eb-149">복원할 대상 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-149">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="ea2eb-150">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="ea2eb-150">-TargetInstanceName</span></span>
<span data-ttu-id="ea2eb-151">복원할 대상 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="ea2eb-152">지정 하지 않으면 대상 인스턴스가 원본 인스턴스와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2eb-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea2eb-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="ea2eb-154">복원할 대상 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="ea2eb-155">지정 하지 않으면 대상 리소스 그룹이 원본 리소스 그룹과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2eb-156">-확인</span><span class="sxs-lookup"><span data-stu-id="ea2eb-156">-Confirm</span></span>
<span data-ttu-id="ea2eb-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea2eb-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea2eb-158">-WhatIf</span></span>
<span data-ttu-id="ea2eb-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea2eb-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea2eb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2eb-161">CommonParameters</span></span>
<span data-ttu-id="ea2eb-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2eb-163">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea2eb-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2eb-164">입력</span><span class="sxs-lookup"><span data-stu-id="ea2eb-164">INPUTS</span></span>

### <span data-ttu-id="ea2eb-165">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="ea2eb-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="ea2eb-166">AzureSqlRecoverableManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="ea2eb-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="ea2eb-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea2eb-167">System.String</span></span>

## <span data-ttu-id="ea2eb-168">출력</span><span class="sxs-lookup"><span data-stu-id="ea2eb-168">OUTPUTS</span></span>

### <span data-ttu-id="ea2eb-169">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="ea2eb-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="ea2eb-170">상속자</span><span class="sxs-lookup"><span data-stu-id="ea2eb-170">NOTES</span></span>

## <span data-ttu-id="ea2eb-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea2eb-171">RELATED LINKS</span></span>
