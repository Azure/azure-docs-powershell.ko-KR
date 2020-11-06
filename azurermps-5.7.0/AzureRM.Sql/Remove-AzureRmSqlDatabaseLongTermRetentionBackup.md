---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 93895a7fffe40309b73c3929f88ffebfe203767f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533579"
---
# <span data-ttu-id="00e67-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="00e67-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="00e67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00e67-102">SYNOPSIS</span></span>
<span data-ttu-id="00e67-103">장기적 보존 백업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-103">Deletes a long term retention backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00e67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00e67-104">SYNTAX</span></span>

### <span data-ttu-id="00e67-105">RemoveBackupDefault (기본값)</span><span class="sxs-lookup"><span data-stu-id="00e67-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e67-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="00e67-106">RemoveBackupByInputObject</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e67-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="00e67-107">RemoveBackupByResourceId</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00e67-108">설명은</span><span class="sxs-lookup"><span data-stu-id="00e67-108">DESCRIPTION</span></span>
<span data-ttu-id="00e67-109">**AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet은 지정 된 백업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-109">The **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="00e67-110">예제의</span><span class="sxs-lookup"><span data-stu-id="00e67-110">EXAMPLES</span></span>

### <span data-ttu-id="00e67-111">예제 1: 단일 백업 삭제</span><span class="sxs-lookup"><span data-stu-id="00e67-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="00e67-112">이름이 601061b7-d10b-46e0-bf77-a2bfb16a6add 인 백업을 삭제 합니다. 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="00e67-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="00e67-113">예제 2: 위치에 대 한 모든 백업 삭제</span><span class="sxs-lookup"><span data-stu-id="00e67-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzureRmSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="00e67-114">이 명령은 northeurope 위치에 대해 장기 보존 백업을 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="00e67-115">변수</span><span class="sxs-lookup"><span data-stu-id="00e67-115">PARAMETERS</span></span>

### <span data-ttu-id="00e67-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="00e67-116">-BackupName</span></span>
<span data-ttu-id="00e67-117">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-117">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e67-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00e67-118">-DatabaseName</span></span>
<span data-ttu-id="00e67-119">백업이 있는 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-119">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e67-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e67-120">-DefaultProfile</span></span>
<span data-ttu-id="00e67-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00e67-122">-Force</span><span class="sxs-lookup"><span data-stu-id="00e67-122">-Force</span></span>
<span data-ttu-id="00e67-123">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="00e67-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e67-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00e67-124">-InputObject</span></span>
<span data-ttu-id="00e67-125">제거할 데이터베이스 장기 보존 백업 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e67-126">-위치</span><span class="sxs-lookup"><span data-stu-id="00e67-126">-Location</span></span>
<span data-ttu-id="00e67-127">백업의 원본 서버 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-127">The location of the backups' source server.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e67-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00e67-128">-ResourceId</span></span>
<span data-ttu-id="00e67-129">제거할 데이터베이스 장기 보존 백업의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e67-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="00e67-130">-ServerName</span></span>
<span data-ttu-id="00e67-131">백업이 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-131">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e67-132">-확인</span><span class="sxs-lookup"><span data-stu-id="00e67-132">-Confirm</span></span>
<span data-ttu-id="00e67-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00e67-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00e67-134">-WhatIf</span></span>
<span data-ttu-id="00e67-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00e67-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00e67-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e67-137">CommonParameters</span></span>
<span data-ttu-id="00e67-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e67-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="00e67-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e67-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e67-140">입력</span><span class="sxs-lookup"><span data-stu-id="00e67-140">INPUTS</span></span>

### <span data-ttu-id="00e67-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00e67-141">System.String</span></span>
<span data-ttu-id="00e67-142">AzureSqlDatabaseLongTermRetentionBackupModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="00e67-142">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="00e67-143">출력</span><span class="sxs-lookup"><span data-stu-id="00e67-143">OUTPUTS</span></span>

### <span data-ttu-id="00e67-144">AzureSqlDatabaseLongTermRetentionBackupModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="00e67-144">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="00e67-145">상속자</span><span class="sxs-lookup"><span data-stu-id="00e67-145">NOTES</span></span>

## <span data-ttu-id="00e67-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00e67-146">RELATED LINKS</span></span>

[<span data-ttu-id="00e67-147">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="00e67-147">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="00e67-148">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="00e67-148">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="00e67-149">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="00e67-149">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="00e67-150">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="00e67-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
