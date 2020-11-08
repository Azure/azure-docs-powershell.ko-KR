---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045426"
---
# <span data-ttu-id="8f35d-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="8f35d-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="8f35d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f35d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f35d-103">데이터베이스의 특정 시점 복원을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="8f35d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f35d-104">SYNTAX</span></span>

### <span data-ttu-id="8f35d-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8f35d-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8f35d-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8f35d-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8f35d-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f35d-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8f35d-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f35d-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f35d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8f35d-109">DESCRIPTION</span></span>
<span data-ttu-id="8f35d-110">**AzureSqlDatabaseRestore** Cmdlet은 기본, 표준 또는 Premium 데이터베이스의 특정 시점 복원을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="8f35d-111">Azure SQL Database에는 7 일, 표준, 14 일간의 기본 데이터베이스 백업 및 35 일간의 Premium이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="8f35d-112">복원 작업을 수행 하면 새 데이터베이스가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="8f35d-113">원본 데이터베이스가 삭제 되지 않은 경우 *sourcedatabasename* 및 *targetdatabasename* 매개 변수는 다른 값을 가져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="8f35d-114">Azure SQL Database는 현재 교차 서버 복원을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="8f35d-115">원본 및 대상 서버 이름은 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="8f35d-116">예제의</span><span class="sxs-lookup"><span data-stu-id="8f35d-116">EXAMPLES</span></span>

### <span data-ttu-id="8f35d-117">예제 1: 개체를 지정 된 시점으로 복원</span><span class="sxs-lookup"><span data-stu-id="8f35d-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="8f35d-118">첫 번째 명령은 Server01 이라는 서버의 Database17 이라는 데이터베이스의 데이터베이스 개체를 가져온 다음이를 $Database 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="8f35d-119">두 번째 명령은 데이터베이스를 지정 된 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="8f35d-120">명령이 새 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="8f35d-121">예제 2: 이름으로 지정 된 데이터베이스를 특정 시점으로 복원</span><span class="sxs-lookup"><span data-stu-id="8f35d-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="8f35d-122">이 명령은 Database17 이라는 데이터베이스를 지정 된 시점으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="8f35d-123">명령이 새 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="8f35d-124">예제 3: 개체를 지정 된 시점에 놓을 때 손실 되는 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="8f35d-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="8f35d-125">첫 번째 명령은 Server01 라는 서버의 Database01 이라는 데이터베이스의 데이터베이스 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="8f35d-126">명령에서 *RestorableDropped* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="8f35d-127">따라서 cmdlet은 지정 된 복원 지점을 restorable 하 여 데이터베이스를 삭제 했습니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="8f35d-128">명령이 $Database 변수에 해당 데이터베이스 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="8f35d-129">두 번째 명령은 $Database에서 지정한 손실 된 데이터베이스를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="8f35d-130">명령이 새 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="8f35d-131">변수</span><span class="sxs-lookup"><span data-stu-id="8f35d-131">PARAMETERS</span></span>

### <span data-ttu-id="8f35d-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="8f35d-132">-PointInTime</span></span>
<span data-ttu-id="8f35d-133">데이터베이스를 복원할 복원 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="8f35d-134">복원 작업이 완료 되 면 데이터베이스는이 매개 변수에서 지정 하는 날짜 및 시간에 원래 상태로 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="8f35d-135">현재 시간으로 설정 된 라이브 데이터베이스와 손실 된 데이터베이스의 경우 기본적으로이 cmdlet은 데이터베이스가 삭제 된 시간을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="8f35d-136">-Profile</span></span>
<span data-ttu-id="8f35d-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f35d-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="8f35d-139">-RestorableDropped</span></span>
<span data-ttu-id="8f35d-140">이 cmdlet이 restorable 손실 된 데이터베이스를 복원 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-141">-원본 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="8f35d-141">-SourceDatabase</span></span>
<span data-ttu-id="8f35d-142">이 cmdlet이 복원 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="8f35d-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="8f35d-144">데이터베이스가 삭제 된 날짜와 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="8f35d-145">실제 데이터베이스 삭제 시간과 일치 하는 시간을 지정할 때는 밀리초를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f35d-146">-SourceDatabaseName</span></span>
<span data-ttu-id="8f35d-147">이 cmdlet이 복원 하는 라이브 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="8f35d-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="8f35d-149">이 cmdlet이 복원 하는 restorable 손실 된 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="8f35d-150">**RestorableDroppedDatabase** 개체를 가져오려면 Get-AzureSqlDatabase cmdlet을 사용 하 고 *RestorableDropped* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="8f35d-151">-SourceServerName</span></span>
<span data-ttu-id="8f35d-152">원본 데이터베이스가 실시간으로 실행 되는 서버의 이름을 지정 하거나 원본 데이터베이스를 삭제 하기 전에 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-153">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f35d-153">-TargetDatabaseName</span></span>
<span data-ttu-id="8f35d-154">복원 작업이 만드는 새 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-154">Specifies the name of the new database that the restore operation creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="8f35d-155">-TargetServerName</span></span>
<span data-ttu-id="8f35d-156">이 cmdlet이 데이터베이스를 복원할 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="8f35d-157">Azure SQL Database는 현재 교차 서버 복원을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="8f35d-158">원본 및 대상 서버 이름은 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-158">The source and target server names must be the same.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f35d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f35d-159">CommonParameters</span></span>
<span data-ttu-id="8f35d-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f35d-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f35d-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f35d-162">입력</span><span class="sxs-lookup"><span data-stu-id="8f35d-162">INPUTS</span></span>

### <span data-ttu-id="8f35d-163">WindowsAzure. SqlDatabase에 대 한 RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="8f35d-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="8f35d-164">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="8f35d-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="8f35d-165">출력</span><span class="sxs-lookup"><span data-stu-id="8f35d-165">OUTPUTS</span></span>

### <span data-ttu-id="8f35d-166">WindowsAzure. SqlDatabase에 대 한 RestoreDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="8f35d-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="8f35d-167">상속자</span><span class="sxs-lookup"><span data-stu-id="8f35d-167">NOTES</span></span>
* <span data-ttu-id="8f35d-168">이 cmdlet을 실행 하려면 인증서 기반 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="8f35d-169">이 cmdlet을 실행 하는 컴퓨터에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f35d-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="8f35d-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f35d-170">RELATED LINKS</span></span>

[<span data-ttu-id="8f35d-171">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="8f35d-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="8f35d-172">데이터베이스 복원 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="8f35d-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="8f35d-173">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="8f35d-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="8f35d-174">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f35d-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


