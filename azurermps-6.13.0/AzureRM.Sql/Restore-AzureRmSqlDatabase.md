---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: b4c444233701a6ecfe66eb77f90dade618c9e08f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530863"
---
# <span data-ttu-id="62524-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62524-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="62524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62524-102">SYNOPSIS</span></span>
<span data-ttu-id="62524-103">SQL 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62524-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62524-104">SYNTAX</span></span>

### <span data-ttu-id="62524-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="62524-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62524-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="62524-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62524-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="62524-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62524-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="62524-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62524-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="62524-109">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62524-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="62524-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62524-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="62524-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62524-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="62524-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62524-113">설명은</span><span class="sxs-lookup"><span data-stu-id="62524-113">DESCRIPTION</span></span>
<span data-ttu-id="62524-114">**AzureRmSqlDatabase** cmdlet은 지역 중복 백업의 SQL 데이터베이스, 삭제 된 데이터베이스의 백업, 장기 보존 백업 또는 라이브 데이터베이스의 특정 시점을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-114">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="62524-115">복원 된 데이터베이스는 새 데이터베이스로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="62524-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="62524-116">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정 하 여 탄력적 SQL 데이터베이스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62524-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="62524-117">예제의</span><span class="sxs-lookup"><span data-stu-id="62524-117">EXAMPLES</span></span>

### <span data-ttu-id="62524-118">예제 1: 지정 된 시점에서 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="62524-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="62524-119">첫 번째 명령은 Database01 이라는 SQL 데이터베이스를 가져온 다음이를 $Database 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="62524-120">두 번째 명령은 지정 된 특정 시점 백업 $Database의 데이터베이스를 RestoredDatabase 이라는 데이터베이스에 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="62524-121">예제 2: 특정 시점부터 탄력적 풀로 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="62524-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="62524-122">첫 번째 명령은 Database01 이라는 SQL 데이터베이스를 가져온 다음이를 $Database 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="62524-123">두 번째 명령은 지정 된 특정 시점 백업에서 $Database의 데이터베이스를 elasticpool01 이라는 탄력적 풀의 RestoredDatabase 이라는 SQL 데이터베이스로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="62524-124">예제 3: 삭제 된 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="62524-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="62524-125">첫 번째 명령은 Get-help를 사용 하 여 복원 하려는 삭제 된 데이터베이스 백업을 가져옵니다. [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="62524-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="62524-126">두 번째 명령은 [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet을 사용 하 여 삭제 된 데이터베이스 백업에서 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-126">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="62524-127">-PointInTime 매개 변수를 지정 하지 않으면 데이터베이스가 삭제 시간으로 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62524-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="62524-128">예제 4: 탄력적 풀에 삭제 된 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="62524-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="62524-129">첫 번째 명령은 Get-help를 사용 하 여 복원 하려는 삭제 된 데이터베이스 백업을 가져옵니다. [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="62524-129">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="62524-130">두 번째 명령은 [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)를 사용 하 여 삭제 된 데이터베이스 백업에서 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-130">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="62524-131">-PointInTime 매개 변수를 지정 하지 않으면 데이터베이스가 삭제 시간으로 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="62524-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="62524-132">예제 5: 데이터베이스 Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="62524-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="62524-133">첫 번째 명령은 Database01 이라는 데이터베이스에 대 한 지역 중복 백업을 가져온 다음이를 $GeoBackup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="62524-134">두 번째 명령은 $GeoBackup의 백업을 RestoredDatabase 이라는 SQL 데이터베이스에 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="62524-135">변수</span><span class="sxs-lookup"><span data-stu-id="62524-135">PARAMETERS</span></span>

### <span data-ttu-id="62524-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62524-136">-AsJob</span></span>
<span data-ttu-id="62524-137">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="62524-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62524-138">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="62524-138">-ComputeGeneration</span></span>
<span data-ttu-id="62524-139">복원 된 데이터베이스에 할당할 계산 생성</span><span class="sxs-lookup"><span data-stu-id="62524-139">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62524-140">-DefaultProfile</span></span>
<span data-ttu-id="62524-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="62524-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-142">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="62524-142">-DeletionDate</span></span>
<span data-ttu-id="62524-143">삭제 날짜를 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-143">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="62524-144">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-144">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62524-145">-에디션</span><span class="sxs-lookup"><span data-stu-id="62524-145">-Edition</span></span>
<span data-ttu-id="62524-146">SQL 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-146">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="62524-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="62524-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62524-148">않아야</span><span class="sxs-lookup"><span data-stu-id="62524-148">None</span></span>
- <span data-ttu-id="62524-149">기본적</span><span class="sxs-lookup"><span data-stu-id="62524-149">Basic</span></span>
- <span data-ttu-id="62524-150">표준이</span><span class="sxs-lookup"><span data-stu-id="62524-150">Standard</span></span>
- <span data-ttu-id="62524-151">Premium</span><span class="sxs-lookup"><span data-stu-id="62524-151">Premium</span></span>
- <span data-ttu-id="62524-152">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="62524-152">DataWarehouse</span></span>
- <span data-ttu-id="62524-153">비우거나</span><span class="sxs-lookup"><span data-stu-id="62524-153">Free</span></span>
- <span data-ttu-id="62524-154">늘이고</span><span class="sxs-lookup"><span data-stu-id="62524-154">Stretch</span></span>
- <span data-ttu-id="62524-155">일반 목적</span><span class="sxs-lookup"><span data-stu-id="62524-155">GeneralPurpose</span></span>
- <span data-ttu-id="62524-156">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="62524-156">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-157">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="62524-157">-ElasticPoolName</span></span>
<span data-ttu-id="62524-158">SQL 데이터베이스를 저장할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-158">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62524-159">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="62524-159">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="62524-160">이 cmdlet이 삭제 된 SQL 데이터베이스의 백업에서 데이터베이스를 복원 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="62524-160">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="62524-161">Get-AzureRMSqlDeletedDatabaseBackup cmdlet을 사용 하 여 삭제 된 SQL 데이터베이스의 백업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62524-161">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-162">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="62524-162">-FromGeoBackup</span></span>
<span data-ttu-id="62524-163">이 cmdlet이 지역 중복 백업의 SQL 데이터베이스를 복원 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="62524-163">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="62524-164">Get-AzureRMSqlDatabaseGeoBackup cmdlet을 사용 하 여 지역 중복 백업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62524-164">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-165">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="62524-165">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="62524-166">이 cmdlet이 장기 보존 백업에서 SQL 데이터베이스를 복원 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="62524-166">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-167">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="62524-167">-FromPointInTimeBackup</span></span>
<span data-ttu-id="62524-168">이 cmdlet이 지정 시간 백업 으로부터 SQL 데이터베이스를 복원 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="62524-168">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-169">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="62524-169">-LicenseType</span></span>
<span data-ttu-id="62524-170">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="62524-170">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-171">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="62524-171">-PointInTime</span></span>
<span data-ttu-id="62524-172">SQL 데이터베이스를 복원 하려는 시점을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-172">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="62524-173">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-173">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="62524-174">이 매개 변수를 *Frompointintimebackup* 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-174">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62524-175">-ResourceGroupName</span></span>
<span data-ttu-id="62524-176">이 cmdlet이 SQL 데이터베이스를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-176">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62524-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62524-177">-ResourceId</span></span>
<span data-ttu-id="62524-178">복원할 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-178">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62524-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62524-179">-ServerName</span></span>
<span data-ttu-id="62524-180">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-180">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62524-181">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="62524-181">-ServiceObjectiveName</span></span>
<span data-ttu-id="62524-182">서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-182">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62524-183">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="62524-183">-TargetDatabaseName</span></span>
<span data-ttu-id="62524-184">복원할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-184">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="62524-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="62524-185">-VCore</span></span>
<span data-ttu-id="62524-186">복원 된 Azure Sql Database의 Vcore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="62524-186">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62524-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62524-187">CommonParameters</span></span>
<span data-ttu-id="62524-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62524-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62524-189">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62524-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62524-190">입력</span><span class="sxs-lookup"><span data-stu-id="62524-190">INPUTS</span></span>

### <span data-ttu-id="62524-191">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="62524-191">System.DateTime</span></span>

### <span data-ttu-id="62524-192">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62524-192">System.String</span></span>

## <span data-ttu-id="62524-193">출력</span><span class="sxs-lookup"><span data-stu-id="62524-193">OUTPUTS</span></span>

### <span data-ttu-id="62524-194">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="62524-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="62524-195">상속자</span><span class="sxs-lookup"><span data-stu-id="62524-195">NOTES</span></span>

## <span data-ttu-id="62524-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62524-196">RELATED LINKS</span></span>

[<span data-ttu-id="62524-197">작동 중지에서 Azure SQL 데이터베이스 복구</span><span class="sxs-lookup"><span data-stu-id="62524-197">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="62524-198">사용자 오류에서 Azure SQL 데이터베이스 복구</span><span class="sxs-lookup"><span data-stu-id="62524-198">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="62524-199">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62524-199">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="62524-200">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="62524-200">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="62524-201">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="62524-201">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="62524-202">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="62524-202">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

