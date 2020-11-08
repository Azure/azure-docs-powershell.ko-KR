---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046298"
---
# <span data-ttu-id="7390a-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7390a-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="7390a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7390a-102">SYNOPSIS</span></span>
<span data-ttu-id="7390a-103">하나 이상의 데이터베이스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="7390a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7390a-104">SYNTAX</span></span>

### <span data-ttu-id="7390a-105">ByConnectionContext (기본값)</span><span class="sxs-lookup"><span data-stu-id="7390a-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7390a-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="7390a-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7390a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7390a-107">DESCRIPTION</span></span>
<span data-ttu-id="7390a-108">**AzureSqlDatabase** Cmdlet은 Azure sql 데이터베이스 서버에서 Azure sql 데이터베이스 인스턴스를 하나 이상 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="7390a-109">**AzureSqlDatabaseServerContext** cmdlet을 사용 하 여 만드는 Azure SQL 데이터베이스 서버 연결 컨텍스트를 사용 하 여 서버를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="7390a-110">또는 Azure SQL 데이터베이스 서버 이름을 지정 하는 경우 cmdlet은 현재 Azure 구독 정보를 사용 하 여 서버에 대 한 액세스 요청을 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="7390a-111">데이터베이스를 지정 하지 않으면 **AzureSqlDatabase** cmdlet은 지정 된 서버의 모든 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="7390a-112">Restorable 손실 된 데이터베이스 검색:</span><span class="sxs-lookup"><span data-stu-id="7390a-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="7390a-113">*RestorableDropped* 매개 변수를 사용 하 여 restorable 손실 된 데이터베이스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="7390a-114">모든 restorable 삭제 된 데이터베이스를 반환 하려면 *DatabaseName* 및 *DatabaseDeletionDate* 없이 *RestorableDropped* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="7390a-115">특정 restorable 손실 된 데이터베이스를 반환 하려면 *DatabaseName* 및 *DatabaseDeletionDate* 매개 변수와 함께 *RestorableDropped* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="7390a-116">*DatabaseName* 매개 변수를 사용 하 여 손실 된 특정 restorable 데이터베이스를 검색 하는 경우 *DatabaseDeletionDate* 매개 변수도 포함 해야 하며 지정 된 *DatabaseDeletionDate* 값에는 원하는 데이터베이스와 일치 하는 밀리초가 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="7390a-117">**AzureSqlDatabase** cmdlet은 서버에서 restorable 손실 된 모든 데이터베이스 또는 *DatabaseName* 과 *DatabaseDeletionDate* 와 모두 일치 하는 특정 데이터베이스 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="7390a-118">특정 이름의 모든 restorable 손실 된 데이터베이스와 같이 다른 조건을 충족 하는 restorable 데이터베이스를 반환 하려면 삭제 한 모든 데이터베이스를 반환 하 고 클라이언트에서 결과를 필터링 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="7390a-119">예제의</span><span class="sxs-lookup"><span data-stu-id="7390a-119">EXAMPLES</span></span>

### <span data-ttu-id="7390a-120">예제 1: 서버의 모든 데이터베이스 검색</span><span class="sxs-lookup"><span data-stu-id="7390a-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="7390a-121">이 명령은 lpqd0zbr8y 이라는 서버의 모든 데이터베이스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="7390a-122">예제 2: 서버에서 restorable 삭제 된 모든 데이터베이스 검색</span><span class="sxs-lookup"><span data-stu-id="7390a-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="7390a-123">이 명령은 lpqd0zbr8y 이라는 서버에서 restorable 손실 된 모든 데이터베이스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="7390a-124">예제 3: 연결 컨텍스트에 지정 된 서버에서 데이터베이스 검색</span><span class="sxs-lookup"><span data-stu-id="7390a-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="7390a-125">이 명령은 연결 컨텍스트 $Context에 지정 된 서버에서 Database01 이라는 데이터베이스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="7390a-126">예제 4: 변수에 데이터베이스 개체 저장</span><span class="sxs-lookup"><span data-stu-id="7390a-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="7390a-127">이 명령은 lpqd0zbr8y 이라는 서버에서 Database01 이라는 데이터베이스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="7390a-128">이 명령은 데이터베이스 개체를 $Database 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="7390a-129">예제 5: restorable 삭제 된 데이터베이스 검색</span><span class="sxs-lookup"><span data-stu-id="7390a-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="7390a-130">이 명령은 lpqd0zbr8y 서버에서 11/9/2012에 삭제 된 Database01 라는 restorable 데이터베이스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="7390a-131">이 명령은 $DroppedDB 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="7390a-132">예제 6: 서버에서 restorable 손실 된 모든 데이터베이스 검색 및 결과 필터링</span><span class="sxs-lookup"><span data-stu-id="7390a-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="7390a-133">이 명령은 lpqd0zbr8y 이라는 서버에서 restorable 손실 된 모든 데이터베이스를 검색 한 다음, 해당 결과를 라는 데이터베이스로만 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="7390a-134">변수</span><span class="sxs-lookup"><span data-stu-id="7390a-134">PARAMETERS</span></span>

### <span data-ttu-id="7390a-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="7390a-135">-ConnectionContext</span></span>
<span data-ttu-id="7390a-136">데이터베이스를 검색할 서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

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

### <span data-ttu-id="7390a-137">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7390a-137">-Database</span></span>
<span data-ttu-id="7390a-138">이 cmdlet에서 검색 하는 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="7390a-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="7390a-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="7390a-140">삭제 날짜와 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="7390a-141">*RestorableDropped* 매개 변수를 지정 하는 경우 삭제 날짜 및 시간을 기준으로 restorable 손실 된 데이터베이스를 검색 하려면이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="7390a-142">*DatabaseDeletionDate* 매개 변수는 원하는 데이터베이스 시간에 맞게 밀리초를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="7390a-143">값을 밀리초 없이 지정 하면 데이터베이스를 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-143">Specifying a value without milliseconds results in the database not being found.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7390a-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7390a-144">-DatabaseName</span></span>
<span data-ttu-id="7390a-145">이 cmdlet에서 검색 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7390a-146">-프로필</span><span class="sxs-lookup"><span data-stu-id="7390a-146">-Profile</span></span>
<span data-ttu-id="7390a-147">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7390a-148">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7390a-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="7390a-149">-RestorableDropped</span></span>
<span data-ttu-id="7390a-150">이 cmdlet이 *데이터베이스* 개체 대신 *RestorableDroppedDatabase* 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="7390a-151">*DatabaseDeletionDate* 매개 변수를 사용 하 여 특정 restorable 끌어 놓은 데이터베이스를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7390a-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="7390a-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="7390a-153">이 cmdlet에서 검색 하는 restorable 손실 된 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7390a-154">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7390a-154">-ServerName</span></span>
<span data-ttu-id="7390a-155">이 cmdlet이 검색 하는 데이터베이스를 포함 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="7390a-156">Cmdlet은 현재 Azure 구독을 사용 하 여 서버에 액세스 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

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

### <span data-ttu-id="7390a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7390a-157">CommonParameters</span></span>
<span data-ttu-id="7390a-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7390a-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7390a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7390a-160">입력</span><span class="sxs-lookup"><span data-stu-id="7390a-160">INPUTS</span></span>

### <span data-ttu-id="7390a-161">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7390a-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="7390a-162">WindowsAzure. SqlDatabase에 대 한 RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="7390a-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="7390a-163">출력</span><span class="sxs-lookup"><span data-stu-id="7390a-163">OUTPUTS</span></span>

### <span data-ttu-id="7390a-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="7390a-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="7390a-165">*RestorableDropped* 매개 변수를 지정 하지 않으면이 Cmdlet은 *Database* 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="7390a-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="7390a-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="7390a-167">*RestorableDropped* 매개 변수를 지정 하면이 Cmdlet은 *RestorableDroppedDatabase* 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7390a-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="7390a-168">상속자</span><span class="sxs-lookup"><span data-stu-id="7390a-168">NOTES</span></span>

## <span data-ttu-id="7390a-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7390a-169">RELATED LINKS</span></span>

[<span data-ttu-id="7390a-170">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="7390a-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="7390a-171">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="7390a-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="7390a-172">새로운 AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7390a-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="7390a-173">새로운 AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="7390a-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="7390a-174">제거-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7390a-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="7390a-175">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7390a-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


