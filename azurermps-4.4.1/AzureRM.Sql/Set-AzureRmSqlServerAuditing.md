---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531799"
---
# <span data-ttu-id="f691e-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="f691e-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="f691e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f691e-102">SYNOPSIS</span></span>
<span data-ttu-id="f691e-103">Azure SQL server의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f691e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f691e-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f691e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f691e-105">DESCRIPTION</span></span>
<span data-ttu-id="f691e-106">**AzureRmSqlServerAuditing** Cmdlet은 Azure SQL server의 감사 설정을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="f691e-107">Cmdlet을 사용 하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 사용 하 여 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="f691e-108">저장소 키를 정의 하는 감사 로그 및 *Storageaccountname* 매개 변수에 대 한 저장소 계정을 지정 하는 *storageaccountname* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="f691e-109">*State* 매개 변수를 사용 하 여 정책을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="f691e-110">*보존 기간 매개 변수* 값을 설정 하 여 감사 로그에 대 한 주기를 정의 하 여 감사 로그에 대 한 보존을 정의할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="f691e-111">Cmdlet이 성공적으로 실행 되 면 지정 된 Azure SQL server에 정의 된 Azure SQL 데이터베이스의 감사가 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="f691e-112">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 서버 식별자 외에도 현재 blob 감사 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="f691e-113">서버 식별자에는 **ResourceGroupName** 및 **ServerName** 이 포함 되지만이에 국한 되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="f691e-114">예제의</span><span class="sxs-lookup"><span data-stu-id="f691e-114">EXAMPLES</span></span>

### <span data-ttu-id="f691e-115">예제 1: Azure SQL server의 감사 정책 사용</span><span class="sxs-lookup"><span data-stu-id="f691e-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="f691e-116">예제 2: Azure SQL server의 감사 정책 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="f691e-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="f691e-117">변수</span><span class="sxs-lookup"><span data-stu-id="f691e-117">PARAMETERS</span></span>

### <span data-ttu-id="f691e-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f691e-118">-AuditActionGroup</span></span>
<span data-ttu-id="f691e-119">감사 작업 그룹 집합</span><span class="sxs-lookup"><span data-stu-id="f691e-119">The set of the audit action groups</span></span>

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

### <span data-ttu-id="f691e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f691e-120">-PassThru</span></span>
<span data-ttu-id="f691e-121">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="f691e-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f691e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f691e-122">-ResourceGroupName</span></span>
<span data-ttu-id="f691e-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f691e-124">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="f691e-124">-RetentionInDays</span></span>
<span data-ttu-id="f691e-125">감사 로그 보존 일 수</span><span class="sxs-lookup"><span data-stu-id="f691e-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="f691e-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f691e-126">-ServerName</span></span>
<span data-ttu-id="f691e-127">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-127">SQL server name.</span></span>

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

### <span data-ttu-id="f691e-128">-상태</span><span class="sxs-lookup"><span data-stu-id="f691e-128">-State</span></span>
<span data-ttu-id="f691e-129">감사 정책의 상태</span><span class="sxs-lookup"><span data-stu-id="f691e-129">The state of the auditing policy</span></span>

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

### <span data-ttu-id="f691e-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f691e-130">-StorageAccountName</span></span>
<span data-ttu-id="f691e-131">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-131">The name of the storage account</span></span>

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

### <span data-ttu-id="f691e-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f691e-132">-StorageKeyType</span></span>
<span data-ttu-id="f691e-133">저장소 키의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-133">The type of the storage key</span></span>

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

### <span data-ttu-id="f691e-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f691e-134">-Confirm</span></span>
<span data-ttu-id="f691e-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f691e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f691e-136">-WhatIf</span></span>
<span data-ttu-id="f691e-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f691e-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f691e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f691e-139">-DefaultProfile</span></span>
<span data-ttu-id="f691e-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f691e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f691e-141">CommonParameters</span></span>
<span data-ttu-id="f691e-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f691e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f691e-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f691e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f691e-144">입력</span><span class="sxs-lookup"><span data-stu-id="f691e-144">INPUTS</span></span>

## <span data-ttu-id="f691e-145">출력</span><span class="sxs-lookup"><span data-stu-id="f691e-145">OUTPUTS</span></span>

### <span data-ttu-id="f691e-146">Microsoft. Test.sql. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="f691e-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="f691e-147">상속자</span><span class="sxs-lookup"><span data-stu-id="f691e-147">NOTES</span></span>

## <span data-ttu-id="f691e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f691e-148">RELATED LINKS</span></span>

