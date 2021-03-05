---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 464334aa67be554a20c7d1b15e7d591a25979809
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974288"
---
# <span data-ttu-id="aba7c-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="aba7c-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="aba7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aba7c-102">SYNOPSIS</span></span>
<span data-ttu-id="aba7c-103">장기 보존 백업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="aba7c-104">구문</span><span class="sxs-lookup"><span data-stu-id="aba7c-104">SYNTAX</span></span>

### <span data-ttu-id="aba7c-105">위치(기본값)</span><span class="sxs-lookup"><span data-stu-id="aba7c-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba7c-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="aba7c-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba7c-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aba7c-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba7c-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="aba7c-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba7c-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="aba7c-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba7c-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="aba7c-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba7c-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="aba7c-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aba7c-112">설명</span><span class="sxs-lookup"><span data-stu-id="aba7c-112">DESCRIPTION</span></span>
<span data-ttu-id="aba7c-113">{{ 설명 }} 채우기</span><span class="sxs-lookup"><span data-stu-id="aba7c-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="aba7c-114">예제</span><span class="sxs-lookup"><span data-stu-id="aba7c-114">EXAMPLES</span></span>

### <span data-ttu-id="aba7c-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="aba7c-115">Example 1</span></span>
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

<span data-ttu-id="aba7c-116">특정 데이터베이스에 대한 모든 장기 보존 백업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="aba7c-117">리소스 그룹은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="aba7c-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aba7c-118">PARAMETERS</span></span>

### <span data-ttu-id="aba7c-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="aba7c-119">-BackupName</span></span>
<span data-ttu-id="aba7c-120">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-120">The name of the backup.</span></span>

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

### <span data-ttu-id="aba7c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aba7c-121">-DatabaseName</span></span>
<span data-ttu-id="aba7c-122">백업이 있는 Managed Database의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-122">The name of the Managed Database the backups are under.</span></span>

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

### <span data-ttu-id="aba7c-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="aba7c-123">-DatabaseState</span></span>
<span data-ttu-id="aba7c-124">찾을 백업, Alive, Deleted 또는 All을 찾은 데이터베이스의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="aba7c-125">기본값을 모두로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-125">Defaults to All</span></span>

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

### <span data-ttu-id="aba7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba7c-126">-DefaultProfile</span></span>
<span data-ttu-id="aba7c-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aba7c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aba7c-128">-InputObject</span></span>
<span data-ttu-id="aba7c-129">백업을 받을 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-129">The database object to get backups for.</span></span>

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

### <span data-ttu-id="aba7c-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="aba7c-130">-InstanceName</span></span>
<span data-ttu-id="aba7c-131">백업이 있는 Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-131">The name of the Managed Instance the backups are under.</span></span>

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

### <span data-ttu-id="aba7c-132">-Location</span><span class="sxs-lookup"><span data-stu-id="aba7c-132">-Location</span></span>
<span data-ttu-id="aba7c-133">백업의 원본 Managed Instance의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-133">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="aba7c-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="aba7c-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="aba7c-135">데이터베이스당 최신 백업만 받을지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="aba7c-136">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-136">Defaults to false.</span></span>

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

### <span data-ttu-id="aba7c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba7c-137">-ResourceGroupName</span></span>
<span data-ttu-id="aba7c-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="aba7c-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aba7c-139">-ResourceId</span></span>
<span data-ttu-id="aba7c-140">백업을 받을 데이터베이스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-140">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="aba7c-141">-확인</span><span class="sxs-lookup"><span data-stu-id="aba7c-141">-Confirm</span></span>
<span data-ttu-id="aba7c-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba7c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba7c-143">-WhatIf</span></span>
<span data-ttu-id="aba7c-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba7c-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba7c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba7c-146">CommonParameters</span></span>
<span data-ttu-id="aba7c-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aba7c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba7c-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aba7c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba7c-149">입력</span><span class="sxs-lookup"><span data-stu-id="aba7c-149">INPUTS</span></span>

### <span data-ttu-id="aba7c-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="aba7c-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="aba7c-151">System.String</span><span class="sxs-lookup"><span data-stu-id="aba7c-151">System.String</span></span>

## <span data-ttu-id="aba7c-152">출력</span><span class="sxs-lookup"><span data-stu-id="aba7c-152">OUTPUTS</span></span>

### <span data-ttu-id="aba7c-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="aba7c-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="aba7c-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aba7c-154">NOTES</span></span>

## <span data-ttu-id="aba7c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aba7c-155">RELATED LINKS</span></span>

[<span data-ttu-id="aba7c-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="aba7c-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="aba7c-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba7c-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="aba7c-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aba7c-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="aba7c-159">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="aba7c-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)