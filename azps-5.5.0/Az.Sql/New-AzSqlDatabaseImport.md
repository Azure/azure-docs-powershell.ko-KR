---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: ab1fcfa9b050f795a464488df51768b95996eb8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188073"
---
# <span data-ttu-id="5c843-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="5c843-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="5c843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c843-102">SYNOPSIS</span></span>
<span data-ttu-id="5c843-103">.bacpac 파일을 가져오고 서버에 새 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="5c843-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c843-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c843-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c843-105">DESCRIPTION</span></span>
<span data-ttu-id="5c843-106">**New-AzSqlDatabaseImport** cmdlet은 Azure 저장소 계정에서 새 Azure SQL 데이터베이스로 bacpac 파일을 가져오습니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="5c843-107">가져오기 데이터베이스 상태 가져오기 요청은 이 요청에 대한 상태 정보를 검색하기 위해 전송될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="5c843-108">예제</span><span class="sxs-lookup"><span data-stu-id="5c843-108">EXAMPLES</span></span>

### <span data-ttu-id="5c843-109">예제 1: bacpac 파일에 대한 가져오기 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="5c843-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="5c843-110">이 명령은 .bacpac을 새 데이터베이스로 가져오는 가져오기 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="5c843-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c843-111">PARAMETERS</span></span>

### <span data-ttu-id="5c843-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="5c843-112">-AdministratorLogin</span></span>
<span data-ttu-id="5c843-113">사용자 지정 관리자의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-113">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="5c843-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="5c843-115">사용자 지정 관리자의 암호를 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="5c843-116">-AuthenticationType</span></span>
<span data-ttu-id="5c843-117">서버에 액세스하는 데 사용되는 인증 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="5c843-118">이 매개 변수는 인증 SQL 설정되어 있는 경우 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="5c843-119">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="5c843-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c843-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="5c843-120">SQL.</span></span>
<span data-ttu-id="5c843-121">SQL 인증을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-121">SQL authentication.</span></span>
<span data-ttu-id="5c843-122">*AdministratorLogin* 및 *AdministratorLoginPassword* 매개 변수를 관리자 SQL 암호로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="5c843-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="5c843-123">ADPassword.</span></span>
<span data-ttu-id="5c843-124">Azure Active Directory 인증.</span><span class="sxs-lookup"><span data-stu-id="5c843-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="5c843-125">*AdministratorLogin 및* *AdministratorLoginPassword를* Azure Active Directory 관리자 사용자 이름 및 암호로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="5c843-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="5c843-126">이 매개 변수는 데이터베이스 V12 SQL 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5c843-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="5c843-128">새로 가져온 데이터베이스에 대한 최대 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c843-129">-DatabaseName</span></span>
<span data-ttu-id="5c843-130">SQL 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-130">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c843-131">-DefaultProfile</span></span>
<span data-ttu-id="5c843-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5c843-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c843-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="5c843-133">-Edition</span></span>
<span data-ttu-id="5c843-134">가져올 새 데이터베이스의 에디션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="5c843-135">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="5c843-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c843-136">프리미엄</span><span class="sxs-lookup"><span data-stu-id="5c843-136">Premium</span></span>
- <span data-ttu-id="5c843-137">기본</span><span class="sxs-lookup"><span data-stu-id="5c843-137">Basic</span></span>
- <span data-ttu-id="5c843-138">표준</span><span class="sxs-lookup"><span data-stu-id="5c843-138">Standard</span></span>
- <span data-ttu-id="5c843-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="5c843-139">DataWarehouse</span></span>
- <span data-ttu-id="5c843-140">무료</span><span class="sxs-lookup"><span data-stu-id="5c843-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical, Hyperscale

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c843-141">-ResourceGroupName</span></span>
<span data-ttu-id="5c843-142">SQL 데이터베이스 서버에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="5c843-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c843-143">-ServerName</span></span>
<span data-ttu-id="5c843-144">SQL 데이터베이스 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="5c843-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5c843-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="5c843-146">Azure SQL Database에 할당할 서비스 목표의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="5c843-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="5c843-148">개인 링크를 만드는 SQL Server 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5c843-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="5c843-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="5c843-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="5c843-150">개인 링크를 만들 저장소 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5c843-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="5c843-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="5c843-151">-StorageKey</span></span>
<span data-ttu-id="5c843-152">저장소 계정에 대한 액세스 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-152">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="5c843-153">-StorageKeyType</span></span>
<span data-ttu-id="5c843-154">저장소 계정에 대한 액세스 키의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="5c843-155">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="5c843-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c843-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="5c843-156">StorageAccessKey.</span></span>
<span data-ttu-id="5c843-157">저장소 계정 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="5c843-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="5c843-158">SharedAccessKey.</span></span>
<span data-ttu-id="5c843-159">SAS(공유 액세스 서명) 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-159">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="5c843-160">-StorageUri</span></span>
<span data-ttu-id="5c843-161">.bacpac 파일의 Blob URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-161">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="5c843-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="5c843-163">설정된 경우 저장소 계정 및/또는 서버용 개인 SQL 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-163">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c843-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c843-164">-Confirm</span></span>
<span data-ttu-id="5c843-165">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c843-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c843-166">-WhatIf</span></span>
<span data-ttu-id="5c843-167">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5c843-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c843-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c843-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c843-169">CommonParameters</span></span>
<span data-ttu-id="5c843-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c843-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c843-171">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c843-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c843-172">입력</span><span class="sxs-lookup"><span data-stu-id="5c843-172">INPUTS</span></span>

### <span data-ttu-id="5c843-173">System.String</span><span class="sxs-lookup"><span data-stu-id="5c843-173">System.String</span></span>

## <span data-ttu-id="5c843-174">출력</span><span class="sxs-lookup"><span data-stu-id="5c843-174">OUTPUTS</span></span>

### <span data-ttu-id="5c843-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="5c843-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="5c843-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c843-176">NOTES</span></span>
* <span data-ttu-id="5c843-177">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="5c843-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="5c843-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c843-178">RELATED LINKS</span></span>

[<span data-ttu-id="5c843-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="5c843-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="5c843-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="5c843-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="5c843-181">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5c843-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

