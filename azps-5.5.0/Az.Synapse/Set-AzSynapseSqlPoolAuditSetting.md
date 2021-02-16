---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195561"
---
# <span data-ttu-id="7440a-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="7440a-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="7440a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7440a-102">SYNOPSIS</span></span>
<span data-ttu-id="7440a-103">Azure Synapse Analytics 풀에 대한 감사 SQL 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7440a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7440a-104">SYNTAX</span></span>

### <span data-ttu-id="7440a-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7440a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7440a-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7440a-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7440a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7440a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7440a-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7440a-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7440a-109">설명</span><span class="sxs-lookup"><span data-stu-id="7440a-109">DESCRIPTION</span></span>
<span data-ttu-id="7440a-110">**Set-AzSynapseSqlPoolAuditSetting** cmdlet은 Azure Synapse Analytics 풀의 감사 설정을 SQL 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="7440a-111">Blob Storage가 감사 로그의 대상인 경우 *StorageAccountResourceId* 매개 변수를 지정하여 감사 로그에 대한 스토리지 계정 및 스토리지 키를 정의하는 *StorageKeyType* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="7440a-112">*RetentionInDays* 매개 변수의 값을 설정하여 감사 로그에 대한 기간을 정의하여 감사 로그에 대한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="7440a-113">예제</span><span class="sxs-lookup"><span data-stu-id="7440a-113">EXAMPLES</span></span>

### <span data-ttu-id="7440a-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="7440a-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="7440a-115">ContosoSqlPool이라는 Azure Synapse Analytics SQL Blob Storage 감사 정책을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="7440a-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="7440a-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="7440a-117">ContosoSqlPool이라는 Azure Synapse Analytics SQL Blob Storage 감사 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="7440a-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="7440a-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="7440a-119">T-SQL 사용하여 고급 필터링을 사용하여 ContosoSqlPool이라는 Azure Synapse Analytics SQL 풀의 Blob Storage 감사 정책을 사용하도록 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="7440a-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="7440a-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="7440a-121">ContosoSqlPool이라는 Azure Synapse Analytics SQL 정책에서 고급 필터링 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="7440a-122">예제 5</span><span class="sxs-lookup"><span data-stu-id="7440a-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="7440a-123">파이프라인을 통해 ContosoSqlPool이라는 Azure Synapse Analytics SQL Blob Storage 감사 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="7440a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7440a-124">PARAMETERS</span></span>

### <span data-ttu-id="7440a-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7440a-125">-AsJob</span></span>
<span data-ttu-id="7440a-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7440a-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7440a-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="7440a-127">-AuditAction</span></span>
<span data-ttu-id="7440a-128">감사 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-128">The set of audit actions.</span></span>

<span data-ttu-id="7440a-129">감사에 지원되는 작업은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-129">The supported actions to audit are:</span></span>

<span data-ttu-id="7440a-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="7440a-130">SELECT</span></span>

<span data-ttu-id="7440a-131">UPDATE</span><span class="sxs-lookup"><span data-stu-id="7440a-131">UPDATE</span></span>

<span data-ttu-id="7440a-132">INSERT</span><span class="sxs-lookup"><span data-stu-id="7440a-132">INSERT</span></span>

<span data-ttu-id="7440a-133">DELETE</span><span class="sxs-lookup"><span data-stu-id="7440a-133">DELETE</span></span>

<span data-ttu-id="7440a-134">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="7440a-134">EXECUTE</span></span>

<span data-ttu-id="7440a-135">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="7440a-135">RECEIVE</span></span>

<span data-ttu-id="7440a-136">참조</span><span class="sxs-lookup"><span data-stu-id="7440a-136">REFERENCES</span></span>

<span data-ttu-id="7440a-137">감사할 작업을 정의하는 일반적인 양식은</span><span class="sxs-lookup"><span data-stu-id="7440a-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="7440a-138">\[action \] ON object BY \[ \] \[ principal\]</span><span class="sxs-lookup"><span data-stu-id="7440a-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="7440a-139">위의 형식의 개체는 테이블, 뷰 또는 저장 프로시저와 같은 개체 또는 전체 데이터베이스 또는 \[ \] 스마마를 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="7440a-140">후자의 경우 데이터베이스:: \[ dbname 및 \] SCHEMA:: \[ schemaname이 각각 \] 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="7440a-141">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="7440a-141">For example:</span></span>

<span data-ttu-id="7440a-142">공용으로 dbo.myTable에서 SELECT</span><span class="sxs-lookup"><span data-stu-id="7440a-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="7440a-143">데이터베이스에서 SELECT::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="7440a-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="7440a-144">SCHEMA::mySchema by public에서 SELECT</span><span class="sxs-lookup"><span data-stu-id="7440a-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="7440a-145">자세한 내용은 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7440a-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="7440a-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="7440a-146">-AuditActionGroup</span></span>
<span data-ttu-id="7440a-147">사용할 권장 작업 그룹 집합은 다음과 같은 조합입니다. 데이터베이스에 대해 실행되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패한 로그인을 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="7440a-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7440a-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="7440a-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="7440a-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="7440a-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="7440a-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="7440a-151">위의 조합은 기본적으로 구성된 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="7440a-152">이러한 그룹은 데이터베이스에 대해 SQL 모든 명령문 및 저장 프로시저를 다루며, 중복 감사 로그를 생성하기 때문에 다른 그룹과 함께 사용되지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="7440a-153">자세한 내용은 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7440a-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440a-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="7440a-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="7440a-155">Blob Storage가 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="7440a-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7440a-156">-DefaultProfile</span></span>
<span data-ttu-id="7440a-157">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7440a-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7440a-158">-InputObject</span></span>
<span data-ttu-id="7440a-159">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7440a-160">-Name</span><span class="sxs-lookup"><span data-stu-id="7440a-160">-Name</span></span>
<span data-ttu-id="7440a-161">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440a-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7440a-162">-PassThru</span></span>
<span data-ttu-id="7440a-163">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7440a-164">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7440a-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="7440a-165">-PredicateExpression</span></span>
<span data-ttu-id="7440a-166">감사 SQL 데 사용되는 T-SQL(WHERE 절)입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="7440a-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7440a-167">-ResourceGroupName</span></span>
<span data-ttu-id="7440a-168">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-168">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440a-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7440a-169">-ResourceId</span></span>
<span data-ttu-id="7440a-170">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-170">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440a-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7440a-171">-RetentionInDays</span></span>
<span data-ttu-id="7440a-172">감사 로그에 대한 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="7440a-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="7440a-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="7440a-174">저장소 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7440a-174">The storage account resource id</span></span>

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

### <span data-ttu-id="7440a-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7440a-175">-StorageKeyType</span></span>
<span data-ttu-id="7440a-176">사용할 저장소 액세스 키 중 어느 것이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="7440a-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7440a-177">-WorkspaceName</span></span>
<span data-ttu-id="7440a-178">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-178">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7440a-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7440a-179">-WorkspaceObject</span></span>
<span data-ttu-id="7440a-180">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7440a-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7440a-181">-Confirm</span></span>
<span data-ttu-id="7440a-182">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7440a-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7440a-183">-WhatIf</span></span>
<span data-ttu-id="7440a-184">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7440a-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7440a-185">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7440a-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7440a-186">CommonParameters</span></span>
<span data-ttu-id="7440a-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7440a-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7440a-188">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7440a-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7440a-189">입력</span><span class="sxs-lookup"><span data-stu-id="7440a-189">INPUTS</span></span>

### <span data-ttu-id="7440a-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7440a-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7440a-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7440a-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7440a-192">출력</span><span class="sxs-lookup"><span data-stu-id="7440a-192">OUTPUTS</span></span>

### <span data-ttu-id="7440a-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="7440a-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="7440a-194">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7440a-194">NOTES</span></span>

## <span data-ttu-id="7440a-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7440a-195">RELATED LINKS</span></span>
