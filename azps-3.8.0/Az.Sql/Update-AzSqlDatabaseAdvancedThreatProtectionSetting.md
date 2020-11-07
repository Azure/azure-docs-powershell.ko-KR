---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878710"
---
# <span data-ttu-id="9ef77-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9ef77-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="9ef77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ef77-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef77-103">데이터베이스에 고급 위협 보호 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="9ef77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ef77-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ef77-105">DESCRIPTION</span></span>
<span data-ttu-id="9ef77-106">**AzSqlDatabaseAdvancedThreatProtectionSetting** Cmdlet은 Azure SQL 데이터베이스에서 고급 위협 방지 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="9ef77-107">데이터베이스에서 고급 위협 보호를 사용 하도록 설정 하려면 해당 데이터베이스에 대 한 감사 설정을 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="9ef77-108">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 지정 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9ef77-109">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9ef77-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9ef77-110">EXAMPLES</span></span>

### <span data-ttu-id="9ef77-111">예제 1: 데이터베이스에 대 한 고급 위협 보호 설정 설정</span><span class="sxs-lookup"><span data-stu-id="9ef77-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="9ef77-112">이 명령은 Server01 라는 서버의 Database01 이라는 데이터베이스에 대 한 고급 위협 보호 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="9ef77-113">변수</span><span class="sxs-lookup"><span data-stu-id="9ef77-113">PARAMETERS</span></span>

### <span data-ttu-id="9ef77-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9ef77-114">-DatabaseName</span></span>
<span data-ttu-id="9ef77-115">설정이 설정 된 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="9ef77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef77-116">-DefaultProfile</span></span>
<span data-ttu-id="9ef77-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9ef77-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ef77-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="9ef77-118">-EmailAdmins</span></span>
<span data-ttu-id="9ef77-119">고급 위협 방지 설정이 전자 메일을 사용 하 여 관리자에 게 연락 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="9ef77-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="9ef77-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="9ef77-121">설정에서 제외할 검색 유형의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="9ef77-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ef77-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="9ef77-123">Sql_Injection</span></span> 
- <span data-ttu-id="9ef77-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="9ef77-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="9ef77-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="9ef77-125">Access_Anomaly</span></span> 
- <span data-ttu-id="9ef77-126">않아야</span><span class="sxs-lookup"><span data-stu-id="9ef77-126">None</span></span>

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

### <span data-ttu-id="9ef77-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="9ef77-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="9ef77-128">설정이 알림을 보내는 세미콜론으로 구분 된 전자 메일 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="9ef77-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ef77-129">-PassThru</span></span>
<span data-ttu-id="9ef77-130">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ef77-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ef77-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef77-132">-ResourceGroupName</span></span>
<span data-ttu-id="9ef77-133">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9ef77-134">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="9ef77-134">-RetentionInDays</span></span>
<span data-ttu-id="9ef77-135">감사 로그 보존 일 수</span><span class="sxs-lookup"><span data-stu-id="9ef77-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="9ef77-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9ef77-136">-ServerName</span></span>
<span data-ttu-id="9ef77-137">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9ef77-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9ef77-138">-StorageAccountName</span></span>
<span data-ttu-id="9ef77-139">사용할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="9ef77-140">와일드 카드는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-140">Wildcards are not permitted.</span></span> <span data-ttu-id="9ef77-141">이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-141">This parameter is not required.</span></span> <span data-ttu-id="9ef77-142">이 매개 변수를 제공 하지 않으면 cmdlet은 이전에 데이터베이스의 고급 위협 보호 설정의 일부로 정의 된 저장소 계정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="9ef77-143">데이터베이스 고급 위협 방지 설정을 처음 정의 하 고이 매개 변수를 제공 하지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="9ef77-144">-확인</span><span class="sxs-lookup"><span data-stu-id="9ef77-144">-Confirm</span></span>
<span data-ttu-id="9ef77-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef77-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef77-146">-WhatIf</span></span>
<span data-ttu-id="9ef77-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef77-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef77-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef77-149">CommonParameters</span></span>
<span data-ttu-id="9ef77-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ef77-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef77-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ef77-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef77-152">입력</span><span class="sxs-lookup"><span data-stu-id="9ef77-152">INPUTS</span></span>

### <span data-ttu-id="9ef77-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ef77-153">System.String</span></span>

### <span data-ttu-id="9ef77-154">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9ef77-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9ef77-155">ThreatDetection. DetectionType []/. \*</span><span class="sxs-lookup"><span data-stu-id="9ef77-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="9ef77-156">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9ef77-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9ef77-157">출력</span><span class="sxs-lookup"><span data-stu-id="9ef77-157">OUTPUTS</span></span>

### <span data-ttu-id="9ef77-158">ThreatDetection. DatabaseThreatDetectionsettingsModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="9ef77-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="9ef77-159">상속자</span><span class="sxs-lookup"><span data-stu-id="9ef77-159">NOTES</span></span>

## <span data-ttu-id="9ef77-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ef77-160">RELATED LINKS</span></span>

[<span data-ttu-id="9ef77-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="9ef77-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="9ef77-162">제거-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="9ef77-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="9ef77-163">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9ef77-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


