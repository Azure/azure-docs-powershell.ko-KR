---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 5ba80e2b8c2ca315f9b51b9873688f0b80f1e85f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878789"
---
# <span data-ttu-id="af67c-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="af67c-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="af67c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af67c-102">SYNOPSIS</span></span>
<span data-ttu-id="af67c-103">Azure SQL server의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="af67c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af67c-104">SYNTAX</span></span>

### <span data-ttu-id="af67c-105">ServerParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="af67c-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af67c-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af67c-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af67c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="af67c-107">DESCRIPTION</span></span>
<span data-ttu-id="af67c-108">**AzSqlServerAudit** Cmdlet은 Azure SQL server의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="af67c-109">Cmdlet을 사용 하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 사용 하 여 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="af67c-110">Blob 저장소가 감사 로그의 대상이 면 저장소 키를 정의 하는 감사 로그 및 *Storagekeytype* 매개 변수에 대 한 저장소 계정을 결정 하는 *storageaccountresourceid* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="af67c-111">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="af67c-112">예제의</span><span class="sxs-lookup"><span data-stu-id="af67c-112">EXAMPLES</span></span>

### <span data-ttu-id="af67c-113">예제 1: Azure SQL server의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="af67c-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="af67c-114">예제 2: Azure SQL server의 blob 저장소 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="af67c-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="af67c-115">예제 3.1: T-SQL 조건자를 사용 하 여 고급 필터링이 포함 된 Azure SQL server의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="af67c-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="af67c-116">예제 3.2: Azure SQL server의 감사 정책에서 고급 필터링 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="af67c-117">예제 4: Azure SQL server의 이벤트 허브 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="af67c-117">Example 4: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="af67c-118">예제 5: Azure SQL server의 이벤트 허브 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="af67c-118">Example 5: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="af67c-119">예제 6: Azure SQL server의 log analytics 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="af67c-119">Example 6: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="af67c-120">예제 7: Azure SQL server의 log analytics 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="af67c-120">Example 7: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="af67c-121">예제 8: Azure SQL server의 log analytics 감사 정책을 통해 파이프라인 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="af67c-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="af67c-122">예제 9: Azure SQL server의 감사 레코드를 blob 저장소로 보내는 기능을 사용 하지 않도록 설정 하 고 로그 분석으로 보내는 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-122">Example 9: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="af67c-123">예제 10: Azure SQL server의 감사 레코드를 blob 저장소, 이벤트 허브 및 로그 분석으로 보내는 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-123">Example 10: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="af67c-124">변수</span><span class="sxs-lookup"><span data-stu-id="af67c-124">PARAMETERS</span></span>

### <span data-ttu-id="af67c-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af67c-125">-AsJob</span></span>
<span data-ttu-id="af67c-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="af67c-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af67c-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="af67c-127">-AuditActionGroup</span></span>
<span data-ttu-id="af67c-128">사용할 권장 되는 작업 그룹 집합은 다음 조합입니다 .이는 데이터베이스에 대해 실행 되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패 한 로그인을 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="af67c-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="af67c-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="af67c-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="af67c-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="af67c-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="af67c-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="af67c-132">위의 조합은 기본적으로 구성 되는 집합 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="af67c-133">이러한 그룹은 데이터베이스에 대해 실행 되는 모든 SQL 문과 저장 프로시저를 다루며, 다른 그룹과 함께 사용 하면 중복 감사 로그가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="af67c-134">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 하세요.</span><span class="sxs-lookup"><span data-stu-id="af67c-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="af67c-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="af67c-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="af67c-136">Blob 저장소가 감사 레코드의 대상 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="af67c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af67c-137">-DefaultProfile</span></span>
<span data-ttu-id="af67c-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af67c-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="af67c-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="af67c-140">이벤트 허브 권한 부여 규칙의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="af67c-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="af67c-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="af67c-141">-EventHubName</span></span>
<span data-ttu-id="af67c-142">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-142">The name of the event hub.</span></span> <span data-ttu-id="af67c-143">EventHubAuthorizationRuleResourceId를 제공할 때 아무것도 지정 하지 않으면 기본 이벤트 허브가 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="af67c-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="af67c-144">-EventHubTargetState</span></span>
<span data-ttu-id="af67c-145">이벤트 허브가 감사 레코드의 대상 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="af67c-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="af67c-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="af67c-147">로그 분석이 감사 레코드의 대상 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="af67c-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af67c-148">-PassThru</span></span>
<span data-ttu-id="af67c-149">Cmdlet 실행이 종료 될 때 감사 정책을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="af67c-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="af67c-150">-PredicateExpression</span></span>
<span data-ttu-id="af67c-151">감사 로그를 필터링 하는 데 사용 되는 T-SQL 조건자 (WHERE 절)</span><span class="sxs-lookup"><span data-stu-id="af67c-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="af67c-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af67c-152">-ResourceGroupName</span></span>
<span data-ttu-id="af67c-153">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="af67c-154">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="af67c-154">-RetentionInDays</span></span>
<span data-ttu-id="af67c-155">감사 로그 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="af67c-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af67c-156">-ServerName</span></span>
<span data-ttu-id="af67c-157">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-157">SQL server name.</span></span>

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

### <span data-ttu-id="af67c-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="af67c-158">-ServerObject</span></span>
<span data-ttu-id="af67c-159">감사 정책을 관리 하는 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-159">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="af67c-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="af67c-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="af67c-161">저장소 계정 리소스 id</span><span class="sxs-lookup"><span data-stu-id="af67c-161">The storage account resource id</span></span>

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

### <span data-ttu-id="af67c-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="af67c-162">-StorageKeyType</span></span>
<span data-ttu-id="af67c-163">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="af67c-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="af67c-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="af67c-165">감사 로그를 보낼 로그 분석 작업 영역에 대 한 작업 영역 ID (로그 분석 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="af67c-166">예:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="af67c-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="af67c-167">-확인</span><span class="sxs-lookup"><span data-stu-id="af67c-167">-Confirm</span></span>
<span data-ttu-id="af67c-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af67c-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af67c-169">-WhatIf</span></span>
<span data-ttu-id="af67c-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af67c-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af67c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af67c-172">CommonParameters</span></span>
<span data-ttu-id="af67c-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af67c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af67c-174">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af67c-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af67c-175">입력</span><span class="sxs-lookup"><span data-stu-id="af67c-175">INPUTS</span></span>

### <span data-ttu-id="af67c-176">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="af67c-176">System.String</span></span>

### <span data-ttu-id="af67c-177">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="af67c-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="af67c-178">Microsoft. Test.sql. 감사. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="af67c-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="af67c-179">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="af67c-179">System.Guid</span></span>

### <span data-ttu-id="af67c-180">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af67c-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af67c-181">Microsoft. .Sql. 감사. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="af67c-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="af67c-182">출력</span><span class="sxs-lookup"><span data-stu-id="af67c-182">OUTPUTS</span></span>

### <span data-ttu-id="af67c-183">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="af67c-183">System.Boolean</span></span>

## <span data-ttu-id="af67c-184">상속자</span><span class="sxs-lookup"><span data-stu-id="af67c-184">NOTES</span></span>

## <span data-ttu-id="af67c-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af67c-185">RELATED LINKS</span></span>
