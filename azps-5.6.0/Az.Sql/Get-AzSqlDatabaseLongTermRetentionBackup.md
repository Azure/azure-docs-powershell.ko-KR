---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ad44b9dcec002a76581a583eb75de430454f4d59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974299"
---
# <span data-ttu-id="3b6df-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3b6df-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="3b6df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b6df-102">SYNOPSIS</span></span>
<span data-ttu-id="3b6df-103">하나 이상의 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="3b6df-104">구문</span><span class="sxs-lookup"><span data-stu-id="3b6df-104">SYNTAX</span></span>

### <span data-ttu-id="3b6df-105">위치(기본값)</span><span class="sxs-lookup"><span data-stu-id="3b6df-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6df-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="3b6df-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6df-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="3b6df-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6df-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b6df-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6df-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b6df-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6df-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b6df-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b6df-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b6df-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b6df-112">설명</span><span class="sxs-lookup"><span data-stu-id="3b6df-112">DESCRIPTION</span></span>
<span data-ttu-id="3b6df-113">**Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet은 위치, 서버 또는 데이터베이스에 대한 모든 장기 보존 백업을 얻거나 특정 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="3b6df-114">예제</span><span class="sxs-lookup"><span data-stu-id="3b6df-114">EXAMPLES</span></span>

### <span data-ttu-id="3b6df-115">예제 1: 위치에 대한 모든 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="3b6df-116">이 명령은 northeurope의 모든 데이터베이스에 대한 장기 보존 백업을 모두 얻게 되고(살아 있을 수도 또는 삭제될 수 있습니다) 서버가 있는 경우 리소스 그룹이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="3b6df-117">예제 2: 리소스 그룹 아래 위치에 대한 모든 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-117">Example 2: Get all backups for a location under a resource group</span></span>
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

<span data-ttu-id="3b6df-118">이 명령은 northeurope의 리소스 그룹 아래에 있는 모든 데이터베이스에 대한 모든 장기 보존 백업(살아 있을 수도 또는 삭제될 수 있습니다)을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="3b6df-119">예제 3: 특정 장기 보존 백업을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-119">Example 3: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="3b6df-120">이 명령은 이름 601061b7-d10b-46e0-bf77-a2bfb16a6add;131656655000000000으로 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="3b6df-121">예제 4: 데이터베이스에 대한 모든 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-121">Example 4: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="3b6df-122">이 명령은 Database01에 대한 모든 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="3b6df-123">예제 5: 필터링을 사용하여 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-123">Example 5: Get long term retention backups using filtering</span></span>
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

<span data-ttu-id="3b6df-124">이 명령은 "601061b7"로 시작하는 이름으로 모든 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="3b6df-125">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3b6df-125">PARAMETERS</span></span>

### <span data-ttu-id="3b6df-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="3b6df-126">-BackupName</span></span>
<span data-ttu-id="3b6df-127">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-127">The name of the backup.</span></span>

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

### <span data-ttu-id="3b6df-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3b6df-128">-DatabaseName</span></span>
<span data-ttu-id="3b6df-129">백업이 시작된 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-129">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="3b6df-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="3b6df-130">-DatabaseState</span></span>
<span data-ttu-id="3b6df-131">찾을 백업, Alive, Deleted 또는 All을 찾은 데이터베이스의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="3b6df-132">기본값을 모두로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-132">Defaults to All</span></span>

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

### <span data-ttu-id="3b6df-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b6df-133">-DefaultProfile</span></span>
<span data-ttu-id="3b6df-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b6df-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b6df-135">-InputObject</span></span>
<span data-ttu-id="3b6df-136">백업을 받을 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-136">The database object to get backups for.</span></span>

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

### <span data-ttu-id="3b6df-137">-Location</span><span class="sxs-lookup"><span data-stu-id="3b6df-137">-Location</span></span>
<span data-ttu-id="3b6df-138">백업의 원본 서버의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-138">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="3b6df-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="3b6df-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="3b6df-140">데이터베이스당 최신 백업만 받을지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="3b6df-141">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-141">Defaults to false.</span></span>

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

### <span data-ttu-id="3b6df-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b6df-142">-ResourceGroupName</span></span>
<span data-ttu-id="3b6df-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="3b6df-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b6df-144">-ResourceId</span></span>
<span data-ttu-id="3b6df-145">백업을 받을 데이터베이스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-145">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="3b6df-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3b6df-146">-ServerName</span></span>
<span data-ttu-id="3b6df-147">백업이 SQL Server Azure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-147">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="3b6df-148">-확인</span><span class="sxs-lookup"><span data-stu-id="3b6df-148">-Confirm</span></span>
<span data-ttu-id="3b6df-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b6df-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b6df-150">-WhatIf</span></span>
<span data-ttu-id="3b6df-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b6df-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b6df-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b6df-153">CommonParameters</span></span>
<span data-ttu-id="3b6df-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3b6df-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b6df-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b6df-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b6df-156">입력</span><span class="sxs-lookup"><span data-stu-id="3b6df-156">INPUTS</span></span>

### <span data-ttu-id="3b6df-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3b6df-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="3b6df-158">System.String</span><span class="sxs-lookup"><span data-stu-id="3b6df-158">System.String</span></span>

## <span data-ttu-id="3b6df-159">출력</span><span class="sxs-lookup"><span data-stu-id="3b6df-159">OUTPUTS</span></span>

### <span data-ttu-id="3b6df-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="3b6df-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="3b6df-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3b6df-161">NOTES</span></span>

## <span data-ttu-id="3b6df-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b6df-162">RELATED LINKS</span></span>

[<span data-ttu-id="3b6df-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3b6df-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3b6df-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3b6df-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3b6df-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3b6df-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3b6df-166">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="3b6df-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)