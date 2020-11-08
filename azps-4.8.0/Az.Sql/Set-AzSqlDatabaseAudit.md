---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: e13e97bd9f636de68344f83b600e440252431a22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048626"
---
# <span data-ttu-id="e4f42-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e4f42-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="e4f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4f42-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f42-103">Azure SQL 데이터베이스에 대 한 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="e4f42-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4f42-104">SYNTAX</span></span>

### <span data-ttu-id="e4f42-105">DatabaseParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4f42-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4f42-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4f42-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f42-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e4f42-107">DESCRIPTION</span></span>
<span data-ttu-id="e4f42-108">**AzSqlDatabaseAudit** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="e4f42-109">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e4f42-110">Blob 저장소가 감사 로그의 대상이 면 저장소 키를 정의 하는 감사 로그 및 *Storagekeytype* 매개 변수에 대 한 저장소 계정을 결정 하는 *storageaccountresourceid* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="e4f42-111">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="e4f42-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e4f42-112">EXAMPLES</span></span>

### <span data-ttu-id="e4f42-113">예제 1: Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e4f42-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="e4f42-114">예제 2: Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e4f42-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="e4f42-115">예제 3: T-SQL 조건자를 사용 하 여 고급 필터링이 포함 된 Azure SQL 데이터베이스의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e4f42-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="e4f42-116">예제 4: Azure SQL 데이터베이스의 감사 정책에서 고급 필터링 설정 제거</span><span class="sxs-lookup"><span data-stu-id="e4f42-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="e4f42-117">예제 5: Azure SQL 데이터베이스의 이벤트 허브 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e4f42-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="e4f42-118">예제 6: Azure SQL 데이터베이스의 이벤트 허브 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e4f42-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="e4f42-119">예제 7: Azure SQL 데이터베이스의 log analytics 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="e4f42-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="e4f42-120">예제 8: Azure SQL 데이터베이스의 log analytics 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e4f42-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="e4f42-121">예제 9: Azure SQL 데이터베이스의 log analytics 감사 정책을 통해 파이프라인 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e4f42-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="e4f42-122">예제 10: Azure SQL 데이터베이스의 감사 레코드를 blob 저장소로 보내는 기능을 사용 하지 않도록 설정 하 고 로그 분석으로 보내는 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="e4f42-123">예제 11: Azure SQL 데이터베이스의 감사 레코드를 blob 저장소, 이벤트 허브 및 로그 분석으로 보내는 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="e4f42-124">변수</span><span class="sxs-lookup"><span data-stu-id="e4f42-124">PARAMETERS</span></span>

### <span data-ttu-id="e4f42-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="e4f42-125">-AuditAction</span></span>
<span data-ttu-id="e4f42-126">감사 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-126">The set of audit actions.</span></span>  
<span data-ttu-id="e4f42-127">감사에 지원 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="e4f42-128">클릭</span><span class="sxs-lookup"><span data-stu-id="e4f42-128">SELECT</span></span>  
<span data-ttu-id="e4f42-129">UPDATE</span><span class="sxs-lookup"><span data-stu-id="e4f42-129">UPDATE</span></span>  
<span data-ttu-id="e4f42-130">넣으십시오</span><span class="sxs-lookup"><span data-stu-id="e4f42-130">INSERT</span></span>  
<span data-ttu-id="e4f42-131">삭제</span><span class="sxs-lookup"><span data-stu-id="e4f42-131">DELETE</span></span>  
<span data-ttu-id="e4f42-132">세기</span><span class="sxs-lookup"><span data-stu-id="e4f42-132">EXECUTE</span></span>  
<span data-ttu-id="e4f42-133">받기</span><span class="sxs-lookup"><span data-stu-id="e4f42-133">RECEIVE</span></span>  
<span data-ttu-id="e4f42-134">REFERENCES</span><span class="sxs-lookup"><span data-stu-id="e4f42-134">REFERENCES</span></span>  
<span data-ttu-id="e4f42-135">감사할 작업을 정의 하는 일반적인 양식은 [principal]에 따라 [개체]에서 [동작]을 선택 합니다. 위의 형식에서 [개체]는 테이블, 뷰 또는 저장 프로시저 또는 전체 데이터베이스 또는 스키마와 같은 개체를 참조할 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4f42-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="e4f42-136">두 번째 경우에는 forms 데이터베이스:: [dbname] 및 SCHEMA:: [schemaname]이 각각 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="e4f42-137">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e4f42-137">For example:</span></span>  
<span data-ttu-id="e4f42-138">공용에서 dbo myTable 선택</span><span class="sxs-lookup"><span data-stu-id="e4f42-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="e4f42-139">Public을 기준으로 데이터베이스:: myDatabase 선택</span><span class="sxs-lookup"><span data-stu-id="e4f42-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="e4f42-140">SCHEMA:: mySchema을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="e4f42-141">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4f42-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="e4f42-142">-AuditActionGroup</span></span>
<span data-ttu-id="e4f42-143">사용할 권장 되는 작업 그룹 집합은 다음 조합입니다 .이는 데이터베이스에 대해 실행 되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패 한 로그인을 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="e4f42-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="e4f42-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="e4f42-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="e4f42-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="e4f42-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="e4f42-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="e4f42-147">위의 조합은 기본적으로 구성 되는 집합 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="e4f42-148">이러한 그룹은 데이터베이스에 대해 실행 되는 모든 SQL 문과 저장 프로시저를 다루며, 다른 그룹과 함께 사용 하면 중복 감사 로그가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="e4f42-149">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4f42-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="e4f42-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="e4f42-151">Blob 저장소가 감사 레코드의 대상 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4f42-152">-DatabaseName</span></span>
<span data-ttu-id="e4f42-153">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e4f42-154">-DatabaseObject</span></span>
<span data-ttu-id="e4f42-155">감사 정책을 관리 하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f42-156">-DefaultProfile</span></span>
<span data-ttu-id="e4f42-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4f42-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="e4f42-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="e4f42-159">이벤트 허브 권한 부여 규칙의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="e4f42-159">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="e4f42-160">-EventHubName</span></span>
<span data-ttu-id="e4f42-161">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-161">The name of the event hub.</span></span> <span data-ttu-id="e4f42-162">EventHubAuthorizationRuleResourceId를 제공할 때 아무것도 지정 하지 않으면 기본 이벤트 허브가 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="e4f42-163">-EventHubTargetState</span></span>
<span data-ttu-id="e4f42-164">이벤트 허브가 감사 레코드의 대상 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="e4f42-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="e4f42-166">로그 분석이 감사 레코드의 대상 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4f42-167">-PassThru</span></span>
<span data-ttu-id="e4f42-168">Cmdlet 실행이 종료 될 때 감사 정책을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e4f42-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="e4f42-169">-PredicateExpression</span></span>
<span data-ttu-id="e4f42-170">감사 로그를 필터링 하는 데 사용 되는 T-SQL 조건자 (WHERE 절)</span><span class="sxs-lookup"><span data-stu-id="e4f42-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f42-171">-ResourceGroupName</span></span>
<span data-ttu-id="e4f42-172">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-173">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="e4f42-173">-RetentionInDays</span></span>
<span data-ttu-id="e4f42-174">감사 로그 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e4f42-175">-ServerName</span></span>
<span data-ttu-id="e4f42-176">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e4f42-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="e4f42-178">저장소 계정 리소스 id</span><span class="sxs-lookup"><span data-stu-id="e4f42-178">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="e4f42-179">-StorageKeyType</span></span>
<span data-ttu-id="e4f42-180">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e4f42-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="e4f42-182">감사 로그를 보낼 로그 분석 작업 영역에 대 한 작업 영역 ID (로그 분석 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="e4f42-183">예:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="e4f42-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4f42-184">-확인</span><span class="sxs-lookup"><span data-stu-id="e4f42-184">-Confirm</span></span>
<span data-ttu-id="e4f42-185">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f42-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f42-186">-WhatIf</span></span>
<span data-ttu-id="e4f42-187">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4f42-188">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f42-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f42-189">CommonParameters</span></span>
<span data-ttu-id="e4f42-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f42-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f42-191">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4f42-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f42-192">입력</span><span class="sxs-lookup"><span data-stu-id="e4f42-192">INPUTS</span></span>

### <span data-ttu-id="e4f42-193">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4f42-193">System.String</span></span>

### <span data-ttu-id="e4f42-194">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="e4f42-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="e4f42-195">Microsoft. Test.sql. 감사. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="e4f42-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="e4f42-196">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e4f42-196">System.String[]</span></span>

### <span data-ttu-id="e4f42-197">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="e4f42-197">System.Guid</span></span>

### <span data-ttu-id="e4f42-198">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4f42-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e4f42-199">Microsoft. .Sql. 감사. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="e4f42-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="e4f42-200">출력</span><span class="sxs-lookup"><span data-stu-id="e4f42-200">OUTPUTS</span></span>

### <span data-ttu-id="e4f42-201">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e4f42-201">System.Boolean</span></span>

## <span data-ttu-id="e4f42-202">상속자</span><span class="sxs-lookup"><span data-stu-id="e4f42-202">NOTES</span></span>

## <span data-ttu-id="e4f42-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4f42-203">RELATED LINKS</span></span>
