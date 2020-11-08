---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045752"
---
# <span data-ttu-id="8338e-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="8338e-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="8338e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8338e-102">SYNOPSIS</span></span>
<span data-ttu-id="8338e-103">Azure SQL 데이터베이스에서 Blob 저장소로 내보내기 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="8338e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8338e-104">SYNTAX</span></span>

### <span data-ttu-id="8338e-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="8338e-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8338e-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="8338e-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8338e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8338e-107">DESCRIPTION</span></span>
<span data-ttu-id="8338e-108">**AzureSqlDatabaseExport** Cmdlet은 Azure SQL 데이터베이스에서 Blob 저장소로 내보내기 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="8338e-109">작업에 데이터베이스 서버 연결 컨텍스트가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="8338e-110">Get-AzureSqlDatabaseImportExportStatus cmdlet을 사용 하 여 내보내기 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="8338e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8338e-111">EXAMPLES</span></span>

### <span data-ttu-id="8338e-112">예제 1: 데이터베이스 내보내기</span><span class="sxs-lookup"><span data-stu-id="8338e-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="8338e-113">이 예제에서는 $DatabaseName 변수에 저장 된 이름을 갖는 Azure SQL 데이터베이스에서 $BlobName 변수에 저장 된 Blob 저장소로 내보내기 프로세스를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="8338e-114">변수</span><span class="sxs-lookup"><span data-stu-id="8338e-114">PARAMETERS</span></span>

### <span data-ttu-id="8338e-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="8338e-115">-BlobName</span></span>
<span data-ttu-id="8338e-116">이 cmdlet이 데이터베이스를 내보낼 Azure Blob 저장소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

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

### <span data-ttu-id="8338e-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8338e-117">-DatabaseName</span></span>
<span data-ttu-id="8338e-118">이 cmdlet에서 데이터를 내보낼 원본 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

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

### <span data-ttu-id="8338e-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="8338e-119">-Profile</span></span>
<span data-ttu-id="8338e-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8338e-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8338e-122">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="8338e-122">-SqlConnectionContext</span></span>
<span data-ttu-id="8338e-123">데이터베이스를 포함 하는 서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-123">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="8338e-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="8338e-124">-StorageContainer</span></span>
<span data-ttu-id="8338e-125">이 cmdlet이 데이터베이스를 내보낼 Blob을 포함 하는 저장소 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

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

### <span data-ttu-id="8338e-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="8338e-126">-StorageContainerName</span></span>
<span data-ttu-id="8338e-127">이 cmdlet이 데이터베이스를 내보낼 Blob을 포함 하는 저장소 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

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

### <span data-ttu-id="8338e-128">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="8338e-128">-StorageContext</span></span>
<span data-ttu-id="8338e-129">Blob 저장소 컨테이너의 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-129">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="8338e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8338e-130">CommonParameters</span></span>
<span data-ttu-id="8338e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8338e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8338e-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8338e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8338e-133">입력</span><span class="sxs-lookup"><span data-stu-id="8338e-133">INPUTS</span></span>

## <span data-ttu-id="8338e-134">출력</span><span class="sxs-lookup"><span data-stu-id="8338e-134">OUTPUTS</span></span>

### <span data-ttu-id="8338e-135">SqlDatabase. WindowsAzure Exportrequest.</span><span class="sxs-lookup"><span data-stu-id="8338e-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="8338e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8338e-136">NOTES</span></span>

## <span data-ttu-id="8338e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8338e-137">RELATED LINKS</span></span>

[<span data-ttu-id="8338e-138">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="8338e-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="8338e-139">데이터베이스 내보내기</span><span class="sxs-lookup"><span data-stu-id="8338e-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="8338e-140">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="8338e-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="8338e-141">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="8338e-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="8338e-142">시작-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="8338e-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


