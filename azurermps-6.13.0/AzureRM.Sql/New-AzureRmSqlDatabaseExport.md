---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 838c09c8a86c081a1b335fa22f4473d099a1b182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704102"
---
# <span data-ttu-id="c4a74-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="c4a74-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="c4a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a74-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a74-103">Azure SQL 데이터베이스를 저장소 계정으로 bacpac 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4a74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4a74-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a74-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4a74-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a74-106">**AzureRmSqlDatabaseExport** Cmdlet은 Azure SQL 데이터베이스를 저장소 계정으로 bacpac 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="c4a74-107">이 요청에 대 한 상태 정보를 검색 하기 위해 내보내기 데이터베이스 상태 가져오기 요청을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="c4a74-108">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c4a74-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c4a74-109">EXAMPLES</span></span>

### <span data-ttu-id="c4a74-110">예제 1: 데이터베이스에 대 한 내보내기 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="c4a74-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="c4a74-111">이 명령은 지정 된 데이터베이스에 대 한 내보내기 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="c4a74-112">변수</span><span class="sxs-lookup"><span data-stu-id="c4a74-112">PARAMETERS</span></span>

### <span data-ttu-id="c4a74-113">-관리자 로그인</span><span class="sxs-lookup"><span data-stu-id="c4a74-113">-AdministratorLogin</span></span>
<span data-ttu-id="c4a74-114">SQL 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="c4a74-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="c4a74-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c4a74-116">SQL 관리자의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="c4a74-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="c4a74-117">-AuthenticationType</span></span>
<span data-ttu-id="c4a74-118">서버에 액세스 하는 데 사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="c4a74-119">인증 유형이 설정 되지 않은 경우 기본값은 SQL입니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="c4a74-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4a74-121">Test.sql.</span><span class="sxs-lookup"><span data-stu-id="c4a74-121">Sql.</span></span>
<span data-ttu-id="c4a74-122">SQL 인증.</span><span class="sxs-lookup"><span data-stu-id="c4a74-122">SQL authentication.</span></span>
<span data-ttu-id="c4a74-123">*관리자 로그인* 을 설정 하 고 SQL 관리자 사용자 이름 및 암호를 *AdministratorLoginPassword* .</span><span class="sxs-lookup"><span data-stu-id="c4a74-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="c4a74-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="c4a74-124">ADPassword.</span></span>
<span data-ttu-id="c4a74-125">Azure Active Directory 인증.</span><span class="sxs-lookup"><span data-stu-id="c4a74-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="c4a74-126">*관리자 로그인* 및 *ADMINISTRATORLOGINPASSWORD* 를 Azure AD 관리자 사용자 이름 및 암호로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="c4a74-127">이 매개 변수는 SQL Database V12 server 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="c4a74-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4a74-128">-DatabaseName</span></span>
<span data-ttu-id="c4a74-129">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="c4a74-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a74-130">-DefaultProfile</span></span>
<span data-ttu-id="c4a74-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c4a74-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4a74-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a74-132">-ResourceGroupName</span></span>
<span data-ttu-id="c4a74-133">SQL 데이터베이스 서버에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="c4a74-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4a74-134">-ServerName</span></span>
<span data-ttu-id="c4a74-135">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="c4a74-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="c4a74-136">-StorageKey</span></span>
<span data-ttu-id="c4a74-137">저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="c4a74-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="c4a74-138">-StorageKeyType</span></span>
<span data-ttu-id="c4a74-139">저장소 계정의 선택 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-139">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="c4a74-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4a74-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="c4a74-141">StorageAccessKey.</span></span>
<span data-ttu-id="c4a74-142">이 값은 저장소 계정 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="c4a74-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="c4a74-143">SharedAccessKey.</span></span>
<span data-ttu-id="c4a74-144">이 값은 SAS (공유 액세스 서명) 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="c4a74-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="c4a74-145">-StorageUri</span></span>
<span data-ttu-id="c4a74-146">Blob 링크를 URL로 서 bacpac 파일에 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="c4a74-147">-확인</span><span class="sxs-lookup"><span data-stu-id="c4a74-147">-Confirm</span></span>
<span data-ttu-id="c4a74-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a74-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a74-149">-WhatIf</span></span>
<span data-ttu-id="c4a74-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a74-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a74-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a74-152">CommonParameters</span></span>
<span data-ttu-id="c4a74-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a74-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a74-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a74-155">입력</span><span class="sxs-lookup"><span data-stu-id="c4a74-155">INPUTS</span></span>

### <span data-ttu-id="c4a74-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4a74-156">System.String</span></span>

## <span data-ttu-id="c4a74-157">출력</span><span class="sxs-lookup"><span data-stu-id="c4a74-157">OUTPUTS</span></span>

### <span data-ttu-id="c4a74-158">AzureSqlDatabaseImportExportBaseModel을 (를) 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="c4a74-158">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="c4a74-159">상속자</span><span class="sxs-lookup"><span data-stu-id="c4a74-159">NOTES</span></span>
* <span data-ttu-id="c4a74-160">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="c4a74-160">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="c4a74-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4a74-161">RELATED LINKS</span></span>

[<span data-ttu-id="c4a74-162">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="c4a74-162">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="c4a74-163">새로운 AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="c4a74-163">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="c4a74-164">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c4a74-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
