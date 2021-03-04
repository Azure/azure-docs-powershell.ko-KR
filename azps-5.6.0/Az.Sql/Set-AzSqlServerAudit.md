---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 8b0312ddcdce5c538b80f0245470496c534bf07f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993225"
---
# <span data-ttu-id="1ac45-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1ac45-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="1ac45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ac45-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac45-103">Azure 서버의 감사 SQL 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="1ac45-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ac45-104">SYNTAX</span></span>

### <span data-ttu-id="1ac45-105">ServerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1ac45-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ac45-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ac45-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ac45-107">설명</span><span class="sxs-lookup"><span data-stu-id="1ac45-107">DESCRIPTION</span></span>
<span data-ttu-id="1ac45-108">**Set-AzSqlServerAudit** cmdlet은 Azure SQL 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="1ac45-109">cmdlet을 사용하 는 *ResourceGroupName* 및 *ServerName* 매개 변수를 사용하여 서버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="1ac45-110">Blob Storage가 감사 로그의 대상이면 *StorageAccountResourceId* 매개 변수를 지정하여 감사 로그에 대한 저장소 계정과 *StorageKeyType* 매개 변수를 결정하여 저장소 키를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="1ac45-111">*또한 RetentionInDays* 매개 변수 값을 설정하여 감사 로그에 대한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="1ac45-112">예제</span><span class="sxs-lookup"><span data-stu-id="1ac45-112">EXAMPLES</span></span>

### <span data-ttu-id="1ac45-113">예제 1: Azure SQL Blob Storage 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="1ac45-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="1ac45-114">예제 2: Azure SQL Blob Storage 감사 정책을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="1ac45-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1ac45-115">예제 3: T-SQL 사전을 사용하여 고급 필터링을 사용하여 Azure SQL 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="1ac45-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="1ac45-116">예제 4: Azure 서버의 감사 정책에서 고급 필터링 SQL 제거</span><span class="sxs-lookup"><span data-stu-id="1ac45-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="1ac45-117">예제 5: Azure SQL 서버의 이벤트 허브 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="1ac45-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="1ac45-118">예제 6: Azure SQL 서버의 이벤트 허브 감사 정책을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="1ac45-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="1ac45-119">예제 7: Azure SQL 서버의 로그 분석 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="1ac45-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="1ac45-120">예제 8: Azure 서버의 로그 분석 감사 정책 SQL 사용 안 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ac45-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1ac45-121">예제 9: 파이프라인을 통해 Azure SQL 감사 정책 사용 안 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ac45-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1ac45-122">예제 10: Azure SQL 서버의 감사 레코드를 Blob Storage에 보내지 않도록 설정하고 로그 분석에 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1ac45-123">예제 11: Azure SQL 서버의 감사 레코드를 Blob Storage, 이벤트 허브 및 로그 분석에 전송하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="1ac45-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ac45-124">PARAMETERS</span></span>

### <span data-ttu-id="1ac45-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ac45-125">-AsJob</span></span>
<span data-ttu-id="1ac45-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1ac45-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ac45-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="1ac45-127">-AuditActionGroup</span></span>
<span data-ttu-id="1ac45-128">사용할 권장되는 작업 그룹 집합은 다음과 같은 조합입니다. 이렇게 하면 데이터베이스에 대해 실행된 모든 쿼리 및 저장 프로시저뿐만 아니라 성공 및 실패한 로그인도 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="1ac45-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="1ac45-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="1ac45-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="1ac45-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="1ac45-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="1ac45-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="1ac45-132">위의 조합은 기본적으로 구성된 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="1ac45-133">이러한 그룹은 데이터베이스에 대해 SQL 모든 명령문 및 저장 프로시저를 다루며, 중복 감사 로그를 생성하기 때문에 다른 그룹과 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="1ac45-134">자세한 내용은 https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1ac45-134">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="1ac45-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="1ac45-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="1ac45-136">Blob Storage가 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="1ac45-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac45-137">-DefaultProfile</span></span>
<span data-ttu-id="1ac45-138">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ac45-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="1ac45-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="1ac45-140">이벤트 허브 권한 부여 규칙에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1ac45-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="1ac45-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="1ac45-141">-EventHubName</span></span>
<span data-ttu-id="1ac45-142">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-142">The name of the event hub.</span></span> <span data-ttu-id="1ac45-143">EventHubAuthorizationRuleResourceId를 제공 할 때 지정되지 않은 경우 기본 이벤트 허브가 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="1ac45-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="1ac45-144">-EventHubTargetState</span></span>
<span data-ttu-id="1ac45-145">이벤트 허브가 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="1ac45-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="1ac45-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="1ac45-147">로그 분석이 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="1ac45-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ac45-148">-PassThru</span></span>
<span data-ttu-id="1ac45-149">cmdlet 실행이 끝날 때 감사 정책을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1ac45-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="1ac45-150">-PredicateExpression</span></span>
<span data-ttu-id="1ac45-151">감사 SQL 필터링하는 데 사용되는 T-SQL(WHERE 절)입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="1ac45-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac45-152">-ResourceGroupName</span></span>
<span data-ttu-id="1ac45-153">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac45-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1ac45-154">-RetentionInDays</span></span>
<span data-ttu-id="1ac45-155">감사 로그에 대한 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="1ac45-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ac45-156">-ServerName</span></span>
<span data-ttu-id="1ac45-157">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac45-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="1ac45-158">-ServerObject</span></span>
<span data-ttu-id="1ac45-159">서버 개체는 감사 정책을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac45-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1ac45-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="1ac45-161">저장소 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1ac45-161">The storage account resource id</span></span>

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

### <span data-ttu-id="1ac45-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="1ac45-162">-StorageKeyType</span></span>
<span data-ttu-id="1ac45-163">사용할 저장소 액세스 키 중를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="1ac45-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="1ac45-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="1ac45-165">감사 로그를 보내고자 하는 Log Analytics 작업 영역의 작업 영역 ID(Log Analytics 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="1ac45-166">예제: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="1ac45-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="1ac45-167">-확인</span><span class="sxs-lookup"><span data-stu-id="1ac45-167">-Confirm</span></span>
<span data-ttu-id="1ac45-168">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ac45-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac45-169">-WhatIf</span></span>
<span data-ttu-id="1ac45-170">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ac45-171">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ac45-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac45-172">CommonParameters</span></span>
<span data-ttu-id="1ac45-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac45-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac45-174">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ac45-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac45-175">입력</span><span class="sxs-lookup"><span data-stu-id="1ac45-175">INPUTS</span></span>

### <span data-ttu-id="1ac45-176">System.String</span><span class="sxs-lookup"><span data-stu-id="1ac45-176">System.String</span></span>

### <span data-ttu-id="1ac45-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1ac45-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="1ac45-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="1ac45-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="1ac45-179">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1ac45-179">System.Guid</span></span>

### <span data-ttu-id="1ac45-180">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1ac45-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1ac45-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="1ac45-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="1ac45-182">출력</span><span class="sxs-lookup"><span data-stu-id="1ac45-182">OUTPUTS</span></span>

### <span data-ttu-id="1ac45-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ac45-183">System.Boolean</span></span>

## <span data-ttu-id="1ac45-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ac45-184">NOTES</span></span>

## <span data-ttu-id="1ac45-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ac45-185">RELATED LINKS</span></span>
