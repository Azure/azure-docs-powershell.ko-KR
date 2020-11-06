---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 80887d1c3cfc91c9eba23f686deac071660cf852
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533247"
---
# <span data-ttu-id="ff35b-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="ff35b-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="ff35b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff35b-102">SYNOPSIS</span></span>
<span data-ttu-id="ff35b-103">Azure SQL server의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff35b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff35b-104">SYNTAX</span></span>

### <span data-ttu-id="ff35b-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff35b-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-PredicateExpression <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff35b-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="ff35b-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff35b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ff35b-107">DESCRIPTION</span></span>
<span data-ttu-id="ff35b-108">**AzureRmSqlServerAuditing** Cmdlet은 Azure SQL server의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-108">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="ff35b-109">Cmdlet을 사용 하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 사용 하 여 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="ff35b-110">저장소 키를 정의 하는 감사 로그 및 *Storageaccountname* 매개 변수에 대 한 저장소 계정을 지정 하는 *storageaccountname* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="ff35b-111">*State* 매개 변수를 사용 하 여 정책을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="ff35b-112">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="ff35b-113">Cmdlet이 성공적으로 실행 되 면 지정 된 Azure SQL server에 정의 된 Azure SQL 데이터베이스의 감사가 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-113">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="ff35b-114">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 서버 식별자 외에도 현재 blob 감사 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="ff35b-115">서버 식별자에는 **ResourceGroupName** 및 **ServerName** 이 포함 되지만이에 국한 되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-115">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="ff35b-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ff35b-116">EXAMPLES</span></span>

### <span data-ttu-id="ff35b-117">예제 1: Azure SQL server의 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="ff35b-117">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="ff35b-118">예제 2: Azure SQL server의 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="ff35b-118">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="ff35b-119">예제 3: 다른 구독의 저장소 계정을 사용 하 여 Azure SQL server의 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="ff35b-119">Example 3: Enable the auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="ff35b-120">예제 4: Azure SQL 데이터베이스의 확장 된 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="ff35b-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="ff35b-121">예제 5: Azure SQL 데이터베이스의 확장 된 감사 정책을 제거 하 고이를 대신 하 여 감사 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="ff35b-122">변수</span><span class="sxs-lookup"><span data-stu-id="ff35b-122">PARAMETERS</span></span>

### <span data-ttu-id="ff35b-123">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="ff35b-123">-AuditActionGroup</span></span>
<span data-ttu-id="ff35b-124">사용할 수 있는 권장 작업 그룹 집합은 다음과 같은 조합입니다 .이는 데이터베이스에 대해 실행 되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 ("BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP")을 감사 하며 위의 조합은 기본적으로 구성 된 집합 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-124">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="ff35b-125">이러한 그룹은 데이터베이스에 대해 실행 되는 모든 SQL 문과 저장 프로시저를 다루며, 다른 그룹과 함께 사용 하면 중복 감사 로그가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-125">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="ff35b-126">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 하세요.</span><span class="sxs-lookup"><span data-stu-id="ff35b-126">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="ff35b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff35b-127">-DefaultProfile</span></span>
<span data-ttu-id="ff35b-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff35b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff35b-129">-PassThru</span></span>
<span data-ttu-id="ff35b-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="ff35b-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ff35b-131">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="ff35b-131">-PredicateExpression</span></span>
<span data-ttu-id="ff35b-132">감사 로그를 필터링 하는 데 사용 되는 Where 절의 문입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-132">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="ff35b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff35b-133">-ResourceGroupName</span></span>
<span data-ttu-id="ff35b-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff35b-135">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="ff35b-135">-RetentionInDays</span></span>
<span data-ttu-id="ff35b-136">감사 로그 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-136">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="ff35b-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ff35b-137">-ServerName</span></span>
<span data-ttu-id="ff35b-138">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-138">SQL server name.</span></span>

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

### <span data-ttu-id="ff35b-139">-상태</span><span class="sxs-lookup"><span data-stu-id="ff35b-139">-State</span></span>
<span data-ttu-id="ff35b-140">정책의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-140">The state of the policy.</span></span>

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

### <span data-ttu-id="ff35b-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff35b-141">-StorageAccountName</span></span>
<span data-ttu-id="ff35b-142">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-142">The name of the storage account.</span></span> <span data-ttu-id="ff35b-143">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-143">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="ff35b-144">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-144">This parameter is not required.</span></span>
<span data-ttu-id="ff35b-145">이 매개 변수를 지정 하지 않으면 이전에 감사 정책의 일부로 정의한 저장소 계정이 cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-145">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="ff35b-146">감사 정책이 처음 정의 될 때이 매개 변수를 지정 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-146">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="ff35b-147">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff35b-147">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="ff35b-148">저장소 계정 구독 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-148">Specifies storage account subscription id</span></span>

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

### <span data-ttu-id="ff35b-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="ff35b-149">-StorageKeyType</span></span>
<span data-ttu-id="ff35b-150">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-150">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="ff35b-151">-확인</span><span class="sxs-lookup"><span data-stu-id="ff35b-151">-Confirm</span></span>
<span data-ttu-id="ff35b-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff35b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff35b-153">-WhatIf</span></span>
<span data-ttu-id="ff35b-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff35b-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff35b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff35b-156">CommonParameters</span></span>
<span data-ttu-id="ff35b-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff35b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff35b-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff35b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff35b-159">입력</span><span class="sxs-lookup"><span data-stu-id="ff35b-159">INPUTS</span></span>

## <span data-ttu-id="ff35b-160">출력</span><span class="sxs-lookup"><span data-stu-id="ff35b-160">OUTPUTS</span></span>

## <span data-ttu-id="ff35b-161">상속자</span><span class="sxs-lookup"><span data-stu-id="ff35b-161">NOTES</span></span>

## <span data-ttu-id="ff35b-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff35b-162">RELATED LINKS</span></span>
