---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: dd3c54b8e2769e1b7643d154b259b4f47fd51f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702441"
---
# <span data-ttu-id="0aaf5-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0aaf5-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="0aaf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aaf5-102">SYNOPSIS</span></span>
<span data-ttu-id="0aaf5-103">SQL 데이터베이스 서버의 감사 정책을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aaf5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0aaf5-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aaf5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0aaf5-105">DESCRIPTION</span></span>
<span data-ttu-id="0aaf5-106">**AzureRmSqlServerAuditingPolicy** Cmdlet은 Azure SQL 데이터베이스 서버의 감사 정책을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="0aaf5-107">*ResourceGroupName* 및 *ServerName* 매개 변수를 지정 하 여 서버를 식별 하 고, *storageaccountname* 매개 변수를 감사 로그에 대 한 저장소 계정을 지정 하 고, *storageaccountname* 매개 변수를 사용 하 여 사용할 저장소 키를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>
<span data-ttu-id="0aaf5-108">보존 *기간 및* *tableidentifier* 매개 변수 값을 설정 하 여 감사 로그 테이블 이름에 대 한 기간과 시드를 정의 하는 감사 로그 테이블에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="0aaf5-109">*EventType* 매개 변수를 지정 하 여 감사할 이벤트 유형을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="0aaf5-110">이 cmdlet을 실행 한 후에는이 서버의 정책을 사용 하는 데이터베이스의 감사를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="0aaf5-111">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 지정 하면 cmdlet은 현재 감사 정책 및 서버 식별자를 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="0aaf5-112">서버 식별자에는 **ResourceGroupName** 및 **ServerName** 이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="0aaf5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="0aaf5-113">EXAMPLES</span></span>

### <span data-ttu-id="0aaf5-114">예제 1: Azure SQL server의 감사 정책 설정 테이블 감사 사용</span><span class="sxs-lookup"><span data-stu-id="0aaf5-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="0aaf5-115">이 명령은 Server01 이라는 서버의 감사 정책을 Storage22 이라는 저장소 계정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="0aaf5-116">예제 2: Azure SQL server의 기존 감사 정책의 저장소 계정 키 설정</span><span class="sxs-lookup"><span data-stu-id="0aaf5-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="0aaf5-117">이 명령은 Server01 이라는 서버의 감사 정책을 보조 키를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="0aaf5-118">이 명령은 저장소 계정 이름을 수정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="0aaf5-119">예제 3: 특정 이벤트 유형을 사용 하도록 Azure SQL server의 감사 정책 설정</span><span class="sxs-lookup"><span data-stu-id="0aaf5-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="0aaf5-120">예제 4: Blob 감사를 사용 하도록 데이터베이스의 감사 정책 설정</span><span class="sxs-lookup"><span data-stu-id="0aaf5-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="0aaf5-121">이 명령은 Server01 이라는 서버의 감사 정책을 설정 하 여 Login_Failure 이벤트 유형을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="0aaf5-122">이 명령은 다른 설정을 수정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="0aaf5-123">변수</span><span class="sxs-lookup"><span data-stu-id="0aaf5-123">PARAMETERS</span></span>

### <span data-ttu-id="0aaf5-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="0aaf5-124">-AuditActionGroup</span></span>
<span data-ttu-id="0aaf5-125">하나 이상의 감사 작업 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="0aaf5-126">이 매개 변수는 Blob 감사에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="0aaf5-127">-AuditType</span><span class="sxs-lookup"><span data-stu-id="0aaf5-127">-AuditType</span></span>
<span data-ttu-id="0aaf5-128">감사 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-128">Specify the audit type.</span></span> <span data-ttu-id="0aaf5-129">감사 로그를 테이블 저장소 또는 Blob 저장소에 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="0aaf5-130">Blob 감사는 성능을 향상 하 고 개체 수준 감사를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

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

### <span data-ttu-id="0aaf5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aaf5-131">-DefaultProfile</span></span>
<span data-ttu-id="0aaf5-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0aaf5-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0aaf5-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="0aaf5-133">-EventType</span></span>
<span data-ttu-id="0aaf5-134">감사할 이벤트 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="0aaf5-135">이 매개 변수는 테이블 감사에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-135">This parameter is only applicable to Table auditing.</span></span>
<span data-ttu-id="0aaf5-136">여러 이벤트 유형을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-136">You can specify several event types.</span></span>
<span data-ttu-id="0aaf5-137">모든 이벤트 유형을 감사 하도록 All을 지정 하거나 없음으로 이벤트 감사를 지정 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="0aaf5-138">모두 또는 모두를 동시에 지정 하지 않으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-138">If you specify All or None at the same time, the command fails.</span></span>

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

### <span data-ttu-id="0aaf5-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0aaf5-139">-PassThru</span></span>
<span data-ttu-id="0aaf5-140">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0aaf5-141">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0aaf5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aaf5-142">-ResourceGroupName</span></span>
<span data-ttu-id="0aaf5-143">데이터베이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="0aaf5-144">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="0aaf5-144">-RetentionInDays</span></span>
<span data-ttu-id="0aaf5-145">감사 로그 테이블의 보존 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="0aaf5-146">값이 0 이면 테이블이 보존 되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="0aaf5-147">이는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-147">this is the default.</span></span>
<span data-ttu-id="0aaf5-148">0 보다 큰 값을 지정 하는 경우 *Tableidentifer* 매개 변수에 대 한 값도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="0aaf5-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0aaf5-149">-ServerName</span></span>
<span data-ttu-id="0aaf5-150">데이터베이스를 포함 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aaf5-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0aaf5-151">-StorageAccountName</span></span>
<span data-ttu-id="0aaf5-152">데이터베이스 감사를 위한 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="0aaf5-153">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="0aaf5-154">이 매개 변수를 지정 하지 않으면 이전에 데이터베이스의 감사 정책 일부로 정의한 저장소 계정이 cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="0aaf5-155">데이터베이스 감사 정책을 처음 정의 하 고이 매개 변수를 지정 하지 않으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="0aaf5-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="0aaf5-156">-StorageKeyType</span></span>
<span data-ttu-id="0aaf5-157">사용할 저장소 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="0aaf5-158">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0aaf5-159">주요한</span><span class="sxs-lookup"><span data-stu-id="0aaf5-159">Primary</span></span>
- <span data-ttu-id="0aaf5-160">보조 기본값은 기본 값입니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-160">Secondary The default value is Primary.</span></span>

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

### <span data-ttu-id="0aaf5-161">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="0aaf5-161">-TableIdentifier</span></span>
<span data-ttu-id="0aaf5-162">감사 로그 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-162">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="0aaf5-163">*보존 기간* 매개 변수에 대해 0 보다 큰 값을 지정 하는 경우이 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-163">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="0aaf5-164">-확인</span><span class="sxs-lookup"><span data-stu-id="0aaf5-164">-Confirm</span></span>
<span data-ttu-id="0aaf5-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aaf5-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aaf5-166">-WhatIf</span></span>
<span data-ttu-id="0aaf5-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aaf5-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aaf5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aaf5-169">CommonParameters</span></span>
<span data-ttu-id="0aaf5-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aaf5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aaf5-171">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aaf5-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aaf5-172">입력</span><span class="sxs-lookup"><span data-stu-id="0aaf5-172">INPUTS</span></span>

### <span data-ttu-id="0aaf5-173">Microsoft. Azure. 감사. AuditType</span><span class="sxs-lookup"><span data-stu-id="0aaf5-173">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType</span></span>

### <span data-ttu-id="0aaf5-174">Microsoft. Test.sql. 감사. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="0aaf5-174">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="0aaf5-175">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="0aaf5-175">System.String[]</span></span>

### <span data-ttu-id="0aaf5-176">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0aaf5-176">System.String</span></span>

### <span data-ttu-id="0aaf5-177">시스템 Null 허용 ' 1 [[시스템. UInt32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0aaf5-177">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0aaf5-178">출력</span><span class="sxs-lookup"><span data-stu-id="0aaf5-178">OUTPUTS</span></span>

### <span data-ttu-id="0aaf5-179">Microsoft. Test.sql. 감사 합니다. Model-AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0aaf5-179">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="0aaf5-180">상속자</span><span class="sxs-lookup"><span data-stu-id="0aaf5-180">NOTES</span></span>

## <span data-ttu-id="0aaf5-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0aaf5-181">RELATED LINKS</span></span>

[<span data-ttu-id="0aaf5-182">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0aaf5-182">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="0aaf5-183">-AzureRmSqlServerAuditingPolicy 사용</span><span class="sxs-lookup"><span data-stu-id="0aaf5-183">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="0aaf5-184">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="0aaf5-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


