---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 9408e51cfcdab3cd2c82617ee7f8cb9bc7d3918a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044276"
---
# <span data-ttu-id="01a46-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="01a46-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="01a46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01a46-102">SYNOPSIS</span></span>
<span data-ttu-id="01a46-103">장기간 보존 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="01a46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01a46-104">SYNTAX</span></span>

### <span data-ttu-id="01a46-105">위치 (기본값)</span><span class="sxs-lookup"><span data-stu-id="01a46-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a46-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="01a46-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a46-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01a46-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a46-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="01a46-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a46-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="01a46-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a46-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="01a46-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a46-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="01a46-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01a46-112">설명은</span><span class="sxs-lookup"><span data-stu-id="01a46-112">DESCRIPTION</span></span>
<span data-ttu-id="01a46-113">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="01a46-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="01a46-114">예제의</span><span class="sxs-lookup"><span data-stu-id="01a46-114">EXAMPLES</span></span>

### <span data-ttu-id="01a46-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="01a46-115">Example 1</span></span>
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

<span data-ttu-id="01a46-116">특정 데이터베이스에 대해 장기 보존 백업을 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="01a46-117">리소스 그룹은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="01a46-118">변수</span><span class="sxs-lookup"><span data-stu-id="01a46-118">PARAMETERS</span></span>

### <span data-ttu-id="01a46-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="01a46-119">-BackupName</span></span>
<span data-ttu-id="01a46-120">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-120">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01a46-121">-DatabaseName</span></span>
<span data-ttu-id="01a46-122">백업이 있는 관리 되는 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="01a46-123">-DatabaseState</span></span>
<span data-ttu-id="01a46-124">백업을 검색, 활성화, 삭제 또는 모두 사용할 데이터베이스의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="01a46-125">기본적으로 모두</span><span class="sxs-lookup"><span data-stu-id="01a46-125">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a46-126">-DefaultProfile</span></span>
<span data-ttu-id="01a46-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01a46-128">-InputObject</span></span>
<span data-ttu-id="01a46-129">백업을 가져올 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-129">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="01a46-130">-InstanceName</span></span>
<span data-ttu-id="01a46-131">백업이 있는 관리 되는 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-132">-위치</span><span class="sxs-lookup"><span data-stu-id="01a46-132">-Location</span></span>
<span data-ttu-id="01a46-133">백업의 원본 관리 인스턴스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="01a46-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="01a46-135">데이터베이스당 최신 백업만 받을지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="01a46-136">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-136">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a46-137">-ResourceGroupName</span></span>
<span data-ttu-id="01a46-138">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-138">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01a46-139">-ResourceId</span></span>
<span data-ttu-id="01a46-140">백업을 가져올 데이터베이스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-141">-확인</span><span class="sxs-lookup"><span data-stu-id="01a46-141">-Confirm</span></span>
<span data-ttu-id="01a46-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01a46-143">-WhatIf</span></span>
<span data-ttu-id="01a46-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01a46-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a46-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a46-146">CommonParameters</span></span>
<span data-ttu-id="01a46-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01a46-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a46-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="01a46-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a46-149">입력</span><span class="sxs-lookup"><span data-stu-id="01a46-149">INPUTS</span></span>

### <span data-ttu-id="01a46-150">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="01a46-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="01a46-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01a46-151">System.String</span></span>

## <span data-ttu-id="01a46-152">출력</span><span class="sxs-lookup"><span data-stu-id="01a46-152">OUTPUTS</span></span>

### <span data-ttu-id="01a46-153">AzureSqlManagedDatabaseLongTermRetentionBackupModel (\*). m. ManagedDatabaseBackup.</span><span class="sxs-lookup"><span data-stu-id="01a46-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="01a46-154">상속자</span><span class="sxs-lookup"><span data-stu-id="01a46-154">NOTES</span></span>

## <span data-ttu-id="01a46-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01a46-155">RELATED LINKS</span></span>

[<span data-ttu-id="01a46-156">제거-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="01a46-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="01a46-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="01a46-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="01a46-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="01a46-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="01a46-159">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="01a46-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)