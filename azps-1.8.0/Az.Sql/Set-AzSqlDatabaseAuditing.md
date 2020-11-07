---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 511207be4094dae96f8d138124021ce2f8ed3913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698803"
---
# <span data-ttu-id="2daa7-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="2daa7-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="2daa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2daa7-102">SYNOPSIS</span></span>
<span data-ttu-id="2daa7-103">Azure SQL 데이터베이스에 대 한 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="2daa7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2daa7-104">SYNTAX</span></span>

### <span data-ttu-id="2daa7-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2daa7-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2daa7-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="2daa7-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2daa7-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="2daa7-107">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2daa7-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="2daa7-108">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2daa7-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="2daa7-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2daa7-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="2daa7-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2daa7-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="2daa7-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2daa7-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="2daa7-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2daa7-113">설명은</span><span class="sxs-lookup"><span data-stu-id="2daa7-113">DESCRIPTION</span></span>
<span data-ttu-id="2daa7-114">**AzSqlDatabaseAuditing** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-114">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="2daa7-115">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-115">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="2daa7-116">감사 로그 대상은 BlobStorage, LogAnalytics 또는 EventHub (지정 하지 않은 경우 기본적으로 BlobStorage)와 같은 스위치 매개 변수 중 하나를 지정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="2daa7-117">*State* 매개 변수를 사용 하 여 정책을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="2daa7-118">감사 로그 대상이 blob storage 인 경우, 저장소 키를 정의 하는 감사 로그 및 *Storageaccountname* 매개 변수에 대 한 저장소 계정을 결정 하는 *storageaccountname* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="2daa7-119">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="2daa7-120">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 데이터베이스 식별자 외에도 현재 감사 설정을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="2daa7-121">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-121">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="2daa7-122">예제의</span><span class="sxs-lookup"><span data-stu-id="2daa7-122">EXAMPLES</span></span>

### <span data-ttu-id="2daa7-123">예제 1: Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="2daa7-123">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="2daa7-124">예제 2: Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2daa7-124">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="2daa7-125">예제 3: 다른 구독의 저장소 계정을 사용 하 여 Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="2daa7-125">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="2daa7-126">예제 4: T-SQL 조건자를 사용 하 여 고급 필터링이 포함 된 Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="2daa7-126">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="2daa7-127">예제 5: Azure SQL 데이터베이스의 blob 저장소 감사 정책에서 고급 필터링 설정 제거</span><span class="sxs-lookup"><span data-stu-id="2daa7-127">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="2daa7-128">예제 6: Azure SQL 데이터베이스의 이벤트 허브 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="2daa7-128">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="2daa7-129">예제 7: Azure SQL 데이터베이스의 이벤트 허브 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2daa7-129">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="2daa7-130">예제 8: Azure SQL 데이터베이스의 log analytics 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="2daa7-130">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="2daa7-131">예제 9: Azure SQL 데이터베이스의 log analytics 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2daa7-131">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="2daa7-132">예제 10: Azure SQL 데이터베이스의 log analytics 감사 정책을 통해 파이프라인 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2daa7-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="2daa7-133">변수</span><span class="sxs-lookup"><span data-stu-id="2daa7-133">PARAMETERS</span></span>

### <span data-ttu-id="2daa7-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2daa7-134">-AsJob</span></span>
<span data-ttu-id="2daa7-135">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2daa7-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2daa7-136">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="2daa7-136">-AuditAction</span></span>
<span data-ttu-id="2daa7-137">감사 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-137">The set of audit actions.</span></span>  
<span data-ttu-id="2daa7-138">감사에 지원 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-138">The supported actions to audit are:</span></span>  
<span data-ttu-id="2daa7-139">클릭</span><span class="sxs-lookup"><span data-stu-id="2daa7-139">SELECT</span></span>  
<span data-ttu-id="2daa7-140">UPDATE</span><span class="sxs-lookup"><span data-stu-id="2daa7-140">UPDATE</span></span>  
<span data-ttu-id="2daa7-141">넣으십시오</span><span class="sxs-lookup"><span data-stu-id="2daa7-141">INSERT</span></span>  
<span data-ttu-id="2daa7-142">삭제</span><span class="sxs-lookup"><span data-stu-id="2daa7-142">DELETE</span></span>  
<span data-ttu-id="2daa7-143">세기</span><span class="sxs-lookup"><span data-stu-id="2daa7-143">EXECUTE</span></span>  
<span data-ttu-id="2daa7-144">받기</span><span class="sxs-lookup"><span data-stu-id="2daa7-144">RECEIVE</span></span>  
<span data-ttu-id="2daa7-145">감사할 작업을 정의 하는 일반적인 형태의 참조: [principal]에 따라 [개체]의 [개체]는 테이블, 뷰 또는 저장 프로시저와 같은 개체 또는 전체 데이터베이스 또는 스키마를 참조할 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="2daa7-145">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="2daa7-146">두 번째 경우에는 forms 데이터베이스:: [dbname] 및 SCHEMA:: [schemaname]이 각각 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-146">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="2daa7-147">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="2daa7-147">For example:</span></span>  
<span data-ttu-id="2daa7-148">공용에서 dbo myTable 선택</span><span class="sxs-lookup"><span data-stu-id="2daa7-148">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="2daa7-149">Public을 기준으로 데이터베이스:: myDatabase 선택</span><span class="sxs-lookup"><span data-stu-id="2daa7-149">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="2daa7-150">SCHEMA:: mySchema을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-150">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="2daa7-151">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 하세요.</span><span class="sxs-lookup"><span data-stu-id="2daa7-151">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="2daa7-152">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="2daa7-152">-AuditActionGroup</span></span>
<span data-ttu-id="2daa7-153">사용할 권장 되는 작업 그룹 집합은 다음 조합입니다 .이는 데이터베이스에 대해 실행 되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패 한 로그인을 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-153">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="2daa7-154">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="2daa7-154">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="2daa7-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="2daa7-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="2daa7-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="2daa7-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="2daa7-157">위의 조합은 기본적으로 구성 되는 집합 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-157">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="2daa7-158">이러한 그룹은 데이터베이스에 대해 실행 되는 모든 SQL 문과 저장 프로시저를 다루며, 다른 그룹과 함께 사용 하면 중복 감사 로그가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-158">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="2daa7-159">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 하세요.</span><span class="sxs-lookup"><span data-stu-id="2daa7-159">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="2daa7-160">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="2daa7-160">-BlobStorage</span></span>
<span data-ttu-id="2daa7-161">감사 로그 대상이 blob storage 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-161">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="2daa7-162">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2daa7-162">-DatabaseName</span></span>
<span data-ttu-id="2daa7-163">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-163">SQL Database name.</span></span>

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

### <span data-ttu-id="2daa7-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2daa7-164">-DefaultProfile</span></span>
<span data-ttu-id="2daa7-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2daa7-166">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2daa7-166">-EventHub</span></span>
<span data-ttu-id="2daa7-167">감사 로그 대상이 이벤트 허브 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-167">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="2daa7-168">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="2daa7-168">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="2daa7-169">이벤트 허브 권한 부여 규칙의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="2daa7-169">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="2daa7-170">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="2daa7-170">-EventHubName</span></span>
<span data-ttu-id="2daa7-171">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-171">The name of the event hub.</span></span> <span data-ttu-id="2daa7-172">EventHubAuthorizationRuleResourceId를 제공할 때 아무것도 지정 하지 않으면 기본 이벤트 허브가 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-172">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="2daa7-173">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2daa7-173">-InputObject</span></span>
<span data-ttu-id="2daa7-174">감사 정책을 관리 하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-174">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="2daa7-175">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="2daa7-175">-LogAnalytics</span></span>
<span data-ttu-id="2daa7-176">감사 로그 대상이 로그 분석 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-176">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="2daa7-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2daa7-177">-PassThru</span></span>
<span data-ttu-id="2daa7-178">Cmdlet 실행이 종료 될 때 감사 정책을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-178">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="2daa7-179">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="2daa7-179">-PredicateExpression</span></span>
<span data-ttu-id="2daa7-180">감사 로그를 필터링 하는 데 사용 되는 T-SQL 조건자 (WHERE 절)</span><span class="sxs-lookup"><span data-stu-id="2daa7-180">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="2daa7-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2daa7-181">-ResourceGroupName</span></span>
<span data-ttu-id="2daa7-182">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-182">The name of the resource group.</span></span>

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

### <span data-ttu-id="2daa7-183">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="2daa7-183">-RetentionInDays</span></span>
<span data-ttu-id="2daa7-184">감사 로그 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-184">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="2daa7-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2daa7-185">-ServerName</span></span>
<span data-ttu-id="2daa7-186">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-186">SQL server name.</span></span>

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

### <span data-ttu-id="2daa7-187">-상태</span><span class="sxs-lookup"><span data-stu-id="2daa7-187">-State</span></span>
<span data-ttu-id="2daa7-188">정책의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-188">The state of the policy.</span></span>

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

### <span data-ttu-id="2daa7-189">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2daa7-189">-StorageAccountName</span></span>
<span data-ttu-id="2daa7-190">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-190">The name of the storage account.</span></span>

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

### <span data-ttu-id="2daa7-191">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2daa7-191">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="2daa7-192">저장소 계정 구독 id</span><span class="sxs-lookup"><span data-stu-id="2daa7-192">The storage account subscription id</span></span>

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

### <span data-ttu-id="2daa7-193">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="2daa7-193">-StorageKeyType</span></span>
<span data-ttu-id="2daa7-194">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-194">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="2daa7-195">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="2daa7-195">-WorkspaceResourceId</span></span>
<span data-ttu-id="2daa7-196">감사 로그를 보낼 로그 분석 작업 영역에 대 한 작업 영역 ID (로그 분석 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-196">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="2daa7-197">예:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="2daa7-197">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="2daa7-198">-확인</span><span class="sxs-lookup"><span data-stu-id="2daa7-198">-Confirm</span></span>
<span data-ttu-id="2daa7-199">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2daa7-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2daa7-200">-WhatIf</span></span>
<span data-ttu-id="2daa7-201">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2daa7-202">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2daa7-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2daa7-203">CommonParameters</span></span>
<span data-ttu-id="2daa7-204">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2daa7-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2daa7-205">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2daa7-205">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2daa7-206">입력</span><span class="sxs-lookup"><span data-stu-id="2daa7-206">INPUTS</span></span>

### <span data-ttu-id="2daa7-207">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2daa7-207">System.String</span></span>

### <span data-ttu-id="2daa7-208">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="2daa7-208">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="2daa7-209">Microsoft. Test.sql. 감사. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="2daa7-209">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="2daa7-210">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="2daa7-210">System.String[]</span></span>

### <span data-ttu-id="2daa7-211">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2daa7-211">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2daa7-212">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="2daa7-212">System.Guid</span></span>

### <span data-ttu-id="2daa7-213">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2daa7-213">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2daa7-214">출력</span><span class="sxs-lookup"><span data-stu-id="2daa7-214">OUTPUTS</span></span>

### <span data-ttu-id="2daa7-215">Microsoft. .Sql. 감사. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="2daa7-215">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="2daa7-216">상속자</span><span class="sxs-lookup"><span data-stu-id="2daa7-216">NOTES</span></span>

## <span data-ttu-id="2daa7-217">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2daa7-217">RELATED LINKS</span></span>
