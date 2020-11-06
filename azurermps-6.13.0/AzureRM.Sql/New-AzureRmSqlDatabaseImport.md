---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 4ea8a6aca74634e8105026e45c25b861e8c060f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530037"
---
# <span data-ttu-id="19887-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="19887-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="19887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19887-102">SYNOPSIS</span></span>
<span data-ttu-id="19887-103">Bacpac 파일을 가져오고 서버에서 새 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19887-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19887-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19887-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19887-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19887-105">DESCRIPTION</span></span>
<span data-ttu-id="19887-106">**AzureRmSqlDatabaseImport** Cmdlet은 azure 저장소 계정에서 새 Azure SQL 데이터베이스로 bacpac 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19887-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="19887-107">이 요청에 대 한 상태 정보를 검색 하기 위해 가져오기 데이터베이스 상태 읽어오기 요청을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19887-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="19887-108">예제의</span><span class="sxs-lookup"><span data-stu-id="19887-108">EXAMPLES</span></span>

### <span data-ttu-id="19887-109">예제 1: bacpac 파일에 대 한 가져오기 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="19887-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
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

<span data-ttu-id="19887-110">이 명령은 가져오기 요청을 만들어 bacpac을 새 데이터베이스로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19887-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="19887-111">변수</span><span class="sxs-lookup"><span data-stu-id="19887-111">PARAMETERS</span></span>

### <span data-ttu-id="19887-112">-관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="19887-112">-AdministratorLogin</span></span>
<span data-ttu-id="19887-113">SQL 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="19887-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="19887-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="19887-115">SQL 관리자의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="19887-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="19887-116">-AuthenticationType</span></span>
<span data-ttu-id="19887-117">서버에 액세스 하는 데 사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="19887-118">인증 유형이 설정 되지 않은 경우이 매개 변수는 기본적으로 SQL입니다.</span><span class="sxs-lookup"><span data-stu-id="19887-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="19887-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="19887-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19887-120">TEST.SQL.</span><span class="sxs-lookup"><span data-stu-id="19887-120">SQL.</span></span>
<span data-ttu-id="19887-121">SQL 인증.</span><span class="sxs-lookup"><span data-stu-id="19887-121">SQL authentication.</span></span>
<span data-ttu-id="19887-122">관리자 *로그인* 및 *AdministratorLoginPassword* 매개 변수를 SQL 관리자 사용자 이름 및 암호로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="19887-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="19887-123">ADPassword.</span></span>
<span data-ttu-id="19887-124">Azure Active Directory 인증.</span><span class="sxs-lookup"><span data-stu-id="19887-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="19887-125">*관리자 로그인* 및 *AdministratorLoginPassword* 를 Azure Active Directory 관리자 사용자 이름 및 암호로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="19887-126">이 매개 변수는 SQL Database V12 server 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19887-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="19887-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="19887-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="19887-128">새로 가져온 데이터베이스의 최대 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="19887-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19887-129">-DatabaseName</span></span>
<span data-ttu-id="19887-130">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="19887-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19887-131">-DefaultProfile</span></span>
<span data-ttu-id="19887-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="19887-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19887-133">-에디션</span><span class="sxs-lookup"><span data-stu-id="19887-133">-Edition</span></span>
<span data-ttu-id="19887-134">가져올 새 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="19887-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="19887-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19887-136">Premium</span><span class="sxs-lookup"><span data-stu-id="19887-136">Premium</span></span>
- <span data-ttu-id="19887-137">기본적</span><span class="sxs-lookup"><span data-stu-id="19887-137">Basic</span></span>
- <span data-ttu-id="19887-138">표준이</span><span class="sxs-lookup"><span data-stu-id="19887-138">Standard</span></span>
- <span data-ttu-id="19887-139">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="19887-139">DataWarehouse</span></span>
- <span data-ttu-id="19887-140">비우거나</span><span class="sxs-lookup"><span data-stu-id="19887-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19887-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19887-141">-ResourceGroupName</span></span>
<span data-ttu-id="19887-142">SQL 데이터베이스 서버에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="19887-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="19887-143">-ServerName</span></span>
<span data-ttu-id="19887-144">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="19887-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="19887-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="19887-146">Azure SQL Database에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="19887-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="19887-147">-StorageKey</span></span>
<span data-ttu-id="19887-148">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-148">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="19887-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="19887-149">-StorageKeyType</span></span>
<span data-ttu-id="19887-150">저장소 계정의 선택 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="19887-151">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="19887-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19887-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="19887-152">StorageAccessKey.</span></span>
<span data-ttu-id="19887-153">저장소 계정 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="19887-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="19887-154">SharedAccessKey.</span></span>
<span data-ttu-id="19887-155">SA (공유 액세스 서명) 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-155">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="19887-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="19887-156">-StorageUri</span></span>
<span data-ttu-id="19887-157">Bacpac 파일의 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-157">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="19887-158">-확인</span><span class="sxs-lookup"><span data-stu-id="19887-158">-Confirm</span></span>
<span data-ttu-id="19887-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19887-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19887-160">-WhatIf</span></span>
<span data-ttu-id="19887-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19887-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19887-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19887-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19887-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19887-163">CommonParameters</span></span>
<span data-ttu-id="19887-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19887-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19887-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19887-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19887-166">입력</span><span class="sxs-lookup"><span data-stu-id="19887-166">INPUTS</span></span>

### <span data-ttu-id="19887-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19887-167">System.String</span></span>

## <span data-ttu-id="19887-168">출력</span><span class="sxs-lookup"><span data-stu-id="19887-168">OUTPUTS</span></span>

### <span data-ttu-id="19887-169">AzureSqlDatabaseImportExportBaseModel을 (를) 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="19887-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="19887-170">상속자</span><span class="sxs-lookup"><span data-stu-id="19887-170">NOTES</span></span>
* <span data-ttu-id="19887-171">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="19887-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="19887-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19887-172">RELATED LINKS</span></span>

[<span data-ttu-id="19887-173">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="19887-173">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="19887-174">새로운 AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="19887-174">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="19887-175">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="19887-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

