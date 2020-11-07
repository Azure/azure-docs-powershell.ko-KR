---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: fc6c6c2756ecb1c4174fc1255c175a49f66360cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873707"
---
# <span data-ttu-id="af647-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="af647-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="af647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af647-102">SYNOPSIS</span></span>
<span data-ttu-id="af647-103">하나 또는 그 이상의 장기 보존 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af647-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="af647-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af647-104">SYNTAX</span></span>

### <span data-ttu-id="af647-105">위치 (기본값)</span><span class="sxs-lookup"><span data-stu-id="af647-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [[-ResourceGroupName] <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af647-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="af647-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [[-ResourceGroupName] <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af647-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="af647-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af647-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="af647-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af647-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="af647-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af647-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="af647-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af647-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="af647-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af647-112">설명은</span><span class="sxs-lookup"><span data-stu-id="af647-112">DESCRIPTION</span></span>
<span data-ttu-id="af647-113">**AzSqlDatabaseLongTermRetentionBackup** cmdlet은 위치, 서버 또는 데이터베이스에 대 한 장기 보존 백업을 모두 가져오거나 특정 장기 보존 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af647-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="af647-114">예제의</span><span class="sxs-lookup"><span data-stu-id="af647-114">EXAMPLES</span></span>

### <span data-ttu-id="af647-115">예제 1: 위치에 대 한 모든 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="af647-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="af647-116">이 명령은 northeurope의 모든 데이터베이스 (활성 또는 삭제 될 수 있음)에 대 한 장기 보존 백업을 모두 가져옵니다. 서버가 활성 상태인 경우에만 리소스 그룹이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af647-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="af647-117">예제 2: 리소스 그룹 아래에 있는 위치에 대 한 모든 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="af647-117">Example 2: Get all backups for a location under a resource group</span></span>
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

<span data-ttu-id="af647-118">이 명령은 northeurope의 리소스 그룹 아래에서 모든 데이터베이스 (활성 또는 삭제 될 수 있음)에 대 한 장기 보존 백업을 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af647-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="af647-119">예제 3: 특정 장기 보존 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="af647-119">Example 3: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="af647-120">이 명령은 이름이 601061b7-d10b-46e0-bf77-a2bfb16a6add 인 백업을 가져옵니다. 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="af647-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="af647-121">예제 4: 모든 장기 보존 데이터베이스에 대 한 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="af647-121">Example 4: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="af647-122">이 명령은 database01 용 장기 보존 백업을 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af647-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="af647-123">예제 5: 필터링을 사용 하 여 장기 보존 백업 받기</span><span class="sxs-lookup"><span data-stu-id="af647-123">Example 5: Get long term retention backups using filtering</span></span>
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

<span data-ttu-id="af647-124">이 명령은 이름이 "601061b7"로 시작 하는 모든 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af647-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="af647-125">변수</span><span class="sxs-lookup"><span data-stu-id="af647-125">PARAMETERS</span></span>

### <span data-ttu-id="af647-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="af647-126">-BackupName</span></span>
<span data-ttu-id="af647-127">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-127">The name of the backup.</span></span>

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

### <span data-ttu-id="af647-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="af647-128">-DatabaseName</span></span>
<span data-ttu-id="af647-129">백업이 있는 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-129">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="af647-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="af647-130">-DatabaseState</span></span>
<span data-ttu-id="af647-131">백업을 검색, 활성화, 삭제 또는 모두 사용할 데이터베이스의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="af647-132">기본적으로 모두</span><span class="sxs-lookup"><span data-stu-id="af647-132">Defaults to All</span></span>

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

### <span data-ttu-id="af647-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af647-133">-DefaultProfile</span></span>
<span data-ttu-id="af647-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af647-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af647-135">-InputObject</span></span>
<span data-ttu-id="af647-136">백업을 가져올 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-136">The database object to get backups for.</span></span>

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

### <span data-ttu-id="af647-137">-위치</span><span class="sxs-lookup"><span data-stu-id="af647-137">-Location</span></span>
<span data-ttu-id="af647-138">백업의 원본 서버 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-138">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="af647-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="af647-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="af647-140">데이터베이스당 최신 백업만 받을지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af647-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="af647-141">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-141">Defaults to false.</span></span>

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

### <span data-ttu-id="af647-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af647-142">-ResourceGroupName</span></span>
<span data-ttu-id="af647-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af647-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af647-144">-ResourceId</span></span>
<span data-ttu-id="af647-145">백업을 가져올 데이터베이스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-145">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="af647-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af647-146">-ServerName</span></span>
<span data-ttu-id="af647-147">백업이 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af647-147">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="af647-148">-확인</span><span class="sxs-lookup"><span data-stu-id="af647-148">-Confirm</span></span>
<span data-ttu-id="af647-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af647-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af647-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af647-150">-WhatIf</span></span>
<span data-ttu-id="af647-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="af647-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af647-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af647-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af647-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af647-153">CommonParameters</span></span>
<span data-ttu-id="af647-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af647-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af647-155">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af647-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af647-156">입력</span><span class="sxs-lookup"><span data-stu-id="af647-156">INPUTS</span></span>

### <span data-ttu-id="af647-157">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="af647-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="af647-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="af647-158">System.String</span></span>

## <span data-ttu-id="af647-159">출력</span><span class="sxs-lookup"><span data-stu-id="af647-159">OUTPUTS</span></span>

### <span data-ttu-id="af647-160">AzureSqlDatabaseLongTermRetentionBackupModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="af647-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="af647-161">상속자</span><span class="sxs-lookup"><span data-stu-id="af647-161">NOTES</span></span>

## <span data-ttu-id="af647-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af647-162">RELATED LINKS</span></span>

[<span data-ttu-id="af647-163">제거-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="af647-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="af647-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="af647-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="af647-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="af647-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="af647-166">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="af647-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)