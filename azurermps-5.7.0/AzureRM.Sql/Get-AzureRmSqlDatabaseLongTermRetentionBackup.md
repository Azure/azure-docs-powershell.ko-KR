---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: da3b47923f39e6910566a210ddbd325d9da76ca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524848"
---
# <span data-ttu-id="8c1f2-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8c1f2-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="8c1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1f2-103">하나 또는 그 이상의 장기 보존 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-103">Gets one or more long term retention backups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c1f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c1f2-104">SYNTAX</span></span>

### <span data-ttu-id="8c1f2-105">위치 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8c1f2-105">Location (Default)</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c1f2-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="8c1f2-106">ServerName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [[-DatabaseName] <String>] [-OnlyLatestPerDatabase] [[-DatabaseState] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f2-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="8c1f2-107">BackupName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f2-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c1f2-108">GetBackupByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f2-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c1f2-109">GetBackupsByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f2-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="8c1f2-110">GetBackupByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1f2-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="8c1f2-111">GetBackupsByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [[-DatabaseState] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c1f2-112">설명은</span><span class="sxs-lookup"><span data-stu-id="8c1f2-112">DESCRIPTION</span></span>
<span data-ttu-id="8c1f2-113">**AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet은 위치, 서버 또는 데이터베이스에 대 한 장기 보존 백업을 모두 가져오거나 특정 장기 보존 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-113">The **Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="8c1f2-114">예제의</span><span class="sxs-lookup"><span data-stu-id="8c1f2-114">EXAMPLES</span></span>

### <span data-ttu-id="8c1f2-115">예제 1: 위치에 대 한 모든 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c1f2-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="8c1f2-116">이 명령은 northeurope의 모든 데이터베이스 (활성 또는 삭제 될 수 있음)에 대 한 장기 보존 백업을 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="8c1f2-117">예제 2: 특정 장기 보존 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c1f2-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="8c1f2-118">이 명령은 이름이 601061b7-d10b-46e0-bf77-a2bfb16a6add 인 백업을 가져옵니다. 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="8c1f2-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="8c1f2-119">예제 3: 데이터베이스에 대 한 모든 장기 보존 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="8c1f2-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzureRmSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="8c1f2-120">이 명령은 database01 용 장기 보존 백업을 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-120">This command gets all long term retention backups for database01</span></span>

## <span data-ttu-id="8c1f2-121">변수</span><span class="sxs-lookup"><span data-stu-id="8c1f2-121">PARAMETERS</span></span>

### <span data-ttu-id="8c1f2-122">-BackupName</span><span class="sxs-lookup"><span data-stu-id="8c1f2-122">-BackupName</span></span>
<span data-ttu-id="8c1f2-123">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-123">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c1f2-124">-DatabaseName</span></span>
<span data-ttu-id="8c1f2-125">백업이 있는 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-125">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: ServerName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-126">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="8c1f2-126">-DatabaseState</span></span>
<span data-ttu-id="8c1f2-127">백업을 검색, 활성화, 삭제 또는 모두 사용할 데이터베이스의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-127">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="8c1f2-128">기본적으로 모두</span><span class="sxs-lookup"><span data-stu-id="8c1f2-128">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1f2-129">-DefaultProfile</span></span>
<span data-ttu-id="8c1f2-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c1f2-131">-InputObject</span></span>
<span data-ttu-id="8c1f2-132">백업을 가져올 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-132">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-133">-위치</span><span class="sxs-lookup"><span data-stu-id="8c1f2-133">-Location</span></span>
<span data-ttu-id="8c1f2-134">백업의 원본 서버 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-134">The location of the backups' source server.</span></span>

```yaml
Type: String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-135">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="8c1f2-135">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="8c1f2-136">데이터베이스당 최신 백업만 받을지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-136">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="8c1f2-137">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-137">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c1f2-138">-ResourceId</span></span>
<span data-ttu-id="8c1f2-139">백업을 가져올 데이터베이스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-139">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c1f2-140">-ServerName</span></span>
<span data-ttu-id="8c1f2-141">백업이 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-141">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-142">-확인</span><span class="sxs-lookup"><span data-stu-id="8c1f2-142">-Confirm</span></span>
<span data-ttu-id="8c1f2-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c1f2-144">-WhatIf</span></span>
<span data-ttu-id="8c1f2-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c1f2-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1f2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1f2-147">CommonParameters</span></span>
<span data-ttu-id="8c1f2-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8c1f2-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c1f2-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1f2-150">입력</span><span class="sxs-lookup"><span data-stu-id="8c1f2-150">INPUTS</span></span>

### <span data-ttu-id="8c1f2-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8c1f2-151">System.String</span></span>
<span data-ttu-id="8c1f2-152">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="8c1f2-152">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8c1f2-153">출력</span><span class="sxs-lookup"><span data-stu-id="8c1f2-153">OUTPUTS</span></span>

### <span data-ttu-id="8c1f2-154">AzureSqlDatabaseLongTermRetentionBackupModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="8c1f2-154">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="8c1f2-155">상속자</span><span class="sxs-lookup"><span data-stu-id="8c1f2-155">NOTES</span></span>

## <span data-ttu-id="8c1f2-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c1f2-156">RELATED LINKS</span></span>

[<span data-ttu-id="8c1f2-157">제거-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8c1f2-157">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8c1f2-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c1f2-158">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8c1f2-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8c1f2-159">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8c1f2-160">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8c1f2-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
