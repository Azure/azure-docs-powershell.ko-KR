---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045427"
---
# <span data-ttu-id="73c6b-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="73c6b-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="73c6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="73c6b-103">Blob 저장소에서 Azure SQL 데이터베이스로 가져오기 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="73c6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73c6b-104">SYNTAX</span></span>

### <span data-ttu-id="73c6b-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="73c6b-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="73c6b-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="73c6b-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="73c6b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="73c6b-107">DESCRIPTION</span></span>
<span data-ttu-id="73c6b-108">**AzureSqlDatabaseImport** Cmdlet은 azure Blob Storage에서 Azure SQL 데이터베이스로 가져오기 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="73c6b-109">데이터베이스가 없는 경우이 cmdlet은 사용자가 지정한 크기와 버전 값을 사용 하 여 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="73c6b-110">작업에 데이터베이스 서버 연결 컨텍스트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="73c6b-111">Get-AzureSqlDatabaseImportExportStatus cmdlet을 사용 하 여 가져오기 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="73c6b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="73c6b-112">EXAMPLES</span></span>

### <span data-ttu-id="73c6b-113">예제 1: 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="73c6b-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="73c6b-114">이 예제에서는 $BlobName 변수의 Blob 저장소에서 DatabaseName 이라는 Azure SQL 데이터베이스에 가져오기 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="73c6b-115">변수</span><span class="sxs-lookup"><span data-stu-id="73c6b-115">PARAMETERS</span></span>

### <span data-ttu-id="73c6b-116">-BlobName</span><span class="sxs-lookup"><span data-stu-id="73c6b-116">-BlobName</span></span>
<span data-ttu-id="73c6b-117">이 cmdlet에서 데이터베이스를 가져오는 Azure Blob 저장소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="73c6b-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="73c6b-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="73c6b-119">데이터베이스의 최대 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="73c6b-120">데이터베이스가 없는 경우이 cmdlet은이 최대 크기를 기준으로 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="73c6b-121">허용 되는 값은 버전에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c6b-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73c6b-122">-DatabaseName</span></span>
<span data-ttu-id="73c6b-123">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-123">Specifies a name for the database.</span></span>
<span data-ttu-id="73c6b-124">데이터베이스가 없는 경우이 cmdlet은 데이터베이스를 만들고이 매개 변수에서 지정 하는 이름을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="73c6b-125">-에디션</span><span class="sxs-lookup"><span data-stu-id="73c6b-125">-Edition</span></span>
<span data-ttu-id="73c6b-126">데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="73c6b-127">데이터베이스가 없으면이 cmdlet이이 버전으로 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="73c6b-128">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-128">Valid values are:</span></span> 

- <span data-ttu-id="73c6b-129">않아야</span><span class="sxs-lookup"><span data-stu-id="73c6b-129">None</span></span>
- <span data-ttu-id="73c6b-130">웹</span><span class="sxs-lookup"><span data-stu-id="73c6b-130">Web</span></span> 
- <span data-ttu-id="73c6b-131">조직</span><span class="sxs-lookup"><span data-stu-id="73c6b-131">Business</span></span> 
- <span data-ttu-id="73c6b-132">기본적</span><span class="sxs-lookup"><span data-stu-id="73c6b-132">Basic</span></span>
- <span data-ttu-id="73c6b-133">표준이</span><span class="sxs-lookup"><span data-stu-id="73c6b-133">Standard</span></span>
- <span data-ttu-id="73c6b-134">Premium</span><span class="sxs-lookup"><span data-stu-id="73c6b-134">Premium</span></span>

<span data-ttu-id="73c6b-135">기본값은 웹입니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c6b-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="73c6b-136">-Profile</span></span>
<span data-ttu-id="73c6b-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="73c6b-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c6b-139">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="73c6b-139">-SqlConnectionContext</span></span>
<span data-ttu-id="73c6b-140">데이터베이스를 포함 하는 서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-140">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c6b-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="73c6b-141">-StorageContainer</span></span>
<span data-ttu-id="73c6b-142">이 cmdlet에서 데이터베이스를 가져오는 Blob을 포함 하는 저장소 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c6b-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="73c6b-143">-StorageContainerName</span></span>
<span data-ttu-id="73c6b-144">Blob 저장소 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-144">Specifies the name of the Blob storage container.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c6b-145">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="73c6b-145">-StorageContext</span></span>
<span data-ttu-id="73c6b-146">Blob 저장소 컨테이너의 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-146">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c6b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c6b-147">CommonParameters</span></span>
<span data-ttu-id="73c6b-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c6b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c6b-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c6b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c6b-150">입력</span><span class="sxs-lookup"><span data-stu-id="73c6b-150">INPUTS</span></span>

## <span data-ttu-id="73c6b-151">출력</span><span class="sxs-lookup"><span data-stu-id="73c6b-151">OUTPUTS</span></span>

### <span data-ttu-id="73c6b-152">SqlDatabase. WindowsAzure Exportrequest.</span><span class="sxs-lookup"><span data-stu-id="73c6b-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="73c6b-153">상속자</span><span class="sxs-lookup"><span data-stu-id="73c6b-153">NOTES</span></span>

## <span data-ttu-id="73c6b-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73c6b-154">RELATED LINKS</span></span>

[<span data-ttu-id="73c6b-155">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="73c6b-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="73c6b-156">데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="73c6b-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="73c6b-157">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="73c6b-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="73c6b-158">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="73c6b-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="73c6b-159">시작-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="73c6b-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


