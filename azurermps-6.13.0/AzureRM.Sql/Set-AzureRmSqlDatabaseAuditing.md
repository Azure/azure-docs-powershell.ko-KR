---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527783"
---
# <span data-ttu-id="0e0b6-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="0e0b6-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="0e0b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e0b6-102">SYNOPSIS</span></span>
<span data-ttu-id="0e0b6-103">Azure SQL 데이터베이스에 대 한 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e0b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e0b6-104">SYNTAX</span></span>

### <span data-ttu-id="0e0b6-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e0b6-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e0b6-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="0e0b6-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e0b6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0e0b6-107">DESCRIPTION</span></span>
<span data-ttu-id="0e0b6-108">**AzureRmSqlDatabaseAuditing** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="0e0b6-109">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0e0b6-110">저장소 키를 정의 하는 감사 로그 및 *Storageaccountname* 매개 변수에 대 한 저장소 계정을 지정 하는 *storageaccountname* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="0e0b6-111">*State* 매개 변수를 사용 하 여 정책을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="0e0b6-112">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="0e0b6-113">Cmdlet이 성공적으로 실행 되 면 데이터베이스 감사를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="0e0b6-114">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 데이터베이스 식별자 외에도 현재 blob 감사 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="0e0b6-115">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="0e0b6-116">예제의</span><span class="sxs-lookup"><span data-stu-id="0e0b6-116">EXAMPLES</span></span>

### <span data-ttu-id="0e0b6-117">예제 1: Azure SQL 데이터베이스의 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="0e0b6-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="0e0b6-118">예제 2: Azure SQL 데이터베이스의 blob 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="0e0b6-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="0e0b6-119">예제 3: 다른 구독의 저장소 계정을 사용 하 여 Azure SQL 데이터베이스의 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="0e0b6-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="0e0b6-120">예제 4: Azure SQL 데이터베이스의 확장 된 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="0e0b6-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="0e0b6-121">예제 5: Azure SQL 데이터베이스의 확장 된 감사 정책을 제거 하 고이를 대신 하 여 감사 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="0e0b6-122">변수</span><span class="sxs-lookup"><span data-stu-id="0e0b6-122">PARAMETERS</span></span>

### <span data-ttu-id="0e0b6-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="0e0b6-123">-AuditAction</span></span>
<span data-ttu-id="0e0b6-124">감사 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-124">The set of audit actions.</span></span>
<span data-ttu-id="0e0b6-125">감사에 대해 수행할 수 있는 작업은 다음과 같습니다. 업데이트 삽입을 선택 합니다. [principal]에 따라 [개체]에 대해 [동작]이 표시 됩니다. 위의 형식에서 [개체]는 테이블, 뷰 또는 저장 프로시저 또는 전체 데이터베이스 또는 스키마와 같은 개체를 참조할 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="0e0b6-126">두 번째 경우에는 forms 데이터베이스:: [dbname] 및 SCHEMA:: [schemaname]이 각각 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="0e0b6-127">예를 들어 다음을 수행 합니다. 공용에서 데이터베이스에서 선택:: \에 공용 선택 합니다. 스키마:: mySchema에서 다음을 수행 합니다. 자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="0e0b6-128">-AuditActionGroup</span></span>
<span data-ttu-id="0e0b6-129">사용할 수 있는 권장 작업 그룹 집합은 다음과 같은 조합입니다 .이는 데이터베이스에 대해 실행 되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 ("BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP")을 감사 하며 위의 조합은 기본적으로 구성 된 집합 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="0e0b6-130">이러한 그룹은 데이터베이스에 대해 실행 되는 모든 SQL 문과 저장 프로시저를 다루며, 다른 그룹과 함께 사용 하면 중복 감사 로그가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="0e0b6-131">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0e0b6-132">-DatabaseName</span></span>
<span data-ttu-id="0e0b6-133">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-133">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0b6-134">-DefaultProfile</span></span>
<span data-ttu-id="0e0b6-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e0b6-136">-PassThru</span></span>
<span data-ttu-id="0e0b6-137">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="0e0b6-137">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0e0b6-138">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="0e0b6-138">-PredicateExpression</span></span>
<span data-ttu-id="0e0b6-139">감사 로그를 필터링 하는 데 사용 되는 Where 절의 문입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-139">The statement of the Where Clause used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e0b6-140">-ResourceGroupName</span></span>
<span data-ttu-id="0e0b6-141">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-142">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="0e0b6-142">-RetentionInDays</span></span>
<span data-ttu-id="0e0b6-143">감사 로그 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-143">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e0b6-144">-ServerName</span></span>
<span data-ttu-id="0e0b6-145">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-145">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-146">-상태</span><span class="sxs-lookup"><span data-stu-id="0e0b6-146">-State</span></span>
<span data-ttu-id="0e0b6-147">정책의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-147">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0e0b6-148">-StorageAccountName</span></span>
<span data-ttu-id="0e0b6-149">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-149">The name of the storage account.</span></span> <span data-ttu-id="0e0b6-150">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="0e0b6-151">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-151">This parameter is not required.</span></span>
<span data-ttu-id="0e0b6-152">이 매개 변수를 지정 하지 않으면 이전에 감사 정책의 일부로 정의한 저장소 계정이 cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="0e0b6-153">감사 정책이 처음 정의 될 때이 매개 변수를 지정 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e0b6-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="0e0b6-155">저장소 계정 구독 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="0e0b6-156">-StorageKeyType</span></span>
<span data-ttu-id="0e0b6-157">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-157">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e0b6-158">-확인</span><span class="sxs-lookup"><span data-stu-id="0e0b6-158">-Confirm</span></span>
<span data-ttu-id="0e0b6-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e0b6-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e0b6-160">-WhatIf</span></span>
<span data-ttu-id="0e0b6-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e0b6-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e0b6-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0b6-163">CommonParameters</span></span>
<span data-ttu-id="0e0b6-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e0b6-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0b6-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e0b6-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0b6-166">입력</span><span class="sxs-lookup"><span data-stu-id="0e0b6-166">INPUTS</span></span>

## <span data-ttu-id="0e0b6-167">출력</span><span class="sxs-lookup"><span data-stu-id="0e0b6-167">OUTPUTS</span></span>

## <span data-ttu-id="0e0b6-168">상속자</span><span class="sxs-lookup"><span data-stu-id="0e0b6-168">NOTES</span></span>

## <span data-ttu-id="0e0b6-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e0b6-169">RELATED LINKS</span></span>
