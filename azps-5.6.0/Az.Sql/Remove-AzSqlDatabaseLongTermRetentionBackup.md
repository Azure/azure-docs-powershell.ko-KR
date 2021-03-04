---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 01f9d475e678cee5b2fc131108a18bc5abec280d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957931"
---
# <span data-ttu-id="8a42a-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8a42a-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="8a42a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a42a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a42a-103">장기 보존 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="8a42a-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a42a-104">SYNTAX</span></span>

### <span data-ttu-id="8a42a-105">RemoveBackupDefault(기본값)</span><span class="sxs-lookup"><span data-stu-id="8a42a-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a42a-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="8a42a-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a42a-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a42a-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a42a-108">설명</span><span class="sxs-lookup"><span data-stu-id="8a42a-108">DESCRIPTION</span></span>
<span data-ttu-id="8a42a-109">**Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet은 지정된 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="8a42a-110">예제</span><span class="sxs-lookup"><span data-stu-id="8a42a-110">EXAMPLES</span></span>

### <span data-ttu-id="8a42a-111">예제 1: 리소스 그룹을 통해 단일 백업 삭제</span><span class="sxs-lookup"><span data-stu-id="8a42a-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


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

<span data-ttu-id="8a42a-112">이름 601061b7-d10b-46e0-bf77-a2bfb16a6add;131656655000000000으로 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="8a42a-113">예제 2: 리소스 그룹 없이 단일 백업 삭제</span><span class="sxs-lookup"><span data-stu-id="8a42a-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


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

<span data-ttu-id="8a42a-114">이름 601061b7-d10b-46e0-bf77-a2bfb16a6add;131656655000000000으로 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="8a42a-115">예제 3: 위치에 대한 모든 백업 삭제</span><span class="sxs-lookup"><span data-stu-id="8a42a-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="8a42a-116">이 명령은 northeurope 위치에 대한 모든 장기 보존 백업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="8a42a-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a42a-117">PARAMETERS</span></span>

### <span data-ttu-id="8a42a-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="8a42a-118">-BackupName</span></span>
<span data-ttu-id="8a42a-119">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-119">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a42a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a42a-120">-DatabaseName</span></span>
<span data-ttu-id="8a42a-121">백업이 시작된 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-121">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a42a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a42a-122">-DefaultProfile</span></span>
<span data-ttu-id="8a42a-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a42a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8a42a-124">-Force</span></span>
<span data-ttu-id="8a42a-125">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="8a42a-125">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a42a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a42a-126">-InputObject</span></span>
<span data-ttu-id="8a42a-127">제거할 데이터베이스 장기 보존 백업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a42a-128">-Location</span><span class="sxs-lookup"><span data-stu-id="8a42a-128">-Location</span></span>
<span data-ttu-id="8a42a-129">백업의 원본 서버의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-129">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a42a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a42a-130">-ResourceGroupName</span></span>
<span data-ttu-id="8a42a-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a42a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a42a-132">-ResourceId</span></span>
<span data-ttu-id="8a42a-133">제거할 데이터베이스 장기 보존 백업의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a42a-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8a42a-134">-ServerName</span></span>
<span data-ttu-id="8a42a-135">백업이 SQL Server Azure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-135">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a42a-136">-확인</span><span class="sxs-lookup"><span data-stu-id="8a42a-136">-Confirm</span></span>
<span data-ttu-id="8a42a-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a42a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a42a-138">-WhatIf</span></span>
<span data-ttu-id="8a42a-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a42a-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a42a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a42a-141">CommonParameters</span></span>
<span data-ttu-id="8a42a-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a42a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a42a-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a42a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a42a-144">입력</span><span class="sxs-lookup"><span data-stu-id="8a42a-144">INPUTS</span></span>

### <span data-ttu-id="8a42a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8a42a-145">System.String</span></span>

## <span data-ttu-id="8a42a-146">출력</span><span class="sxs-lookup"><span data-stu-id="8a42a-146">OUTPUTS</span></span>

### <span data-ttu-id="8a42a-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="8a42a-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="8a42a-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a42a-148">NOTES</span></span>

## <span data-ttu-id="8a42a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a42a-149">RELATED LINKS</span></span>

[<span data-ttu-id="8a42a-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8a42a-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8a42a-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8a42a-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8a42a-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8a42a-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8a42a-153">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8a42a-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)