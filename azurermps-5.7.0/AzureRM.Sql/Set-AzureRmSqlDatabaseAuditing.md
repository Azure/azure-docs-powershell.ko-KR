---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528753"
---
# <span data-ttu-id="42b74-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="42b74-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="42b74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42b74-102">SYNOPSIS</span></span>
<span data-ttu-id="42b74-103">Azure SQL 데이터베이스에 대 한 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42b74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42b74-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42b74-105">설명은</span><span class="sxs-lookup"><span data-stu-id="42b74-105">DESCRIPTION</span></span>
<span data-ttu-id="42b74-106">**AzureRmSqlDatabaseAuditing** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="42b74-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="42b74-108">저장소 키를 정의 하는 감사 로그 및 *Storageaccountname* 매개 변수에 대 한 저장소 계정을 지정 하는 *storageaccountname* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="42b74-109">*State* 매개 변수를 사용 하 여 정책을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="42b74-110">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="42b74-111">Cmdlet이 성공적으로 실행 되 면 데이터베이스 감사를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="42b74-112">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 데이터베이스 식별자 외에도 현재 blob 감사 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="42b74-113">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="42b74-114">예제의</span><span class="sxs-lookup"><span data-stu-id="42b74-114">EXAMPLES</span></span>

### <span data-ttu-id="42b74-115">예제 1: Azure SQL 데이터베이스의 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="42b74-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="42b74-116">예제 2: Azure SQL 데이터베이스의 blob 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="42b74-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="42b74-117">변수</span><span class="sxs-lookup"><span data-stu-id="42b74-117">PARAMETERS</span></span>

### <span data-ttu-id="42b74-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="42b74-118">-AuditAction</span></span>
<span data-ttu-id="42b74-119">감사 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-119">The set of audit actions.</span></span>  
<span data-ttu-id="42b74-120">감사에 지원 되는 작업은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="42b74-121">클릭</span><span class="sxs-lookup"><span data-stu-id="42b74-121">SELECT</span></span>  
<span data-ttu-id="42b74-122">UPDATE</span><span class="sxs-lookup"><span data-stu-id="42b74-122">UPDATE</span></span>  
<span data-ttu-id="42b74-123">넣으십시오</span><span class="sxs-lookup"><span data-stu-id="42b74-123">INSERT</span></span>  
<span data-ttu-id="42b74-124">삭제</span><span class="sxs-lookup"><span data-stu-id="42b74-124">DELETE</span></span>  
<span data-ttu-id="42b74-125">세기</span><span class="sxs-lookup"><span data-stu-id="42b74-125">EXECUTE</span></span>  
<span data-ttu-id="42b74-126">받기</span><span class="sxs-lookup"><span data-stu-id="42b74-126">RECEIVE</span></span>  
<span data-ttu-id="42b74-127">REFERENCES</span><span class="sxs-lookup"><span data-stu-id="42b74-127">REFERENCES</span></span>  

<span data-ttu-id="42b74-128">감사할 작업을 정의 하는 일반적인 형태는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="42b74-129">함수 [Principal]에의 한 [개체]</span><span class="sxs-lookup"><span data-stu-id="42b74-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="42b74-130">위의 형식에서 [개체]는 테이블, 뷰 또는 저장 프로시저와 같은 개체 또는 전체 데이터베이스 또는 스키마를 참조할 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="42b74-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="42b74-131">두 번째 경우에는 forms 데이터베이스:: [dbname] 및 SCHEMA:: [schemaname]이 각각 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="42b74-132">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="42b74-132">For example:</span></span>  
<span data-ttu-id="42b74-133">공용에서 dbo myTable 선택</span><span class="sxs-lookup"><span data-stu-id="42b74-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="42b74-134">Public을 기준으로 데이터베이스:: myDatabase 선택</span><span class="sxs-lookup"><span data-stu-id="42b74-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="42b74-135">SCHEMA:: mySchema을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="42b74-136">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions 하세요.</span><span class="sxs-lookup"><span data-stu-id="42b74-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="42b74-137">-AuditActionGroup</span></span>
<span data-ttu-id="42b74-138">사용할 권장 되는 작업 그룹 집합은 다음 조합입니다 .이는 데이터베이스에 대해 실행 되는 모든 쿼리 및 저장 프로시저와 성공한 로그인 및 실패 한 로그인을 감사 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="42b74-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="42b74-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="42b74-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="42b74-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="42b74-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="42b74-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="42b74-142">위의 조합은 기본적으로 구성 되는 집합 이기도 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="42b74-143">이러한 그룹은 데이터베이스에 대해 실행 되는 모든 SQL 문과 저장 프로시저를 다루며, 다른 그룹과 함께 사용 하면 중복 감사 로그가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="42b74-144">자세한 내용은을 참조 https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups 하세요.</span><span class="sxs-lookup"><span data-stu-id="42b74-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42b74-145">-DatabaseName</span></span>
<span data-ttu-id="42b74-146">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b74-147">-DefaultProfile</span></span>
<span data-ttu-id="42b74-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42b74-149">-PassThru</span></span>
<span data-ttu-id="42b74-150">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="42b74-150">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b74-151">-ResourceGroupName</span></span>
<span data-ttu-id="42b74-152">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-153">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="42b74-153">-RetentionInDays</span></span>
<span data-ttu-id="42b74-154">감사 로그 보존 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-155">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42b74-155">-ServerName</span></span>
<span data-ttu-id="42b74-156">SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-157">-상태</span><span class="sxs-lookup"><span data-stu-id="42b74-157">-State</span></span>
<span data-ttu-id="42b74-158">정책의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42b74-159">-StorageAccountName</span></span>
<span data-ttu-id="42b74-160">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-160">The name of the storage account.</span></span> <span data-ttu-id="42b74-161">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="42b74-162">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-162">This parameter is not required.</span></span>  
<span data-ttu-id="42b74-163">이 매개 변수를 지정 하지 않으면 이전에 감사 정책의 일부로 정의한 저장소 계정이 cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="42b74-164">감사 정책이 처음 정의 될 때이 매개 변수를 지정 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="42b74-165">-StorageKeyType</span></span>
<span data-ttu-id="42b74-166">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-167">-확인</span><span class="sxs-lookup"><span data-stu-id="42b74-167">-Confirm</span></span>
<span data-ttu-id="42b74-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42b74-169">-WhatIf</span></span>
<span data-ttu-id="42b74-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42b74-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b74-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b74-172">CommonParameters</span></span>
<span data-ttu-id="42b74-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b74-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b74-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b74-175">입력</span><span class="sxs-lookup"><span data-stu-id="42b74-175">INPUTS</span></span>

### <span data-ttu-id="42b74-176">않아야</span><span class="sxs-lookup"><span data-stu-id="42b74-176">None</span></span>
<span data-ttu-id="42b74-177">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42b74-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42b74-178">출력</span><span class="sxs-lookup"><span data-stu-id="42b74-178">OUTPUTS</span></span>

### <span data-ttu-id="42b74-179">Microsoft .Sql. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="42b74-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="42b74-180">상속자</span><span class="sxs-lookup"><span data-stu-id="42b74-180">NOTES</span></span>

## <span data-ttu-id="42b74-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42b74-181">RELATED LINKS</span></span>
