---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046293"
---
# <span data-ttu-id="a0852-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="a0852-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="a0852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0852-102">SYNOPSIS</span></span>
<span data-ttu-id="a0852-103">Azure 서버에서 데이터베이스 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="a0852-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0852-104">SYNTAX</span></span>

### <span data-ttu-id="a0852-105">ByConnectionContext (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0852-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a0852-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="a0852-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a0852-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a0852-107">DESCRIPTION</span></span>
<span data-ttu-id="a0852-108">**AzureSqlDatabaseOperation** cmdlet은 지정 된 Azure 서버에서 데이터베이스 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="a0852-109">*ServerName* 또는 *connectioncontext* 매개 변수만 지정 하는 경우에는 cmdlet에서 서버에 대 한 모든 데이터베이스 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="a0852-110">*데이터베이스* 또는 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 지정 하는 경우이 cmdlet은 지정 된 데이터베이스에 대 한 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="a0852-111">작업 GUID와 *ServerName* 또는 *connectioncontext* 를 지정 하면 cmdlet은 단일 데이터베이스 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="a0852-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a0852-112">EXAMPLES</span></span>

### <span data-ttu-id="a0852-113">예제 1: 데이터베이스에 대 한 모든 데이터베이스 작업의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="a0852-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="a0852-114">이 명령은 연결 컨텍스트가 $Context 지정 하는 서버의 Database17 이라는 데이터베이스에서 모든 데이터베이스 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="a0852-115">예제 2: 서버에 대 한 모든 데이터베이스 작업의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="a0852-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="a0852-116">이 명령은 연결 컨텍스트가 $Context 지정 하는 서버에 있는 모든 데이터베이스 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="a0852-117">변수</span><span class="sxs-lookup"><span data-stu-id="a0852-117">PARAMETERS</span></span>

### <span data-ttu-id="a0852-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="a0852-118">-ConnectionContext</span></span>
<span data-ttu-id="a0852-119">서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0852-120">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="a0852-120">-Database</span></span>
<span data-ttu-id="a0852-121">Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="a0852-122">이 매개 변수를 지정 하는 경우 *ServerName* 매개 변수 또는 *connectioncontext* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0852-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0852-123">-DatabaseName</span></span>
<span data-ttu-id="a0852-124">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-124">Specifies the name of a database.</span></span>
<span data-ttu-id="a0852-125">이 매개 변수를 지정 하는 경우 *ServerName* 매개 변수 또는 *connectioncontext* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0852-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="a0852-126">-OperationGuid</span></span>
<span data-ttu-id="a0852-127">이 cmdlet이 상태를 가져오는 특정 데이터베이스 작업을 나타내는 작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="a0852-128">Azure SQL 데이터베이스 또는 서버에 대 한 모든 데이터베이스 작업을 요청 하 여 작업 Id를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="a0852-129">이 매개 변수를 지정 하는 경우 *ServerName* 매개 변수 또는 *connectioncontext* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0852-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="a0852-130">-Profile</span></span>
<span data-ttu-id="a0852-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0852-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0852-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0852-133">-ServerName</span></span>
<span data-ttu-id="a0852-134">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-134">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0852-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0852-135">CommonParameters</span></span>
<span data-ttu-id="a0852-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0852-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0852-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0852-138">입력</span><span class="sxs-lookup"><span data-stu-id="a0852-138">INPUTS</span></span>

### <span data-ttu-id="a0852-139">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="a0852-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="a0852-140">WindowsAzure. SqlDatabase. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="a0852-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="a0852-141">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="a0852-141">System.Guid</span></span>

## <span data-ttu-id="a0852-142">출력</span><span class="sxs-lookup"><span data-stu-id="a0852-142">OUTPUTS</span></span>

### <span data-ttu-id="a0852-143">WindowsAzure. SqlDatabase. \* 데이터베이스의 DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="a0852-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="a0852-144">이 cmdlet은 여러 작업을 가져오는 경우 **Databaseoperationresponselist** 개체의 배열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0852-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="a0852-145">WindowsAzure를 SqlDatabase. \*. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a0852-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="a0852-146">상속자</span><span class="sxs-lookup"><span data-stu-id="a0852-146">NOTES</span></span>

## <span data-ttu-id="a0852-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0852-147">RELATED LINKS</span></span>

[<span data-ttu-id="a0852-148">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="a0852-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="a0852-149">데이터베이스 작업 상태</span><span class="sxs-lookup"><span data-stu-id="a0852-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="a0852-150">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="a0852-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="a0852-151">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0852-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="a0852-152">새로운 AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="a0852-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


