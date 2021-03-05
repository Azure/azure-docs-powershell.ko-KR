---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9677f45e772cbcb48190f5792df97e96051180c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992273"
---
# <span data-ttu-id="e1e58-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e1e58-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="e1e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1e58-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e58-103">데이터베이스에 대한 고급 위협 보호 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="e1e58-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1e58-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1e58-105">설명</span><span class="sxs-lookup"><span data-stu-id="e1e58-105">DESCRIPTION</span></span>
<span data-ttu-id="e1e58-106">**Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet은 Azure SQL 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="e1e58-107">데이터베이스에서 고급 위협 보호를 사용하도록 설정하려면 해당 데이터베이스에서 감사 설정을 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="e1e58-108">이 cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 지정하여 데이터베이스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e1e58-109">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e1e58-110">예제</span><span class="sxs-lookup"><span data-stu-id="e1e58-110">EXAMPLES</span></span>

### <span data-ttu-id="e1e58-111">예제 1: 데이터베이스에 대한 고급 위협 보호 설정 설정</span><span class="sxs-lookup"><span data-stu-id="e1e58-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e1e58-112">이 명령은 Server01이라는 서버에서 Database01이라는 데이터베이스에 대한 고급 위협 보호 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="e1e58-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1e58-113">PARAMETERS</span></span>

### <span data-ttu-id="e1e58-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1e58-114">-DatabaseName</span></span>
<span data-ttu-id="e1e58-115">설정이 설정된 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="e1e58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e58-116">-DefaultProfile</span></span>
<span data-ttu-id="e1e58-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e1e58-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1e58-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e1e58-118">-EmailAdmins</span></span>
<span data-ttu-id="e1e58-119">고급 위협 보호 설정이 전자 메일을 사용하여 관리자와 접촉하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1e58-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e1e58-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="e1e58-121">설정에서 제외할 검색 형식 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="e1e58-122">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1e58-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e1e58-123">Sql_Injection</span></span> 
- <span data-ttu-id="e1e58-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e1e58-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="e1e58-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e1e58-125">Access_Anomaly</span></span> 
- <span data-ttu-id="e1e58-126">없음</span><span class="sxs-lookup"><span data-stu-id="e1e58-126">None</span></span>

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

### <span data-ttu-id="e1e58-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e1e58-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e1e58-128">설정에서 경고를 보내는 세미코론으로 구분된 전자 메일 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="e1e58-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1e58-129">-PassThru</span></span>
<span data-ttu-id="e1e58-130">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1e58-131">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1e58-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1e58-132">-ResourceGroupName</span></span>
<span data-ttu-id="e1e58-133">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e1e58-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e1e58-134">-RetentionInDays</span></span>
<span data-ttu-id="e1e58-135">감사 로그에 대한 보존 일 수</span><span class="sxs-lookup"><span data-stu-id="e1e58-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="e1e58-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e1e58-136">-ServerName</span></span>
<span data-ttu-id="e1e58-137">서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e1e58-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e1e58-138">-StorageAccountName</span></span>
<span data-ttu-id="e1e58-139">사용할 저장소 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e1e58-140">와일드카드는 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-140">Wildcards are not permitted.</span></span> <span data-ttu-id="e1e58-141">이 매개 변수는 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-141">This parameter is not required.</span></span> <span data-ttu-id="e1e58-142">이 매개 변수가 제공되지 않은 경우 cmdlet은 데이터베이스의 고급 위협 보호 설정의 일부로 이전에 정의된 저장소 계정을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="e1e58-143">데이터베이스 고급 위협 보호 설정이 처음으로 정의되고 이 매개 변수가 제공되지 않는 경우 cmdlet이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e1e58-144">-확인</span><span class="sxs-lookup"><span data-stu-id="e1e58-144">-Confirm</span></span>
<span data-ttu-id="e1e58-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1e58-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1e58-146">-WhatIf</span></span>
<span data-ttu-id="e1e58-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1e58-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1e58-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e58-149">CommonParameters</span></span>
<span data-ttu-id="e1e58-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1e58-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e58-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1e58-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e58-152">입력</span><span class="sxs-lookup"><span data-stu-id="e1e58-152">INPUTS</span></span>

### <span data-ttu-id="e1e58-153">System.String</span><span class="sxs-lookup"><span data-stu-id="e1e58-153">System.String</span></span>

### <span data-ttu-id="e1e58-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1e58-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e1e58-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="e1e58-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="e1e58-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1e58-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e1e58-157">출력</span><span class="sxs-lookup"><span data-stu-id="e1e58-157">OUTPUTS</span></span>

### <span data-ttu-id="e1e58-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="e1e58-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="e1e58-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1e58-159">NOTES</span></span>

## <span data-ttu-id="e1e58-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1e58-160">RELATED LINKS</span></span>

[<span data-ttu-id="e1e58-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="e1e58-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="e1e58-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="e1e58-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="e1e58-163">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="e1e58-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


