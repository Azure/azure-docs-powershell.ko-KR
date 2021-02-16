---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176740"
---
# <span data-ttu-id="624c7-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="624c7-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="624c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="624c7-102">SYNOPSIS</span></span>
<span data-ttu-id="624c7-103">백업 단기 보존 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="624c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="624c7-104">SYNTAX</span></span>

### <span data-ttu-id="624c7-105">PolicyByResourceInstanceDatabaseSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="624c7-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="624c7-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="624c7-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="624c7-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="624c7-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="624c7-108">설명</span><span class="sxs-lookup"><span data-stu-id="624c7-108">DESCRIPTION</span></span>
<span data-ttu-id="624c7-109">**Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet은 이 데이터베이스에 등록된 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="624c7-110">정책은 지정 시간 복원 백업의 보존 기간(일)입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="624c7-111">예제</span><span class="sxs-lookup"><span data-stu-id="624c7-111">EXAMPLES</span></span>

### <span data-ttu-id="624c7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="624c7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="624c7-113">이 명령은 database01에 대한 단기 보존 정책을 35일로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="624c7-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="624c7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="624c7-115">이 명령은 데이터베이스 개체의 파이핑을 통해 database01에 대한 단기 보존 정책을 35일로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="624c7-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="624c7-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="624c7-117">이 명령은 삭제된 데이터베이스 개체의 파이핑을 통해 DB1이라는 모든 삭제된 데이터베이스에 대한 단기 보존 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="624c7-118">삭제된 데이터베이스에 대한 보존 기간만 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="624c7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="624c7-119">PARAMETERS</span></span>

### <span data-ttu-id="624c7-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="624c7-120">-DatabaseName</span></span>
<span data-ttu-id="624c7-121">백업을 검색할 Azure SQL Instance 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="624c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="624c7-122">-DefaultProfile</span></span>
<span data-ttu-id="624c7-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="624c7-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="624c7-124">-DeletionDate</span></span>
<span data-ttu-id="624c7-125">밀리초 정밀도(예: 2016-02-23T00:21:22.847Z)를 사용하여 백업을 검색할 Azure SQL Instance Database의 지운 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="624c7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="624c7-126">-InputObject</span></span>
<span data-ttu-id="624c7-127">정책을 얻거나 설정할 라이브 또는 삭제된 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="624c7-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="624c7-128">-InstanceName</span></span>
<span data-ttu-id="624c7-129">데이터베이스가 있는 Azure SQL Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="624c7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="624c7-130">-ResourceGroupName</span></span>
<span data-ttu-id="624c7-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="624c7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="624c7-132">-ResourceId</span></span>
<span data-ttu-id="624c7-133">단기 보존 정책 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="624c7-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="624c7-134">-RetentionDays</span></span>
<span data-ttu-id="624c7-135">백업 보존 일수입니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="624c7-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="624c7-136">-Confirm</span></span>
<span data-ttu-id="624c7-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="624c7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="624c7-138">-WhatIf</span></span>
<span data-ttu-id="624c7-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="624c7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="624c7-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="624c7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="624c7-141">CommonParameters</span></span>
<span data-ttu-id="624c7-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="624c7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="624c7-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="624c7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="624c7-144">입력</span><span class="sxs-lookup"><span data-stu-id="624c7-144">INPUTS</span></span>

### <span data-ttu-id="624c7-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="624c7-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="624c7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="624c7-146">System.String</span></span>

## <span data-ttu-id="624c7-147">출력</span><span class="sxs-lookup"><span data-stu-id="624c7-147">OUTPUTS</span></span>

### <span data-ttu-id="624c7-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="624c7-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="624c7-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="624c7-149">NOTES</span></span>

## <span data-ttu-id="624c7-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="624c7-150">RELATED LINKS</span></span>
