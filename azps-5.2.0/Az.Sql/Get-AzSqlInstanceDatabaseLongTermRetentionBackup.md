---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ccd716b493640afef7b5adea0b2e834c10893c3c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325779"
---
# <span data-ttu-id="a688b-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a688b-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="a688b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a688b-102">SYNOPSIS</span></span>
<span data-ttu-id="a688b-103">장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="a688b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a688b-104">SYNTAX</span></span>

### <span data-ttu-id="a688b-105">위치(기본값)</span><span class="sxs-lookup"><span data-stu-id="a688b-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a688b-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="a688b-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a688b-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a688b-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a688b-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="a688b-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a688b-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="a688b-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a688b-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="a688b-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a688b-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="a688b-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a688b-112">설명</span><span class="sxs-lookup"><span data-stu-id="a688b-112">DESCRIPTION</span></span>
<span data-ttu-id="a688b-113">{{ 설명 }}에 입력</span><span class="sxs-lookup"><span data-stu-id="a688b-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="a688b-114">예제</span><span class="sxs-lookup"><span data-stu-id="a688b-114">EXAMPLES</span></span>

### <span data-ttu-id="a688b-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="a688b-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="a688b-116">특정 데이터베이스에 대한 모든 장기 보존 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="a688b-117">리소스 그룹은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="a688b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a688b-118">PARAMETERS</span></span>

### <span data-ttu-id="a688b-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="a688b-119">-BackupName</span></span>
<span data-ttu-id="a688b-120">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a688b-121">-DatabaseName</span></span>
<span data-ttu-id="a688b-122">백업이 있는 관리되는 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="a688b-123">-DatabaseState</span></span>
<span data-ttu-id="a688b-124">백업을 찾거나, 연결하거나, 삭제하거나, 모두를 찾은 데이터베이스의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="a688b-125">기본값은 모두</span><span class="sxs-lookup"><span data-stu-id="a688b-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a688b-126">-DefaultProfile</span></span>
<span data-ttu-id="a688b-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a688b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a688b-128">-InputObject</span></span>
<span data-ttu-id="a688b-129">백업을 받을 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a688b-130">-InstanceName</span></span>
<span data-ttu-id="a688b-131">백업이 있는 Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-132">-Location</span><span class="sxs-lookup"><span data-stu-id="a688b-132">-Location</span></span>
<span data-ttu-id="a688b-133">백업의 원본 Managed Instance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="a688b-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="a688b-135">데이터베이스당 최신 백업만 받을지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="a688b-136">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a688b-137">-ResourceGroupName</span></span>
<span data-ttu-id="a688b-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a688b-139">-ResourceId</span></span>
<span data-ttu-id="a688b-140">백업을 받을 데이터베이스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a688b-141">-Confirm</span></span>
<span data-ttu-id="a688b-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a688b-143">-WhatIf</span></span>
<span data-ttu-id="a688b-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a688b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a688b-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a688b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a688b-146">CommonParameters</span></span>
<span data-ttu-id="a688b-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a688b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a688b-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a688b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a688b-149">입력</span><span class="sxs-lookup"><span data-stu-id="a688b-149">INPUTS</span></span>

### <span data-ttu-id="a688b-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a688b-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="a688b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a688b-151">System.String</span></span>

## <span data-ttu-id="a688b-152">출력</span><span class="sxs-lookup"><span data-stu-id="a688b-152">OUTPUTS</span></span>

### <span data-ttu-id="a688b-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="a688b-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="a688b-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a688b-154">NOTES</span></span>

## <span data-ttu-id="a688b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a688b-155">RELATED LINKS</span></span>

[<span data-ttu-id="a688b-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a688b-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="a688b-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a688b-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="a688b-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a688b-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="a688b-159">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a688b-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)