---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 8ebe1cecc42d8ee01c270b994e1e10de4f402c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529990"
---
# <span data-ttu-id="a78a7-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="a78a7-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="a78a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a78a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a78a7-103">Bacpac 파일을 가져오고 서버에서 새 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a78a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a78a7-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a78a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a78a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a78a7-106">**AzureRmSqlDatabaseImport** Cmdlet은 azure 저장소 계정에서 새 Azure SQL 데이터베이스로 bacpac 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="a78a7-107">이 요청에 대 한 상태 정보를 검색 하기 위해 가져오기 데이터베이스 상태 읽어오기 요청을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="a78a7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a78a7-108">EXAMPLES</span></span>

### <span data-ttu-id="a78a7-109">예제 1: bacpac 파일에 대 한 가져오기 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="a78a7-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="a78a7-110">이 명령은 가져오기 요청을 만들어 bacpac을 새 데이터베이스로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="a78a7-111">변수</span><span class="sxs-lookup"><span data-stu-id="a78a7-111">PARAMETERS</span></span>

### <span data-ttu-id="a78a7-112">-관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="a78a7-112">-AdministratorLogin</span></span>
<span data-ttu-id="a78a7-113">SQL 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="a78a7-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="a78a7-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="a78a7-115">SQL 관리자의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="a78a7-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a78a7-116">-AuthenticationType</span></span>
<span data-ttu-id="a78a7-117">서버에 액세스 하는 데 사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="a78a7-118">인증 유형이 설정 되지 않은 경우이 매개 변수는 기본적으로 SQL입니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="a78a7-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a78a7-120">TEST.SQL.</span><span class="sxs-lookup"><span data-stu-id="a78a7-120">SQL.</span></span>
<span data-ttu-id="a78a7-121">SQL 인증.</span><span class="sxs-lookup"><span data-stu-id="a78a7-121">SQL authentication.</span></span>
<span data-ttu-id="a78a7-122">관리자 *로그인* 및 *AdministratorLoginPassword* 매개 변수를 SQL 관리자 사용자 이름 및 암호로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="a78a7-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="a78a7-123">ADPassword.</span></span>
<span data-ttu-id="a78a7-124">Azure Active Directory 인증.</span><span class="sxs-lookup"><span data-stu-id="a78a7-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="a78a7-125">*관리자 로그인* 및 *AdministratorLoginPassword* 를 Azure Active Directory 관리자 사용자 이름 및 암호로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="a78a7-126">이 매개 변수는 SQL Database V12 server 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="a78a7-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="a78a7-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="a78a7-128">새로 가져온 데이터베이스의 최대 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="a78a7-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a78a7-129">-DatabaseName</span></span>
<span data-ttu-id="a78a7-130">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="a78a7-131">-에디션</span><span class="sxs-lookup"><span data-stu-id="a78a7-131">-Edition</span></span>
<span data-ttu-id="a78a7-132">가져올 새 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-132">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="a78a7-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a78a7-134">Premium</span><span class="sxs-lookup"><span data-stu-id="a78a7-134">Premium</span></span>
- <span data-ttu-id="a78a7-135">기본적</span><span class="sxs-lookup"><span data-stu-id="a78a7-135">Basic</span></span>
- <span data-ttu-id="a78a7-136">표준이</span><span class="sxs-lookup"><span data-stu-id="a78a7-136">Standard</span></span>
- <span data-ttu-id="a78a7-137">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="a78a7-137">DataWarehouse</span></span>
- <span data-ttu-id="a78a7-138">비우거나</span><span class="sxs-lookup"><span data-stu-id="a78a7-138">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a78a7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78a7-139">-ResourceGroupName</span></span>
<span data-ttu-id="a78a7-140">SQL 데이터베이스 서버에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-140">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="a78a7-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a78a7-141">-ServerName</span></span>
<span data-ttu-id="a78a7-142">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-142">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="a78a7-143">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a78a7-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="a78a7-144">Azure SQL Database에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-144">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a78a7-145">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="a78a7-145">-StorageKey</span></span>
<span data-ttu-id="a78a7-146">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-146">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="a78a7-147">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="a78a7-147">-StorageKeyType</span></span>
<span data-ttu-id="a78a7-148">저장소 계정의 선택 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-148">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="a78a7-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a78a7-150">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="a78a7-150">StorageAccessKey.</span></span>
<span data-ttu-id="a78a7-151">저장소 계정 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-151">Uses the storage account key.</span></span> 
- <span data-ttu-id="a78a7-152">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="a78a7-152">SharedAccessKey.</span></span>
<span data-ttu-id="a78a7-153">SA (공유 액세스 서명) 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-153">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="a78a7-154">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="a78a7-154">-StorageUri</span></span>
<span data-ttu-id="a78a7-155">Bacpac 파일의 blob URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-155">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="a78a7-156">-확인</span><span class="sxs-lookup"><span data-stu-id="a78a7-156">-Confirm</span></span>
<span data-ttu-id="a78a7-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a78a7-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a78a7-158">-WhatIf</span></span>
<span data-ttu-id="a78a7-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a78a7-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a78a7-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78a7-161">-DefaultProfile</span></span>
<span data-ttu-id="a78a7-162">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a78a7-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78a7-163">CommonParameters</span></span>
<span data-ttu-id="a78a7-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78a7-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78a7-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a78a7-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78a7-166">입력</span><span class="sxs-lookup"><span data-stu-id="a78a7-166">INPUTS</span></span>

## <span data-ttu-id="a78a7-167">출력</span><span class="sxs-lookup"><span data-stu-id="a78a7-167">OUTPUTS</span></span>

### <span data-ttu-id="a78a7-168">AzureSqlDatabaseImportExportBaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="a78a7-168">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="a78a7-169">상속자</span><span class="sxs-lookup"><span data-stu-id="a78a7-169">NOTES</span></span>
* <span data-ttu-id="a78a7-170">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="a78a7-170">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="a78a7-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a78a7-171">RELATED LINKS</span></span>

[<span data-ttu-id="a78a7-172">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="a78a7-172">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="a78a7-173">새로운 AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="a78a7-173">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="a78a7-174">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a78a7-174">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

