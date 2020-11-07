---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: 44db866488459382a3b66f77328b5cbc9259754b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698758"
---
# <span data-ttu-id="a5c60-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="a5c60-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="a5c60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5c60-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c60-103">Azure SQL server의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="a5c60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5c60-104">SYNTAX</span></span>

### <span data-ttu-id="a5c60-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5c60-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c60-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="a5c60-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c60-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="a5c60-107">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c60-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="a5c60-108">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c60-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a5c60-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c60-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a5c60-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c60-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a5c60-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c60-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="a5c60-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c60-113">설명은</span><span class="sxs-lookup"><span data-stu-id="a5c60-113">DESCRIPTION</span></span>
<span data-ttu-id="a5c60-114">**AzSqlServerAuditing** Cmdlet은 Azure SQL server의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-114">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="a5c60-115">Cmdlet을 사용 하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 사용 하 여 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-115">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="a5c60-116">감사 로그 대상은 BlobStorage, LogAnalytics 또는 EventHub (지정 하지 않은 경우 기본적으로 BlobStorage)와 같은 스위치 매개 변수 중 하나를 지정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="a5c60-117">*State* 매개 변수를 사용 하 여 정책을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="a5c60-118">감사 로그 대상이 blob storage 인 경우, 저장소 키를 정의 하는 감사 로그 및 *Storageaccountname* 매개 변수에 대 한 저장소 계정을 결정 하는 *storageaccountname* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="a5c60-119">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="a5c60-120">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 서버 식별자 외에도 현재 감사 설정을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="a5c60-121">서버 식별자에는 **ResourceGroupName** 및 **ServerName** 이 포함 되지만이에 국한 되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-121">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="a5c60-122">예제의</span><span class="sxs-lookup"><span data-stu-id="a5c60-122">EXAMPLES</span></span>

### <span data-ttu-id="a5c60-123">예제 1: Azure SQL server의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="a5c60-123">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="a5c60-124">예제 2: Azure SQL server의 blob 저장소 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a5c60-124">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="a5c60-125">예제 3: 다른 구독의 저장소 계정을 사용 하 여 Azure SQL server의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="a5c60-125">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="a5c60-126">예제 4: T-SQL 조건자를 사용 하 여 고급 필터링이 포함 된 Azure SQL server의 blob 저장소 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="a5c60-126">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="a5c60-127">예제 5: Azure SQL server의 blob 감사 저장소 정책에서 고급 필터링 설정 제거</span><span class="sxs-lookup"><span data-stu-id="a5c60-127">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="a5c60-128">예제 6: Azure SQL server의 이벤트 허브 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="a5c60-128">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="a5c60-129">예제 7: Azure SQL server의 이벤트 허브 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a5c60-129">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="a5c60-130">예제 8: Azure SQL server의 log analytics 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="a5c60-130">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="a5c60-131">예제 9: Azure SQL server의 log analytics 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a5c60-131">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="a5c60-132">예제 10: Azure SQL server의 log analytics 감사 정책을 통해 파이프라인 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a5c60-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="a5c60-133">변수</span><span class="sxs-lookup"><span data-stu-id="a5c60-133">PARAMETERS</span></span>

### <span data-ttu-id="a5c60-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5c60-134">-AsJob</span></span>
<span data-ttu-id="a5c60-135">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a5c60-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5c60-136">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="a5c60-136">-AuditActionGroup</span></span>
<span data-ttu-id="a5c60-137">사용할 권장 되는 작업 그룹 집합은 다음 조합입니다 .이는 데이터베이스에 대해 실행 되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패 한 로그인을 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-137">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="a5c60-138">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a5c60-138">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="a5c60-139">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="a5c60-139">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="a5c60-140">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="a5c60-140">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="a5c60-141">위의 조합은 기본적으로 구성 되는 집합 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-141">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="a5c60-142">이러한 그룹은 데이터베이스에 대해 실행 되는 모든 SQL 문과 저장 프로시저를 다루며, 다른 그룹과 함께 사용 하면 중복 감사 로그가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-142">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="a5c60-143">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5c60-143">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="a5c60-144">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="a5c60-144">-BlobStorage</span></span>
<span data-ttu-id="a5c60-145">감사 로그 대상이 blob storage 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-145">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="a5c60-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c60-146">-DefaultProfile</span></span>
<span data-ttu-id="a5c60-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5c60-148">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a5c60-148">-EventHub</span></span>
<span data-ttu-id="a5c60-149">감사 로그 대상이 이벤트 허브 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-149">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="a5c60-150">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c60-150">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="a5c60-151">이벤트 허브 권한 부여 규칙의 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="a5c60-151">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="a5c60-152">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="a5c60-152">-EventHubName</span></span>
<span data-ttu-id="a5c60-153">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-153">The name of the event hub.</span></span> <span data-ttu-id="a5c60-154">EventHubAuthorizationRuleResourceId를 제공할 때 아무것도 지정 하지 않으면 기본 이벤트 허브가 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-154">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="a5c60-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5c60-155">-InputObject</span></span>
<span data-ttu-id="a5c60-156">감사 정책을 관리 하는 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-156">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c60-157">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="a5c60-157">-LogAnalytics</span></span>
<span data-ttu-id="a5c60-158">감사 로그 대상이 로그 분석 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-158">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="a5c60-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5c60-159">-PassThru</span></span>
<span data-ttu-id="a5c60-160">Cmdlet 실행이 종료 될 때 감사 정책을 출력할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-160">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="a5c60-161">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="a5c60-161">-PredicateExpression</span></span>
<span data-ttu-id="a5c60-162">감사 로그를 필터링 하는 데 사용 되는 T-SQL 조건자 (WHERE 절)</span><span class="sxs-lookup"><span data-stu-id="a5c60-162">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="a5c60-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c60-163">-ResourceGroupName</span></span>
<span data-ttu-id="a5c60-164">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-164">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5c60-165">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="a5c60-165">-RetentionInDays</span></span>
<span data-ttu-id="a5c60-166">감사 로그 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-166">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="a5c60-167">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a5c60-167">-ServerName</span></span>
<span data-ttu-id="a5c60-168">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-168">SQL server name.</span></span>

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

### <span data-ttu-id="a5c60-169">-상태</span><span class="sxs-lookup"><span data-stu-id="a5c60-169">-State</span></span>
<span data-ttu-id="a5c60-170">정책의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-170">The state of the policy.</span></span>

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

### <span data-ttu-id="a5c60-171">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a5c60-171">-StorageAccountName</span></span>
<span data-ttu-id="a5c60-172">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-172">The name of the storage account.</span></span>

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

### <span data-ttu-id="a5c60-173">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5c60-173">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="a5c60-174">저장소 계정 구독 id</span><span class="sxs-lookup"><span data-stu-id="a5c60-174">The storage account subscription id</span></span>

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

### <span data-ttu-id="a5c60-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a5c60-175">-StorageKeyType</span></span>
<span data-ttu-id="a5c60-176">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="a5c60-177">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c60-177">-WorkspaceResourceId</span></span>
<span data-ttu-id="a5c60-178">감사 로그를 보낼 로그 분석 작업 영역에 대 한 작업 영역 ID (로그 분석 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-178">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="a5c60-179">예:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="a5c60-179">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="a5c60-180">-확인</span><span class="sxs-lookup"><span data-stu-id="a5c60-180">-Confirm</span></span>
<span data-ttu-id="a5c60-181">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c60-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c60-182">-WhatIf</span></span>
<span data-ttu-id="a5c60-183">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-183">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5c60-184">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c60-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c60-185">CommonParameters</span></span>
<span data-ttu-id="a5c60-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c60-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c60-187">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5c60-187">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c60-188">입력</span><span class="sxs-lookup"><span data-stu-id="a5c60-188">INPUTS</span></span>

### <span data-ttu-id="a5c60-189">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a5c60-189">System.String</span></span>

### <span data-ttu-id="a5c60-190">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="a5c60-190">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="a5c60-191">Microsoft. Test.sql. 감사. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="a5c60-191">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="a5c60-192">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5c60-192">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a5c60-193">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="a5c60-193">System.Guid</span></span>

### <span data-ttu-id="a5c60-194">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a5c60-194">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a5c60-195">출력</span><span class="sxs-lookup"><span data-stu-id="a5c60-195">OUTPUTS</span></span>

### <span data-ttu-id="a5c60-196">Microsoft. .Sql. 감사. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="a5c60-196">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="a5c60-197">상속자</span><span class="sxs-lookup"><span data-stu-id="a5c60-197">NOTES</span></span>

## <span data-ttu-id="a5c60-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5c60-198">RELATED LINKS</span></span>
