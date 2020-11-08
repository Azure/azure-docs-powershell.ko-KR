---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046294"
---
# <span data-ttu-id="aaadf-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="aaadf-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="aaadf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaadf-102">SYNOPSIS</span></span>
<span data-ttu-id="aaadf-103">가져오기 또는 내보내기 요청의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="aaadf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aaadf-104">SYNTAX</span></span>

### <span data-ttu-id="aaadf-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="aaadf-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="aaadf-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="aaadf-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaadf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aaadf-107">DESCRIPTION</span></span>
<span data-ttu-id="aaadf-108">**Get-AzureSqlDatabaseImportExportStatus** cmdlet은 가져오기 또는 내보내기 요청의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="aaadf-109">Start-AzureSqlDatabaseImport 또는 Start-AzureSqlDatabaseExport cmdlet이 요청을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="aaadf-110">*요청 매개 변수* 를 사용 하 여 요청 개체를 지정 하거나 *RequestId* 매개 변수 및 *Username* , *Password* , *ServerName* 매개 변수를 사용 하 여 요청을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="aaadf-111">예제의</span><span class="sxs-lookup"><span data-stu-id="aaadf-111">EXAMPLES</span></span>

### <span data-ttu-id="aaadf-112">예제 1: 내보내기 요청의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="aaadf-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="aaadf-113">첫 번째 명령은 내보내기 요청을 만든 다음 $ExportRequest 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="aaadf-114">두 번째 명령은 $ExportRequest에 저장 된 내보내기 요청의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="aaadf-115">변수</span><span class="sxs-lookup"><span data-stu-id="aaadf-115">PARAMETERS</span></span>

### <span data-ttu-id="aaadf-116">-암호</span><span class="sxs-lookup"><span data-stu-id="aaadf-116">-Password</span></span>
<span data-ttu-id="aaadf-117">Azure SQL 데이터베이스 서버에 연결 하는 데 필요한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="aaadf-118">*RequestId* 매개 변수를 지정한 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaadf-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="aaadf-119">-Profile</span></span>
<span data-ttu-id="aaadf-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aaadf-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aaadf-122">-요청</span><span class="sxs-lookup"><span data-stu-id="aaadf-122">-Request</span></span>
<span data-ttu-id="aaadf-123">**Importexportrequest** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="aaadf-124">가져오기 또는 내보내기 요청 개체를 가져오려면 Start-AzureSqlDatabaseImport 또는 Start-AzureSqlDatabaseExport cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaadf-125">-RequestId</span><span class="sxs-lookup"><span data-stu-id="aaadf-125">-RequestId</span></span>
<span data-ttu-id="aaadf-126">이 cmdlet이 상태를 가져오는 가져오기 또는 내보내기 작업의 GUID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="aaadf-127">이 매개 변수를 지정 하는 경우 *UserName* , *Password* , *ServerName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaadf-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aaadf-128">-ServerName</span></span>
<span data-ttu-id="aaadf-129">Azure SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="aaadf-130">*RequestId* 매개 변수를 지정한 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaadf-131">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="aaadf-131">-Username</span></span>
<span data-ttu-id="aaadf-132">Azure SQL 데이터베이스 서버에 연결 하는 데 필요한 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="aaadf-133">*RequestId* 매개 변수를 지정한 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaadf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaadf-134">CommonParameters</span></span>
<span data-ttu-id="aaadf-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaadf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaadf-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaadf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaadf-137">입력</span><span class="sxs-lookup"><span data-stu-id="aaadf-137">INPUTS</span></span>

## <span data-ttu-id="aaadf-138">출력</span><span class="sxs-lookup"><span data-stu-id="aaadf-138">OUTPUTS</span></span>

### <span data-ttu-id="aaadf-139">WindowsAzure. SqlDatabase. \*. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="aaadf-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="aaadf-140">상속자</span><span class="sxs-lookup"><span data-stu-id="aaadf-140">NOTES</span></span>

## <span data-ttu-id="aaadf-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaadf-141">RELATED LINKS</span></span>

[<span data-ttu-id="aaadf-142">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="aaadf-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="aaadf-143">가져오기/내보내기 데이터베이스 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="aaadf-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="aaadf-144">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="aaadf-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="aaadf-145">시작-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="aaadf-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="aaadf-146">시작-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="aaadf-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


