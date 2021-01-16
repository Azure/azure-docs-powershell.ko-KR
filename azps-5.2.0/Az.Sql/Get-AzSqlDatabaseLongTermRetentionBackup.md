---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363357"
---
# <span data-ttu-id="c257f-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c257f-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="c257f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c257f-102">SYNOPSIS</span></span>
<span data-ttu-id="c257f-103">하나 이상의 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="c257f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c257f-104">SYNTAX</span></span>

### <span data-ttu-id="c257f-105">위치(기본값)</span><span class="sxs-lookup"><span data-stu-id="c257f-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c257f-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="c257f-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c257f-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="c257f-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c257f-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="c257f-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c257f-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="c257f-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c257f-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="c257f-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c257f-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="c257f-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c257f-112">설명</span><span class="sxs-lookup"><span data-stu-id="c257f-112">DESCRIPTION</span></span>
<span data-ttu-id="c257f-113">**Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet은 위치, 서버 또는 데이터베이스에 대한 모든 장기 보존 백업을 얻거나 특정 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="c257f-114">예제</span><span class="sxs-lookup"><span data-stu-id="c257f-114">EXAMPLES</span></span>

### <span data-ttu-id="c257f-115">예제 1: 위치에 대한 모든 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="c257f-116">이 명령은 북유럽에 있는 모든 데이터베이스에 대한 모든 장기 보존 백업을 얻게 되고 서버가 라이브 상태인 경우 리소스 그룹이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="c257f-117">예제 2: 리소스 그룹 아래 위치에 대한 모든 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="c257f-118">이 명령은 northeurope의 리소스 그룹 아래에 있는 모든 데이터베이스에 대한 모든 장기 보존 백업을 얻습니다(연결되거나 삭제될 수 있습니다).</span><span class="sxs-lookup"><span data-stu-id="c257f-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="c257f-119">예제 3: 특정 장기 보존 백업을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="c257f-120">이 명령은 이름이 601061b7-d10b-46e0-bf77-a2bfb16a6add;1316566655000000인 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="c257f-121">예제 4: 데이터베이스에 대한 모든 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="c257f-122">이 명령은 database01에 대한 모든 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="c257f-123">예제 5: 필터링을 사용하여 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="c257f-124">이 명령은 "601061b7"으로 시작하는 이름으로 모든 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="c257f-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c257f-125">PARAMETERS</span></span>

### <span data-ttu-id="c257f-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="c257f-126">-BackupName</span></span>
<span data-ttu-id="c257f-127">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c257f-128">-DatabaseName</span></span>
<span data-ttu-id="c257f-129">백업이 있는 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-129">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="c257f-130">-DatabaseState</span></span>
<span data-ttu-id="c257f-131">백업을 찾거나, 연결하거나, 삭제하거나, 모두를 찾은 데이터베이스의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="c257f-132">기본값은 모두</span><span class="sxs-lookup"><span data-stu-id="c257f-132">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c257f-133">-DefaultProfile</span></span>
<span data-ttu-id="c257f-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c257f-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c257f-135">-InputObject</span></span>
<span data-ttu-id="c257f-136">백업을 받을 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-136">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-137">-Location</span><span class="sxs-lookup"><span data-stu-id="c257f-137">-Location</span></span>
<span data-ttu-id="c257f-138">백업의 원본 서버 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-138">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="c257f-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="c257f-140">데이터베이스당 최신 백업만 받을지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="c257f-141">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-141">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c257f-142">-ResourceGroupName</span></span>
<span data-ttu-id="c257f-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c257f-144">-ResourceId</span></span>
<span data-ttu-id="c257f-145">백업을 받을 데이터베이스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-145">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c257f-146">-ServerName</span></span>
<span data-ttu-id="c257f-147">백업이 있는 Azure SQL Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-147">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c257f-148">-Confirm</span></span>
<span data-ttu-id="c257f-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c257f-150">-WhatIf</span></span>
<span data-ttu-id="c257f-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c257f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c257f-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c257f-153">CommonParameters</span></span>
<span data-ttu-id="c257f-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c257f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c257f-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c257f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c257f-156">입력</span><span class="sxs-lookup"><span data-stu-id="c257f-156">INPUTS</span></span>

### <span data-ttu-id="c257f-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c257f-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="c257f-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c257f-158">System.String</span></span>

## <span data-ttu-id="c257f-159">출력</span><span class="sxs-lookup"><span data-stu-id="c257f-159">OUTPUTS</span></span>

### <span data-ttu-id="c257f-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="c257f-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="c257f-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c257f-161">NOTES</span></span>

## <span data-ttu-id="c257f-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c257f-162">RELATED LINKS</span></span>

[<span data-ttu-id="c257f-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c257f-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c257f-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c257f-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c257f-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c257f-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c257f-166">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c257f-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)