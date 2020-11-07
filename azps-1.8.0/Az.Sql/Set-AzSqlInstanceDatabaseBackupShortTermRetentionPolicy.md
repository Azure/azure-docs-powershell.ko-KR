---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 6ec4e3163d1bcd388ef0b4b8813ece89a41bfd23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698771"
---
# <span data-ttu-id="bb373-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bb373-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="bb373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb373-102">SYNOPSIS</span></span>
<span data-ttu-id="bb373-103">단기 백업 기간 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="bb373-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb373-104">SYNTAX</span></span>

### <span data-ttu-id="bb373-105">PolicyByResourceInstanceDatabaseSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bb373-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb373-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb373-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb373-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bb373-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb373-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bb373-108">DESCRIPTION</span></span>
<span data-ttu-id="bb373-109">**AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet은이 데이터베이스에 등록 된 단기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="bb373-110">정책은 시간 지정 복원 백업의 보존 기간을 일 수로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="bb373-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bb373-111">EXAMPLES</span></span>

### <span data-ttu-id="bb373-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb373-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="bb373-113">이 명령은 database01에 대 한 단기 보존 정책을 35 days로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="bb373-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="bb373-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="bb373-115">이 명령은 데이터베이스 개체에서 파이핑을 통해 database01에 대 한 단기 보존 정책을 35 일 수로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="bb373-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="bb373-116">Example 3</span></span>
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

<span data-ttu-id="bb373-117">이 명령은 deleted 데이터베이스 개체에서 파이핑을 통해 DB1 라는 모든 삭제 된 데이터베이스에 대 한 단기 보존 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="bb373-118">참고 삭제 된 데이터베이스의 보존 기간만 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="bb373-119">변수</span><span class="sxs-lookup"><span data-stu-id="bb373-119">PARAMETERS</span></span>

### <span data-ttu-id="bb373-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb373-120">-DatabaseName</span></span>
<span data-ttu-id="bb373-121">백업을 검색할 Azure SQL 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="bb373-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb373-122">-DefaultProfile</span></span>
<span data-ttu-id="bb373-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb373-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="bb373-124">-DeletionDate</span></span>
<span data-ttu-id="bb373-125">백업을 검색할 Azure SQL 인스턴스 데이터베이스의 삭제 날짜입니다 (예: 2016-02-23T00:21:22.847 Z).</span><span class="sxs-lookup"><span data-stu-id="bb373-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="bb373-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb373-126">-InputObject</span></span>
<span data-ttu-id="bb373-127">정책을 가져오거나 설정 하는 데 사용할 라이브 또는 삭제 된 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-127">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="bb373-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bb373-128">-InstanceName</span></span>
<span data-ttu-id="bb373-129">데이터베이스가 있는 Azure SQL 관리 되는 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="bb373-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb373-130">-ResourceGroupName</span></span>
<span data-ttu-id="bb373-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb373-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb373-132">-ResourceId</span></span>
<span data-ttu-id="bb373-133">단기 보존 정책 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-133">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="bb373-134">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="bb373-134">-RetentionDays</span></span>
<span data-ttu-id="bb373-135">백업 보존 일 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="bb373-136">-확인</span><span class="sxs-lookup"><span data-stu-id="bb373-136">-Confirm</span></span>
<span data-ttu-id="bb373-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb373-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb373-138">-WhatIf</span></span>
<span data-ttu-id="bb373-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb373-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb373-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb373-141">CommonParameters</span></span>
<span data-ttu-id="bb373-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb373-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb373-143">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb373-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb373-144">입력</span><span class="sxs-lookup"><span data-stu-id="bb373-144">INPUTS</span></span>

### <span data-ttu-id="bb373-145">AzureSqlManagedDatabaseBaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="bb373-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="bb373-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb373-146">System.String</span></span>

## <span data-ttu-id="bb373-147">출력</span><span class="sxs-lookup"><span data-stu-id="bb373-147">OUTPUTS</span></span>

### <span data-ttu-id="bb373-148">AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel (\*). m. ManagedDatabaseBackup.</span><span class="sxs-lookup"><span data-stu-id="bb373-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="bb373-149">상속자</span><span class="sxs-lookup"><span data-stu-id="bb373-149">NOTES</span></span>

## <span data-ttu-id="bb373-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb373-150">RELATED LINKS</span></span>