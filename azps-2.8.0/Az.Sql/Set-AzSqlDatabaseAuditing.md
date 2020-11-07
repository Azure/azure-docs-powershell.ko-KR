---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: f8a31171309a9c869d29078ff09ce8903288e8bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873553"
---
# <span data-ttu-id="e6b68-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="e6b68-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="e6b68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b68-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b68-103">**중요:이 cmdlet은 더 이상 사용 되지 않으며, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) 에서 바꿉니다.**</span><span class="sxs-lookup"><span data-stu-id="e6b68-103">**Important: This cmdlet is deprecated, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="e6b68-104">Azure SQL 데이터베이스에 대 한 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-104">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="e6b68-105">구문과</span><span class="sxs-lookup"><span data-stu-id="e6b68-105">SYNTAX</span></span>

### <span data-ttu-id="e6b68-106">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e6b68-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b68-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="e6b68-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b68-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="e6b68-108">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b68-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="e6b68-109">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b68-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="e6b68-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b68-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="e6b68-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6b68-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="e6b68-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6b68-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="e6b68-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6b68-114">설명은</span><span class="sxs-lookup"><span data-stu-id="e6b68-114">DESCRIPTION</span></span>
<span data-ttu-id="e6b68-115">**AzSqlDatabaseAuditing** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-115">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="e6b68-116">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-116">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e6b68-117">감사 로그 대상은 BlobStorage, LogAnalytics 또는 EventHub (지정 하지 않은 경우 기본적으로 BlobStorage)와 같은 스위치 매개 변수 중 하나를 지정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="e6b68-118">*State* 매개 변수를 사용 하 여 정책을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="e6b68-119">감사 로그 대상이 blob storage 인 경우, 저장소 키를 정의 하는 감사 로그 및 *Storageaccountname* 매개 변수에 대 한 저장소 계정을 결정 하는 *storageaccountname* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="e6b68-120">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="e6b68-121">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 데이터베이스 식별자 외에도 현재 감사 설정을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="e6b68-122">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-122">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="e6b68-123">예제의</span><span class="sxs-lookup"><span data-stu-id="e6b68-123">EXAMPLES</span></span>

### <span data-ttu-id="e6b68-124">예제 1: Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e6b68-124">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="e6b68-125">예제 2: Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e6b68-125">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="e6b68-126">예제 3: 다른 구독의 저장소 계정을 사용 하 여 Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e6b68-126">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="e6b68-127">예제 4: T-SQL 조건자를 사용 하 여 고급 필터링이 포함 된 Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e6b68-127">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="e6b68-128">예제 5: Azure SQL 데이터베이스의 blob 저장소 감사 정책에서 고급 필터링 설정 제거</span><span class="sxs-lookup"><span data-stu-id="e6b68-128">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="e6b68-129">예제 6: Azure SQL 데이터베이스의 이벤트 허브 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e6b68-129">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="e6b68-130">예제 7: Azure SQL 데이터베이스의 이벤트 허브 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e6b68-130">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="e6b68-131">예제 8: Azure SQL 데이터베이스의 log analytics 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e6b68-131">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="e6b68-132">예제 9: Azure SQL 데이터베이스의 log analytics 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e6b68-132">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="e6b68-133">예제 10: Azure SQL 데이터베이스의 log analytics 감사 정책을 통해 파이프라인 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e6b68-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="e6b68-134">변수</span><span class="sxs-lookup"><span data-stu-id="e6b68-134">PARAMETERS</span></span>

### <span data-ttu-id="e6b68-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6b68-135">-AsJob</span></span>
<span data-ttu-id="e6b68-136">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e6b68-136">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-137">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="e6b68-137">-AuditAction</span></span>
<span data-ttu-id="e6b68-138">감사 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-138">The set of audit actions.</span></span>  
<span data-ttu-id="e6b68-139">감사에 지원 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-139">The supported actions to audit are:</span></span>  
<span data-ttu-id="e6b68-140">클릭</span><span class="sxs-lookup"><span data-stu-id="e6b68-140">SELECT</span></span>  
<span data-ttu-id="e6b68-141">UPDATE</span><span class="sxs-lookup"><span data-stu-id="e6b68-141">UPDATE</span></span>  
<span data-ttu-id="e6b68-142">넣으십시오</span><span class="sxs-lookup"><span data-stu-id="e6b68-142">INSERT</span></span>  
<span data-ttu-id="e6b68-143">삭제</span><span class="sxs-lookup"><span data-stu-id="e6b68-143">DELETE</span></span>  
<span data-ttu-id="e6b68-144">세기</span><span class="sxs-lookup"><span data-stu-id="e6b68-144">EXECUTE</span></span>  
<span data-ttu-id="e6b68-145">받기</span><span class="sxs-lookup"><span data-stu-id="e6b68-145">RECEIVE</span></span>  
<span data-ttu-id="e6b68-146">감사할 작업을 정의 하는 일반적인 형태의 참조: [principal]에 따라 [개체]의 [개체]는 테이블, 뷰 또는 저장 프로시저와 같은 개체 또는 전체 데이터베이스 또는 스키마를 참조할 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6b68-146">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="e6b68-147">두 번째 경우에는 forms 데이터베이스:: [dbname] 및 SCHEMA:: [schemaname]이 각각 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-147">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="e6b68-148">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e6b68-148">For example:</span></span>  
<span data-ttu-id="e6b68-149">공용에서 dbo myTable 선택</span><span class="sxs-lookup"><span data-stu-id="e6b68-149">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="e6b68-150">Public을 기준으로 데이터베이스:: myDatabase 선택</span><span class="sxs-lookup"><span data-stu-id="e6b68-150">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="e6b68-151">SCHEMA:: mySchema을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-151">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="e6b68-152">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6b68-152">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="e6b68-153">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="e6b68-153">-AuditActionGroup</span></span>
<span data-ttu-id="e6b68-154">사용할 권장 되는 작업 그룹 집합은 다음 조합입니다 .이는 데이터베이스에 대해 실행 되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패 한 로그인을 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-154">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="e6b68-155">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="e6b68-155">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="e6b68-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="e6b68-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="e6b68-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="e6b68-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="e6b68-158">위의 조합은 기본적으로 구성 되는 집합 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-158">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="e6b68-159">이러한 그룹은 데이터베이스에 대해 실행 되는 모든 SQL 문과 저장 프로시저를 다루며, 다른 그룹과 함께 사용 하면 중복 감사 로그가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-159">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="e6b68-160">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6b68-160">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-161">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="e6b68-161">-BlobStorage</span></span>
<span data-ttu-id="e6b68-162">감사 로그 대상이 blob storage 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-162">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-163">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6b68-163">-DatabaseName</span></span>
<span data-ttu-id="e6b68-164">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-164">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b68-165">-DefaultProfile</span></span>
<span data-ttu-id="e6b68-166">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-166">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b68-167">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e6b68-167">-EventHub</span></span>
<span data-ttu-id="e6b68-168">감사 로그 대상이 이벤트 허브 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-168">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-169">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b68-169">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="e6b68-170">이벤트 허브 권한 부여 규칙의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="e6b68-170">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-171">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="e6b68-171">-EventHubName</span></span>
<span data-ttu-id="e6b68-172">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-172">The name of the event hub.</span></span> <span data-ttu-id="e6b68-173">EventHubAuthorizationRuleResourceId를 제공할 때 아무것도 지정 하지 않으면 기본 이벤트 허브가 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-173">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-174">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6b68-174">-InputObject</span></span>
<span data-ttu-id="e6b68-175">감사 정책을 관리 하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-175">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-176">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="e6b68-176">-LogAnalytics</span></span>
<span data-ttu-id="e6b68-177">감사 로그 대상이 로그 분석 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-177">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-178">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6b68-178">-PassThru</span></span>
<span data-ttu-id="e6b68-179">Cmdlet 실행이 종료 될 때 감사 정책을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-179">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-180">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="e6b68-180">-PredicateExpression</span></span>
<span data-ttu-id="e6b68-181">감사 로그를 필터링 하는 데 사용 되는 T-SQL 조건자 (WHERE 절)</span><span class="sxs-lookup"><span data-stu-id="e6b68-181">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="e6b68-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b68-182">-ResourceGroupName</span></span>
<span data-ttu-id="e6b68-183">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-183">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-184">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="e6b68-184">-RetentionInDays</span></span>
<span data-ttu-id="e6b68-185">감사 로그 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-185">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-186">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6b68-186">-ServerName</span></span>
<span data-ttu-id="e6b68-187">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-187">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-188">-상태</span><span class="sxs-lookup"><span data-stu-id="e6b68-188">-State</span></span>
<span data-ttu-id="e6b68-189">정책의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-189">The state of the policy.</span></span>

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

### <span data-ttu-id="e6b68-190">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e6b68-190">-StorageAccountName</span></span>
<span data-ttu-id="e6b68-191">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-191">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-192">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6b68-192">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="e6b68-193">저장소 계정 구독 id</span><span class="sxs-lookup"><span data-stu-id="e6b68-193">The storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-194">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="e6b68-194">-StorageKeyType</span></span>
<span data-ttu-id="e6b68-195">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-195">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-196">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b68-196">-WorkspaceResourceId</span></span>
<span data-ttu-id="e6b68-197">감사 로그를 보낼 로그 분석 작업 영역에 대 한 작업 영역 ID (로그 분석 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-197">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="e6b68-198">예:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="e6b68-198">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b68-199">-확인</span><span class="sxs-lookup"><span data-stu-id="e6b68-199">-Confirm</span></span>
<span data-ttu-id="e6b68-200">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6b68-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6b68-201">-WhatIf</span></span>
<span data-ttu-id="e6b68-202">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6b68-203">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6b68-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b68-204">CommonParameters</span></span>
<span data-ttu-id="e6b68-205">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6b68-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b68-206">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6b68-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b68-207">입력</span><span class="sxs-lookup"><span data-stu-id="e6b68-207">INPUTS</span></span>

### <span data-ttu-id="e6b68-208">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6b68-208">System.String</span></span>

### <span data-ttu-id="e6b68-209">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="e6b68-209">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="e6b68-210">Microsoft. Test.sql. 감사. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="e6b68-210">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="e6b68-211">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e6b68-211">System.String[]</span></span>

### <span data-ttu-id="e6b68-212">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e6b68-212">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e6b68-213">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="e6b68-213">System.Guid</span></span>

### <span data-ttu-id="e6b68-214">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e6b68-214">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e6b68-215">출력</span><span class="sxs-lookup"><span data-stu-id="e6b68-215">OUTPUTS</span></span>

### <span data-ttu-id="e6b68-216">Microsoft. .Sql. 감사. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="e6b68-216">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="e6b68-217">상속자</span><span class="sxs-lookup"><span data-stu-id="e6b68-217">NOTES</span></span>

## <span data-ttu-id="e6b68-218">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6b68-218">RELATED LINKS</span></span>
