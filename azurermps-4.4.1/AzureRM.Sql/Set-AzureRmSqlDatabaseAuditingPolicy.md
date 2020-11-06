---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527196"
---
# <span data-ttu-id="3e622-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="3e622-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="3e622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e622-102">SYNOPSIS</span></span>
<span data-ttu-id="3e622-103">데이터베이스에 대 한 감사 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e622-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e622-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e622-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3e622-105">DESCRIPTION</span></span>
<span data-ttu-id="3e622-106">**AzureRmSqlDatabaseAuditingPolicy** Cmdlet은 Azure SQL 데이터베이스의 감사 정책을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="3e622-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="3e622-108">저장소 키를 정의 하는 감사 로그 및 *Storageaccountname* 매개 변수에 대 한 저장소 계정을 지정 하는 *storageaccountname* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="3e622-109">보존 *기간 및* *tableidentifier* 매개 변수 값을 설정 하 여 감사 로그 테이블 이름에 대 한 기간과 시드를 정의 하는 감사 로그 테이블에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="3e622-110">*EventType* 매개 변수를 지정 하 여 감사할 이벤트 유형을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="3e622-111">Cmdlet이 성공적으로 실행 되 면 데이터베이스 감사를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="3e622-112">이 cmdlet을 실행 하기 전에 데이터베이스에서 감사에 대 한 서버 정책을 사용 하는 경우 감사가 해당 정책의 사용을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-112">If the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span>
<span data-ttu-id="3e622-113">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 데이터베이스 식별자 외에도 현재 감사 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-113">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="3e622-114">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-114">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="3e622-115">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-115">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3e622-116">예제의</span><span class="sxs-lookup"><span data-stu-id="3e622-116">EXAMPLES</span></span>

### <span data-ttu-id="3e622-117">예제 1: 테이블 감사를 사용 하도록 데이터베이스의 감사 정책 설정</span><span class="sxs-lookup"><span data-stu-id="3e622-117">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="3e622-118">이 명령은 Storage31 이라는 저장소 계정을 사용 하도록 Server01에 있는 Database01 이라는 데이터베이스의 감사 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-118">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="3e622-119">예제 2: 데이터베이스의 기존 감사 정책의 저장소 계정 키 설정</span><span class="sxs-lookup"><span data-stu-id="3e622-119">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="3e622-120">이 명령은 Server01에 있는 Database01 이라는 데이터베이스의 감사 정책을 설정 하 여 동일한 저장소 계정 이름을 계속 사용 하지만 이제 보조 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-120">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="3e622-121">예제 3: 특정 이벤트 유형을 사용 하도록 데이터베이스의 감사 정책 설정</span><span class="sxs-lookup"><span data-stu-id="3e622-121">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="3e622-122">예제 4: Blob 감사를 사용 하도록 데이터베이스의 감사 정책 설정</span><span class="sxs-lookup"><span data-stu-id="3e622-122">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="3e622-123">이 명령은 Server01에 있는 Database01 이라는 데이터베이스의 감사 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-123">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="3e622-124">정책은 Login_Failure 이벤트 유형을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-124">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="3e622-125">이 명령은 저장소 설정을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-125">The command does not change the storage settings.</span></span>

## <span data-ttu-id="3e622-126">변수</span><span class="sxs-lookup"><span data-stu-id="3e622-126">PARAMETERS</span></span>

### <span data-ttu-id="3e622-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="3e622-127">-AuditAction</span></span>
<span data-ttu-id="3e622-128">하나 이상의 감사 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-128">Specify one or more audit actions.</span></span>
<span data-ttu-id="3e622-129">이 매개 변수는 Blob 감사에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-129">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="3e622-130">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="3e622-130">-AuditActionGroup</span></span>
<span data-ttu-id="3e622-131">하나 이상의 감사 작업 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-131">Specify one or more audit action groups.</span></span>
<span data-ttu-id="3e622-132">이 매개 변수는 Blob 감사에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-132">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="3e622-133">-AuditType</span><span class="sxs-lookup"><span data-stu-id="3e622-133">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e622-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e622-134">-DatabaseName</span></span>
<span data-ttu-id="3e622-135">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-135">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e622-136">-EventType</span><span class="sxs-lookup"><span data-stu-id="3e622-136">-EventType</span></span>
<span data-ttu-id="3e622-137">감사할 이벤트 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-137">Specifies the event types to audit.</span></span>
<span data-ttu-id="3e622-138">이 매개 변수는 테이블 감사에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-138">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="3e622-139">여러 이벤트 유형을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-139">You can specify several event types.</span></span>
<span data-ttu-id="3e622-140">모든 이벤트 유형을 감사 하도록 All을 지정 하거나 없음으로 이벤트 감사를 지정 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-140">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="3e622-141">모두 또는 모두를 동시에 지정 하는 경우에는 cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-141">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e622-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e622-142">-PassThru</span></span>
<span data-ttu-id="3e622-143">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3e622-144">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e622-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e622-145">-ResourceGroupName</span></span>
<span data-ttu-id="3e622-146">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-146">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3e622-147">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="3e622-147">-RetentionInDays</span></span>
<span data-ttu-id="3e622-148">감사 로그 테이블의 보존 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-148">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="3e622-149">값이 0 이면 테이블이 보존 되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-149">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="3e622-150">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-150">The default value is zero.</span></span>
<span data-ttu-id="3e622-151">0 보다 큰 값을 지정 하는 경우 *Tableidentifer* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-151">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="3e622-152">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3e622-152">-ServerName</span></span>
<span data-ttu-id="3e622-153">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-153">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3e622-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e622-154">-StorageAccountName</span></span>
<span data-ttu-id="3e622-155">데이터베이스 감사를 위한 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-155">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="3e622-156">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-156">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="3e622-157">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-157">This parameter is not required.</span></span>
<span data-ttu-id="3e622-158">이 매개 변수를 지정 하지 않으면 이전에 데이터베이스의 감사 정책 일부로 정의한 저장소 계정이 cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-158">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="3e622-159">데이터베이스 감사 정책을 처음 정의 하 고이 매개 변수를 지정 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-159">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="3e622-160">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3e622-160">-StorageKeyType</span></span>
<span data-ttu-id="3e622-161">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-161">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="3e622-162">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3e622-163">주요한</span><span class="sxs-lookup"><span data-stu-id="3e622-163">Primary</span></span>
- <span data-ttu-id="3e622-164">보조</span><span class="sxs-lookup"><span data-stu-id="3e622-164">Secondary</span></span>

<span data-ttu-id="3e622-165">기본값은 기본 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-165">The default value is Primary.</span></span>

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

### <span data-ttu-id="3e622-166">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="3e622-166">-TableIdentifier</span></span>
<span data-ttu-id="3e622-167">감사 로그 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-167">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="3e622-168">*보존 기간* 매개 변수에 대해 0 보다 큰 값을 지정 하는 경우이 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-168">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="3e622-169">-확인</span><span class="sxs-lookup"><span data-stu-id="3e622-169">-Confirm</span></span>
<span data-ttu-id="3e622-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e622-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e622-171">-WhatIf</span></span>
<span data-ttu-id="3e622-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e622-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e622-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e622-174">-DefaultProfile</span></span>
<span data-ttu-id="3e622-175">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e622-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e622-176">CommonParameters</span></span>
<span data-ttu-id="3e622-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e622-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e622-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e622-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e622-179">입력</span><span class="sxs-lookup"><span data-stu-id="3e622-179">INPUTS</span></span>

## <span data-ttu-id="3e622-180">출력</span><span class="sxs-lookup"><span data-stu-id="3e622-180">OUTPUTS</span></span>

### <span data-ttu-id="3e622-181">Microsoft. \*. \* DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3e622-181">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="3e622-182">상속자</span><span class="sxs-lookup"><span data-stu-id="3e622-182">NOTES</span></span>

## <span data-ttu-id="3e622-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e622-183">RELATED LINKS</span></span>

[<span data-ttu-id="3e622-184">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="3e622-184">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="3e622-185">제거-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="3e622-185">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="3e622-186">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="3e622-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


