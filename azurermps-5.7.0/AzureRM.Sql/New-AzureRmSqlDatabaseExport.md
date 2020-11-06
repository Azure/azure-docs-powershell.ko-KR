---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 324686ace908235e3b48fb150249d2bad22c169b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524816"
---
# <span data-ttu-id="ebabb-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="ebabb-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="ebabb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebabb-102">SYNOPSIS</span></span>
<span data-ttu-id="ebabb-103">Azure SQL 데이터베이스를 저장소 계정으로 bacpac 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebabb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebabb-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebabb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ebabb-105">DESCRIPTION</span></span>
<span data-ttu-id="ebabb-106">**AzureRmSqlDatabaseExport** Cmdlet은 Azure SQL 데이터베이스를 저장소 계정으로 bacpac 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="ebabb-107">이 요청에 대 한 상태 정보를 검색 하기 위해 내보내기 데이터베이스 상태 가져오기 요청을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="ebabb-108">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ebabb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ebabb-109">EXAMPLES</span></span>

### <span data-ttu-id="ebabb-110">예제 1: 데이터베이스에 대 한 내보내기 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="ebabb-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="ebabb-111">이 명령은 지정 된 데이터베이스에 대 한 내보내기 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="ebabb-112">변수</span><span class="sxs-lookup"><span data-stu-id="ebabb-112">PARAMETERS</span></span>

### <span data-ttu-id="ebabb-113">-관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="ebabb-113">-AdministratorLogin</span></span>
<span data-ttu-id="ebabb-114">SQL 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-114">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebabb-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ebabb-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ebabb-116">SQL 관리자의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-116">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebabb-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="ebabb-117">-AuthenticationType</span></span>
<span data-ttu-id="ebabb-118">서버에 액세스 하는 데 사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="ebabb-119">인증 유형이 설정 되지 않은 경우 기본값은 SQL입니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="ebabb-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ebabb-121">Test.sql.</span><span class="sxs-lookup"><span data-stu-id="ebabb-121">Sql.</span></span>
<span data-ttu-id="ebabb-122">SQL 인증.</span><span class="sxs-lookup"><span data-stu-id="ebabb-122">SQL authentication.</span></span>
<span data-ttu-id="ebabb-123">*관리자 로그인* 을 설정 하 고 SQL 관리자 사용자 이름 및 암호를 *AdministratorLoginPassword* .</span><span class="sxs-lookup"><span data-stu-id="ebabb-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="ebabb-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="ebabb-124">ADPassword.</span></span>
<span data-ttu-id="ebabb-125">Azure Active Directory 인증.</span><span class="sxs-lookup"><span data-stu-id="ebabb-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="ebabb-126">*관리자 로그인* 및 *ADMINISTRATORLOGINPASSWORD* 를 Azure AD 관리자 사용자 이름 및 암호로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="ebabb-127">이 매개 변수는 SQL Database V12 server 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-127">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebabb-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebabb-128">-DatabaseName</span></span>
<span data-ttu-id="ebabb-129">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="ebabb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebabb-130">-DefaultProfile</span></span>
<span data-ttu-id="ebabb-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ebabb-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebabb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebabb-132">-ResourceGroupName</span></span>
<span data-ttu-id="ebabb-133">SQL 데이터베이스 서버에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="ebabb-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ebabb-134">-ServerName</span></span>
<span data-ttu-id="ebabb-135">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="ebabb-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="ebabb-136">-StorageKey</span></span>
<span data-ttu-id="ebabb-137">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebabb-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="ebabb-138">-StorageKeyType</span></span>
<span data-ttu-id="ebabb-139">저장소 계정의 선택 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-139">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="ebabb-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ebabb-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="ebabb-141">StorageAccessKey.</span></span>
<span data-ttu-id="ebabb-142">이 값은 저장소 계정 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="ebabb-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="ebabb-143">SharedAccessKey.</span></span>
<span data-ttu-id="ebabb-144">이 값은 SAS (공유 액세스 서명) 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-144">This value uses a Shared Access Signature (SAS) key.</span></span>

```yaml
Type: StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebabb-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="ebabb-145">-StorageUri</span></span>
<span data-ttu-id="ebabb-146">Blob 링크를 URL로 서 bacpac 파일에 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebabb-147">-확인</span><span class="sxs-lookup"><span data-stu-id="ebabb-147">-Confirm</span></span>
<span data-ttu-id="ebabb-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebabb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebabb-149">-WhatIf</span></span>
<span data-ttu-id="ebabb-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebabb-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebabb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebabb-152">CommonParameters</span></span>
<span data-ttu-id="ebabb-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebabb-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebabb-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebabb-155">입력</span><span class="sxs-lookup"><span data-stu-id="ebabb-155">INPUTS</span></span>

### <span data-ttu-id="ebabb-156">않아야</span><span class="sxs-lookup"><span data-stu-id="ebabb-156">None</span></span>
<span data-ttu-id="ebabb-157">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebabb-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ebabb-158">출력</span><span class="sxs-lookup"><span data-stu-id="ebabb-158">OUTPUTS</span></span>

### <span data-ttu-id="ebabb-159">AzureSqlDatabaseImportExportBaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="ebabb-159">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="ebabb-160">상속자</span><span class="sxs-lookup"><span data-stu-id="ebabb-160">NOTES</span></span>
* <span data-ttu-id="ebabb-161">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="ebabb-161">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="ebabb-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebabb-162">RELATED LINKS</span></span>

[<span data-ttu-id="ebabb-163">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="ebabb-163">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="ebabb-164">새로운 AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="ebabb-164">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="ebabb-165">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ebabb-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
