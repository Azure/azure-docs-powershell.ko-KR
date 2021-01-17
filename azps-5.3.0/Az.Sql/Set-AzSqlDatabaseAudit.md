---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 9afa329aae934fd713d80702dc32b402015afc8a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492164"
---
# <span data-ttu-id="6ad18-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6ad18-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="6ad18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad18-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad18-103">Azure SQL 데이터베이스에 대한 감사 설정을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="6ad18-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ad18-104">SYNTAX</span></span>

### <span data-ttu-id="6ad18-105">DatabaseParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ad18-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad18-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad18-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad18-107">설명</span><span class="sxs-lookup"><span data-stu-id="6ad18-107">DESCRIPTION</span></span>
<span data-ttu-id="6ad18-108">**Set-AzSqlDatabaseAudit cmdlet은** Azure SQL 데이터베이스의 감사 설정을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="6ad18-109">cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 사용하여 데이터베이스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="6ad18-110">Blob Storage가 감사 로그의 대상인 경우 *StorageAccountResourceId* 매개 변수를 지정하여 감사 로그에 대한 스토리지 계정 및 스토리지 키를 정의하는 *StorageKeyType* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="6ad18-111">*RetentionInDays* 매개 변수의 값을 설정하여 감사 로그에 대한 기간을 정의하여 감사 로그에 대한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="6ad18-112">예제</span><span class="sxs-lookup"><span data-stu-id="6ad18-112">EXAMPLES</span></span>

### <span data-ttu-id="6ad18-113">예제 1: Azure SQL 데이터베이스의 Blob Storage 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="6ad18-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="6ad18-114">예제 2: Azure SQL 데이터베이스의 Blob Storage 감사 정책 비활성화</span><span class="sxs-lookup"><span data-stu-id="6ad18-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="6ad18-115">예제 3: T-SQL 사용하여 필터링을 통해 Azure SQL 데이터베이스의 Blob Storage 감사 정책을 사용하도록 SQL 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "schema_name <> 'sys''" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="6ad18-116">예제 4: Azure SQL 데이터베이스의 감사 정책에서 필터링 제거</span><span class="sxs-lookup"><span data-stu-id="6ad18-116">Example 4: Remove the filtering from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="6ad18-117">예제 5: Azure SQL 데이터베이스의 이벤트 허브 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="6ad18-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="6ad18-118">예제 6: Azure SQL 데이터베이스의 이벤트 허브 감사 정책 비활성화</span><span class="sxs-lookup"><span data-stu-id="6ad18-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="6ad18-119">예제 7: Azure SQL 데이터베이스의 로그 분석 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="6ad18-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="6ad18-120">예제 8: Azure SQL 데이터베이스의 로그 분석 감사 정책 비활성화</span><span class="sxs-lookup"><span data-stu-id="6ad18-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="6ad18-121">예제 9: 파이프라인을 통해 Azure SQL 데이터베이스의 로그 분석 감사 정책 비활성화</span><span class="sxs-lookup"><span data-stu-id="6ad18-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="6ad18-122">예제 10: Azure SQL 데이터베이스의 감사 레코드를 Blob Storage로 보내지 않도록 설정하고 로그 분석에 보낼 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="6ad18-123">예제 11: Azure SQL 데이터베이스의 감사 레코드를 Blob Storage, 이벤트 허브 및 로그 분석에 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="6ad18-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ad18-124">PARAMETERS</span></span>

### <span data-ttu-id="6ad18-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="6ad18-125">-AuditAction</span></span>
<span data-ttu-id="6ad18-126">감사 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-126">The set of audit actions.</span></span>  
<span data-ttu-id="6ad18-127">감사에 지원되는 작업은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="6ad18-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="6ad18-128">SELECT</span></span>  
<span data-ttu-id="6ad18-129">UPDATE</span><span class="sxs-lookup"><span data-stu-id="6ad18-129">UPDATE</span></span>  
<span data-ttu-id="6ad18-130">INSERT</span><span class="sxs-lookup"><span data-stu-id="6ad18-130">INSERT</span></span>  
<span data-ttu-id="6ad18-131">DELETE</span><span class="sxs-lookup"><span data-stu-id="6ad18-131">DELETE</span></span>  
<span data-ttu-id="6ad18-132">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="6ad18-132">EXECUTE</span></span>  
<span data-ttu-id="6ad18-133">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="6ad18-133">RECEIVE</span></span>  
<span data-ttu-id="6ad18-134">참조</span><span class="sxs-lookup"><span data-stu-id="6ad18-134">REFERENCES</span></span>  
<span data-ttu-id="6ad18-135">감사할 작업을 정의하는 일반적인 양식은 [action] ON [object] BY [principal] 위 형식의 [object]는 테이블, 뷰 또는 저장 프로시저와 같은 개체 또는 전체 데이터베이스 또는 schema를 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="6ad18-136">후자의 경우 각각 DATABASE::[dbname] 및 SCHEMA::[schemaname] 양식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="6ad18-137">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="6ad18-137">For example:</span></span>  
<span data-ttu-id="6ad18-138">공용으로 dbo.myTable에서 SELECT</span><span class="sxs-lookup"><span data-stu-id="6ad18-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="6ad18-139">데이터베이스에서 SELECT::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="6ad18-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="6ad18-140">SCHEMA::mySchema by public에서 SELECT</span><span class="sxs-lookup"><span data-stu-id="6ad18-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="6ad18-141">자세한 내용은 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6ad18-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="6ad18-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="6ad18-142">-AuditActionGroup</span></span>
<span data-ttu-id="6ad18-143">사용할 권장 작업 그룹 집합은 다음과 같은 조합입니다. 데이터베이스에 대해 실행되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패한 로그인을 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="6ad18-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="6ad18-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="6ad18-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="6ad18-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="6ad18-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="6ad18-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="6ad18-147">위의 조합은 기본적으로 구성된 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="6ad18-148">이러한 그룹은 데이터베이스에 대해 SQL 모든 명령문 및 저장 프로시저를 다루며, 중복 감사 로그를 생성하기 때문에 다른 그룹과 함께 사용되지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="6ad18-149">자세한 내용은 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6ad18-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="6ad18-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="6ad18-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="6ad18-151">Blob Storage가 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="6ad18-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ad18-152">-DatabaseName</span></span>
<span data-ttu-id="6ad18-153">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-153">SQL Database name.</span></span>

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

### <span data-ttu-id="6ad18-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6ad18-154">-DatabaseObject</span></span>
<span data-ttu-id="6ad18-155">감사 정책을 관리하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="6ad18-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad18-156">-DefaultProfile</span></span>
<span data-ttu-id="6ad18-157">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad18-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad18-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="6ad18-159">이벤트 허브 권한 부여 규칙에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6ad18-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="6ad18-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="6ad18-160">-EventHubName</span></span>
<span data-ttu-id="6ad18-161">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-161">The name of the event hub.</span></span> <span data-ttu-id="6ad18-162">EventHubAuthorizationRuleResourceId를 제공하는 경우 지정되지 않은 경우 기본 이벤트 허브가 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="6ad18-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="6ad18-163">-EventHubTargetState</span></span>
<span data-ttu-id="6ad18-164">이벤트 허브가 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="6ad18-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="6ad18-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="6ad18-166">로그 분석이 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="6ad18-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ad18-167">-PassThru</span></span>
<span data-ttu-id="6ad18-168">cmdlet 실행이 끝나면 감사 정책을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="6ad18-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="6ad18-169">-PredicateExpression</span></span>
<span data-ttu-id="6ad18-170">감사 SQL 데 사용되는 T-SQL(WHERE 절)입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="6ad18-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad18-171">-ResourceGroupName</span></span>
<span data-ttu-id="6ad18-172">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ad18-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6ad18-173">-RetentionInDays</span></span>
<span data-ttu-id="6ad18-174">감사 로그에 대한 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="6ad18-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6ad18-175">-ServerName</span></span>
<span data-ttu-id="6ad18-176">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-176">SQL server name.</span></span>

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

### <span data-ttu-id="6ad18-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad18-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="6ad18-178">저장소 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6ad18-178">The storage account resource id</span></span>

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

### <span data-ttu-id="6ad18-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="6ad18-179">-StorageKeyType</span></span>
<span data-ttu-id="6ad18-180">사용할 저장소 액세스 키 중 어느 것이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="6ad18-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad18-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="6ad18-182">감사 로그를 보내고자 하는 Log Analytics 작업 영역의 작업 영역 ID(Log Analytics 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="6ad18-183">예: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="6ad18-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="6ad18-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ad18-184">-Confirm</span></span>
<span data-ttu-id="6ad18-185">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad18-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad18-186">-WhatIf</span></span>
<span data-ttu-id="6ad18-187">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6ad18-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ad18-188">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad18-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad18-189">CommonParameters</span></span>
<span data-ttu-id="6ad18-190">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad18-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad18-191">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ad18-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad18-192">입력</span><span class="sxs-lookup"><span data-stu-id="6ad18-192">INPUTS</span></span>

### <span data-ttu-id="6ad18-193">System.String</span><span class="sxs-lookup"><span data-stu-id="6ad18-193">System.String</span></span>

### <span data-ttu-id="6ad18-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6ad18-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="6ad18-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="6ad18-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="6ad18-196">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6ad18-196">System.String[]</span></span>

### <span data-ttu-id="6ad18-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6ad18-197">System.Guid</span></span>

### <span data-ttu-id="6ad18-198">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ad18-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6ad18-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="6ad18-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="6ad18-200">출력</span><span class="sxs-lookup"><span data-stu-id="6ad18-200">OUTPUTS</span></span>

### <span data-ttu-id="6ad18-201">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ad18-201">System.Boolean</span></span>

## <span data-ttu-id="6ad18-202">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ad18-202">NOTES</span></span>

## <span data-ttu-id="6ad18-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ad18-203">RELATED LINKS</span></span>
