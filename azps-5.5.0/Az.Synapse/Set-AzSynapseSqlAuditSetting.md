---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ae09bb11b56bd6c5fa0add402ace850fe560b293
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188748"
---
# <span data-ttu-id="07572-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="07572-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="07572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07572-102">SYNOPSIS</span></span>
<span data-ttu-id="07572-103">Azure Synapse Analytics 작업 영역의 감사 설정을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="07572-104">구문</span><span class="sxs-lookup"><span data-stu-id="07572-104">SYNTAX</span></span>

### <span data-ttu-id="07572-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="07572-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07572-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07572-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07572-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07572-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07572-108">설명</span><span class="sxs-lookup"><span data-stu-id="07572-108">DESCRIPTION</span></span>
<span data-ttu-id="07572-109">**Set-AzSynapseSqlAuditSetting** cmdlet은 Azure Synapse 분석 작업 영역의 감사 설정을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="07572-110">Blob Storage가 감사 로그의 대상인 경우 *StorageAccountResourceId* 매개 변수를 지정하여 감사 로그에 대한 스토리지 계정 및 스토리지 키를 정의하는 *StorageKeyType* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="07572-111">*RetentionInDays* 매개 변수의 값을 설정하여 감사 로그에 대한 기간을 정의하여 감사 로그에 대한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07572-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="07572-112">예제</span><span class="sxs-lookup"><span data-stu-id="07572-112">EXAMPLES</span></span>

### <span data-ttu-id="07572-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="07572-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="07572-114">ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 Blob Storage 감사 정책을 사용하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07572-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="07572-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="07572-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="07572-116">ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 Blob Storage 감사 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="07572-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="07572-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="07572-118">T-SQL 사용하여 고급 필터링을 통해 ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 Blob Storage 감사 정책을 사용하도록 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="07572-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="07572-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="07572-120">ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 감사 정책에서 고급 필터링 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="07572-121">예제 5</span><span class="sxs-lookup"><span data-stu-id="07572-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="07572-122">파이프라인을 통해 ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 Blob Storage 감사 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="07572-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07572-123">PARAMETERS</span></span>

### <span data-ttu-id="07572-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07572-124">-AsJob</span></span>
<span data-ttu-id="07572-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="07572-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07572-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="07572-126">-AuditActionGroup</span></span>
<span data-ttu-id="07572-127">권장되는 작업 그룹 집합은 다음과 같은 조합입니다. 데이터베이스에 대해 실행되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패한 로그인을 감사합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="07572-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="07572-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="07572-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="07572-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="07572-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="07572-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="07572-131">위의 조합은 기본적으로 구성된 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="07572-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="07572-132">이러한 그룹은 데이터베이스에 대해 SQL 모든 명령문 및 저장 프로시저를 다루며, 중복 감사 로그를 생성하기 때문에 다른 그룹과 함께 사용되지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="07572-133">자세한 내용은 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07572-133">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="07572-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="07572-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="07572-135">Blob Storage가 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="07572-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="07572-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07572-136">-DefaultProfile</span></span>
<span data-ttu-id="07572-137">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07572-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07572-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07572-138">-InputObject</span></span>
<span data-ttu-id="07572-139">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="07572-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07572-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07572-140">-PassThru</span></span>
<span data-ttu-id="07572-141">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07572-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="07572-142">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="07572-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="07572-143">-PredicateExpression</span></span>
<span data-ttu-id="07572-144">감사 SQL 데 사용되는 T-SQL(WHERE 절)입니다.</span><span class="sxs-lookup"><span data-stu-id="07572-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="07572-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07572-145">-ResourceGroupName</span></span>
<span data-ttu-id="07572-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07572-146">Resource group name.</span></span>

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

### <span data-ttu-id="07572-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07572-147">-ResourceId</span></span>
<span data-ttu-id="07572-148">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="07572-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="07572-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="07572-149">-RetentionInDays</span></span>
<span data-ttu-id="07572-150">감사 로그에 대한 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="07572-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="07572-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="07572-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="07572-152">저장소 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="07572-152">The storage account resource id</span></span>

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

### <span data-ttu-id="07572-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="07572-153">-StorageKeyType</span></span>
<span data-ttu-id="07572-154">사용할 저장소 액세스 키 중 어느 것이 필요한지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="07572-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07572-155">-WorkspaceName</span></span>
<span data-ttu-id="07572-156">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07572-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="07572-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07572-157">-Confirm</span></span>
<span data-ttu-id="07572-158">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07572-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07572-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07572-159">-WhatIf</span></span>
<span data-ttu-id="07572-160">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="07572-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07572-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07572-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07572-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07572-162">CommonParameters</span></span>
<span data-ttu-id="07572-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07572-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07572-164">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="07572-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07572-165">입력</span><span class="sxs-lookup"><span data-stu-id="07572-165">INPUTS</span></span>

### <span data-ttu-id="07572-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="07572-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="07572-167">출력</span><span class="sxs-lookup"><span data-stu-id="07572-167">OUTPUTS</span></span>

### <span data-ttu-id="07572-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="07572-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="07572-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07572-169">NOTES</span></span>

## <span data-ttu-id="07572-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07572-170">RELATED LINKS</span></span>
