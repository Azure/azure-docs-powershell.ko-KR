---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529078"
---
# <span data-ttu-id="d1059-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d1059-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="d1059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1059-102">SYNOPSIS</span></span>
<span data-ttu-id="d1059-103">SQL 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1059-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1059-104">SYNTAX</span></span>

### <span data-ttu-id="d1059-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1059-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1059-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1059-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1059-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d1059-109">DESCRIPTION</span></span>
<span data-ttu-id="d1059-110">**AzureRmSqlDatabase** cmdlet은 지역 중복 백업의 SQL 데이터베이스, 삭제 된 데이터베이스의 백업, 장기 보존 백업 또는 라이브 데이터베이스의 특정 시점을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="d1059-111">복원 된 데이터베이스는 새 데이터베이스로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="d1059-112">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정 하 여 탄력적 SQL 데이터베이스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="d1059-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d1059-113">EXAMPLES</span></span>

### <span data-ttu-id="d1059-114">예제 1: 지정 된 시점에서 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="d1059-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="d1059-115">첫 번째 명령은 Database01 이라는 SQL 데이터베이스를 가져온 다음이를 $Database 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="d1059-116">두 번째 명령은 지정 된 특정 시점 백업 $Database의 데이터베이스를 RestoredDatabase 이라는 데이터베이스에 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="d1059-117">예제 2: 특정 시점부터 탄력적 풀로 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="d1059-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="d1059-118">첫 번째 명령은 Database01 이라는 SQL 데이터베이스를 가져온 다음이를 $Database 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="d1059-119">두 번째 명령은 지정 된 특정 시점 백업에서 $Database의 데이터베이스를 elasticpool01 이라는 탄력적 풀의 RestoredDatabase 이라는 SQL 데이터베이스로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="d1059-120">예제 3: 삭제 된 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="d1059-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="d1059-121">첫 번째 명령은 Get-help를 사용 하 여 복원 하려는 삭제 된 데이터베이스 백업을 가져옵니다. [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="d1059-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="d1059-122">두 번째 명령은 [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet을 사용 하 여 삭제 된 데이터베이스 백업에서 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="d1059-123">-PointInTime 매개 변수를 지정 하지 않으면 데이터베이스가 삭제 시간으로 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="d1059-124">예제 4: 탄력적 풀에 삭제 된 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="d1059-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="d1059-125">첫 번째 명령은 Get-help를 사용 하 여 복원 하려는 삭제 된 데이터베이스 백업을 가져옵니다. [AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="d1059-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="d1059-126">두 번째 명령은 [restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)를 사용 하 여 삭제 된 데이터베이스 백업에서 복원을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="d1059-127">-PointInTime 매개 변수를 지정 하지 않으면 데이터베이스가 삭제 시간으로 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="d1059-128">예제 5: 데이터베이스 Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="d1059-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="d1059-129">첫 번째 명령은 Database01 이라는 데이터베이스에 대 한 지역 중복 백업을 가져온 다음이를 $GeoBackup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="d1059-130">두 번째 명령은 $GeoBackup의 백업을 RestoredDatabase 이라는 SQL 데이터베이스에 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="d1059-131">변수</span><span class="sxs-lookup"><span data-stu-id="d1059-131">PARAMETERS</span></span>

### <span data-ttu-id="d1059-132">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="d1059-132">-DeletionDate</span></span>
<span data-ttu-id="d1059-133">삭제 날짜를 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-133">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="d1059-134">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-134">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-135">-에디션</span><span class="sxs-lookup"><span data-stu-id="d1059-135">-Edition</span></span>
<span data-ttu-id="d1059-136">SQL 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-136">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="d1059-137">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1059-138">않아야</span><span class="sxs-lookup"><span data-stu-id="d1059-138">None</span></span>
- <span data-ttu-id="d1059-139">Premium</span><span class="sxs-lookup"><span data-stu-id="d1059-139">Premium</span></span>
- <span data-ttu-id="d1059-140">기본적</span><span class="sxs-lookup"><span data-stu-id="d1059-140">Basic</span></span>
- <span data-ttu-id="d1059-141">표준이</span><span class="sxs-lookup"><span data-stu-id="d1059-141">Standard</span></span>
- <span data-ttu-id="d1059-142">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="d1059-142">DataWarehouse</span></span>
- <span data-ttu-id="d1059-143">비우거나</span><span class="sxs-lookup"><span data-stu-id="d1059-143">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-144">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d1059-144">-ElasticPoolName</span></span>
<span data-ttu-id="d1059-145">SQL 데이터베이스를 저장할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-145">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-146">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-146">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="d1059-147">이 cmdlet이 삭제 된 SQL 데이터베이스의 백업에서 데이터베이스를 복원 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-147">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="d1059-148">Get-AzureRMSqlDeletedDatabaseBackup cmdlet을 사용 하 여 삭제 된 SQL 데이터베이스의 백업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-148">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-149">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-149">-FromGeoBackup</span></span>
<span data-ttu-id="d1059-150">이 cmdlet이 지역 중복 백업의 SQL 데이터베이스를 복원 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-150">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="d1059-151">Get-AzureRMSqlDatabaseGeoBackup cmdlet을 사용 하 여 지역 중복 백업을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-151">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-152">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-152">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="d1059-153">이 cmdlet이 장기 보존 백업에서 SQL 데이터베이스를 복원 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-153">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-154">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-154">-FromPointInTimeBackup</span></span>
<span data-ttu-id="d1059-155">이 cmdlet이 지정 시간 백업 으로부터 SQL 데이터베이스를 복원 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-155">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-156">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="d1059-156">-PointInTime</span></span>
<span data-ttu-id="d1059-157">SQL 데이터베이스를 복원 하려는 시점을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-157">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="d1059-158">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-158">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="d1059-159">이 매개 변수를 *Frompointintimebackup* 매개 변수와 함께 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-159">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1059-160">-ResourceGroupName</span></span>
<span data-ttu-id="d1059-161">이 cmdlet이 SQL 데이터베이스를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-161">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="d1059-162">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1059-162">-ResourceId</span></span>
<span data-ttu-id="d1059-163">복원할 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-163">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="d1059-164">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1059-164">-ServerName</span></span>
<span data-ttu-id="d1059-165">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-165">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="d1059-166">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d1059-166">-ServiceObjectiveName</span></span>
<span data-ttu-id="d1059-167">서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-167">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1059-168">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1059-168">-TargetDatabaseName</span></span>
<span data-ttu-id="d1059-169">복원할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-169">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="d1059-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1059-170">-DefaultProfile</span></span>
<span data-ttu-id="d1059-171">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1059-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1059-172">CommonParameters</span></span>
<span data-ttu-id="d1059-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1059-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1059-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1059-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1059-175">입력</span><span class="sxs-lookup"><span data-stu-id="d1059-175">INPUTS</span></span>

## <span data-ttu-id="d1059-176">출력</span><span class="sxs-lookup"><span data-stu-id="d1059-176">OUTPUTS</span></span>

### <span data-ttu-id="d1059-177">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="d1059-177">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d1059-178">상속자</span><span class="sxs-lookup"><span data-stu-id="d1059-178">NOTES</span></span>

## <span data-ttu-id="d1059-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1059-179">RELATED LINKS</span></span>

[<span data-ttu-id="d1059-180">작동 중지에서 Azure SQL 데이터베이스 복구</span><span class="sxs-lookup"><span data-stu-id="d1059-180">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="d1059-181">사용자 오류에서 Azure SQL 데이터베이스 복구</span><span class="sxs-lookup"><span data-stu-id="d1059-181">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="d1059-182">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d1059-182">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="d1059-183">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-183">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="d1059-184">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="d1059-184">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="d1059-185">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d1059-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
