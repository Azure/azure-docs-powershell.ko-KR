---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: be2e9342407cea6ba3da0bf239ee73e7b726dd82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043195"
---
# <span data-ttu-id="b43a4-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b43a4-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="b43a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b43a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b43a4-103">장기적 보존 백업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="b43a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b43a4-104">SYNTAX</span></span>

### <span data-ttu-id="b43a4-105">RemoveBackupDefault (기본값)</span><span class="sxs-lookup"><span data-stu-id="b43a4-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b43a4-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="b43a4-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b43a4-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="b43a4-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b43a4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b43a4-108">DESCRIPTION</span></span>
<span data-ttu-id="b43a4-109">**AzSqlDatabaseLongTermRetentionBackup** cmdlet은 지정 된 백업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="b43a4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b43a4-110">EXAMPLES</span></span>

### <span data-ttu-id="b43a4-111">예제 1: 리소스 그룹을 사용 하 여 단일 백업 삭제</span><span class="sxs-lookup"><span data-stu-id="b43a4-111">Example 1: Delete a single backup with resource group</span></span>
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

<span data-ttu-id="b43a4-112">이름이 601061b7-d10b-46e0-bf77-a2bfb16a6add 인 백업을 삭제 합니다. 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="b43a4-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="b43a4-113">예제 2: 리소스 그룹을 제외한 단일 백업 삭제</span><span class="sxs-lookup"><span data-stu-id="b43a4-113">Example 2: Delete a single backup without resource group</span></span>
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

<span data-ttu-id="b43a4-114">이름이 601061b7-d10b-46e0-bf77-a2bfb16a6add 인 백업을 삭제 합니다. 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="b43a4-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="b43a4-115">예제 3: 위치에 대 한 모든 백업 삭제</span><span class="sxs-lookup"><span data-stu-id="b43a4-115">Example 3: Delete all backups for a location</span></span>
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

<span data-ttu-id="b43a4-116">이 명령은 northeurope 위치에 대해 장기 보존 백업을 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="b43a4-117">변수</span><span class="sxs-lookup"><span data-stu-id="b43a4-117">PARAMETERS</span></span>

### <span data-ttu-id="b43a4-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="b43a4-118">-BackupName</span></span>
<span data-ttu-id="b43a4-119">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-119">The name of the backup.</span></span>

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

### <span data-ttu-id="b43a4-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b43a4-120">-DatabaseName</span></span>
<span data-ttu-id="b43a4-121">백업이 있는 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-121">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="b43a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43a4-122">-DefaultProfile</span></span>
<span data-ttu-id="b43a4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b43a4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b43a4-124">-Force</span></span>
<span data-ttu-id="b43a4-125">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="b43a4-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b43a4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b43a4-126">-InputObject</span></span>
<span data-ttu-id="b43a4-127">제거할 데이터베이스 장기 보존 백업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-127">The Database Long Term Retention Backup object to remove.</span></span>

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

### <span data-ttu-id="b43a4-128">-위치</span><span class="sxs-lookup"><span data-stu-id="b43a4-128">-Location</span></span>
<span data-ttu-id="b43a4-129">백업의 원본 서버 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-129">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="b43a4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43a4-130">-ResourceGroupName</span></span>
<span data-ttu-id="b43a4-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="b43a4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b43a4-132">-ResourceId</span></span>
<span data-ttu-id="b43a4-133">제거할 데이터베이스 장기 보존 백업의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="b43a4-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b43a4-134">-ServerName</span></span>
<span data-ttu-id="b43a4-135">백업이 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-135">The name of the Azure SQL Server the backup is under.</span></span>

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

### <span data-ttu-id="b43a4-136">-확인</span><span class="sxs-lookup"><span data-stu-id="b43a4-136">-Confirm</span></span>
<span data-ttu-id="b43a4-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b43a4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b43a4-138">-WhatIf</span></span>
<span data-ttu-id="b43a4-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b43a4-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b43a4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43a4-141">CommonParameters</span></span>
<span data-ttu-id="b43a4-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b43a4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43a4-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b43a4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43a4-144">입력</span><span class="sxs-lookup"><span data-stu-id="b43a4-144">INPUTS</span></span>

### <span data-ttu-id="b43a4-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b43a4-145">System.String</span></span>

## <span data-ttu-id="b43a4-146">출력</span><span class="sxs-lookup"><span data-stu-id="b43a4-146">OUTPUTS</span></span>

### <span data-ttu-id="b43a4-147">AzureSqlDatabaseLongTermRetentionBackupModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="b43a4-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="b43a4-148">상속자</span><span class="sxs-lookup"><span data-stu-id="b43a4-148">NOTES</span></span>

## <span data-ttu-id="b43a4-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b43a4-149">RELATED LINKS</span></span>

[<span data-ttu-id="b43a4-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b43a4-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b43a4-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b43a4-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b43a4-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b43a4-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b43a4-153">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b43a4-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)