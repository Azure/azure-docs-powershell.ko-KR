---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046295"
---
# <span data-ttu-id="16916-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="16916-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="16916-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16916-102">SYNOPSIS</span></span>
<span data-ttu-id="16916-103">복사 관계의 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="16916-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16916-104">SYNTAX</span></span>

### <span data-ttu-id="16916-105">ByServerNameOnly (기본값)</span><span class="sxs-lookup"><span data-stu-id="16916-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="16916-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="16916-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="16916-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="16916-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="16916-108">설명은</span><span class="sxs-lookup"><span data-stu-id="16916-108">DESCRIPTION</span></span>
<span data-ttu-id="16916-109">**AzureSqlDatabaseCopy** cmdlet은 하나 이상의 활성 복사본 관계의 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="16916-110">Start-AzureSqlDatabaseCopy 또는 Stop-AzureSqlDatabaseCopy cmdlet을 실행 한 후이 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="16916-111">특정 복사본 관계, 모든 관계 복사 또는 특정 대상 서버의 모든 복사본과 같이 필터링 된 복사본 관계 목록을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16916-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="16916-112">원본 또는 대상 데이터베이스를 호스트 하는 서버에서이 cmdlet을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16916-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="16916-113">이 cmdlet은 동기적으로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16916-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="16916-114">Cmdlet은 status 개체를 반환할 때까지 Azure PowerShell 콘솔을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="16916-115">함께 *서버* 및 함께 *데이터베이스* 매개 변수를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="16916-116">매개 변수 중 하나를 지정 하지 않으면이 cmdlet은 결과 테이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="16916-117">특정 데이터베이스의 상태만 보려면 두 매개 변수를 모두 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="16916-118">예제의</span><span class="sxs-lookup"><span data-stu-id="16916-118">EXAMPLES</span></span>

### <span data-ttu-id="16916-119">예제 1: 데이터베이스의 복사 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="16916-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="16916-120">이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16916-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="16916-121">함께 *서버* 매개 변수는이 명령을 bk0b8kf658 서버로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="16916-122">예제 2: 서버의 모든 복사본 상태 가져오기 서버에 있는 모든 복사본의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="16916-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="16916-123">이 명령은 lpqd0zbr8y 이라는 서버에 있는 모든 활성 복사본의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16916-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="16916-124">변수</span><span class="sxs-lookup"><span data-stu-id="16916-124">PARAMETERS</span></span>

### <span data-ttu-id="16916-125">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="16916-125">-Database</span></span>
<span data-ttu-id="16916-126">원본 Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="16916-127">이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 복사본 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16916-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16916-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="16916-128">-DatabaseCopy</span></span>
<span data-ttu-id="16916-129">데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="16916-130">이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 복사본 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16916-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="16916-131">이 매개 변수는 파이프라인 입력을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-131">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16916-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16916-132">-DatabaseName</span></span>
<span data-ttu-id="16916-133">원본 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="16916-134">이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 복사본 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16916-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16916-135">-데이터 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="16916-135">-PartnerDatabase</span></span>
<span data-ttu-id="16916-136">보조 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="16916-137">Sys.dm_database_copies 동적 관리 보기에서이 데이터베이스를 찾을 수 없는 경우이 cmdlet은 빈 상태 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16916-138">-또는 서버</span><span class="sxs-lookup"><span data-stu-id="16916-138">-PartnerServer</span></span>
<span data-ttu-id="16916-139">대상 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="16916-140">Sys.dm_database_copies 동적 관리 보기에서이 서버를 찾을 수 없는 경우이 cmdlet은 빈 상태 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16916-141">-프로필</span><span class="sxs-lookup"><span data-stu-id="16916-141">-Profile</span></span>
<span data-ttu-id="16916-142">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16916-143">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="16916-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16916-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16916-144">-ServerName</span></span>
<span data-ttu-id="16916-145">데이터베이스 복사본이 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-145">Specifies the name of the server on which the database copy resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16916-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16916-146">CommonParameters</span></span>
<span data-ttu-id="16916-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16916-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16916-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16916-149">입력</span><span class="sxs-lookup"><span data-stu-id="16916-149">INPUTS</span></span>

### <span data-ttu-id="16916-150">WindowsAzure. SqlDatabase. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="16916-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="16916-151">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="16916-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="16916-152">출력</span><span class="sxs-lookup"><span data-stu-id="16916-152">OUTPUTS</span></span>

### <span data-ttu-id="16916-153">WindowsAzure. SqlDatabase. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="16916-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="16916-154">상속자</span><span class="sxs-lookup"><span data-stu-id="16916-154">NOTES</span></span>
* <span data-ttu-id="16916-155">인증:이 cmdlet을 사용 하려면 인증서 기반 인증이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="16916-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="16916-156">인증서 기반 인증을 사용 하 여 현재 구독을 설정 하는 방법에 대 한 예제는 New-AzureSqlDatabaseServerContext cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16916-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="16916-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16916-157">RELATED LINKS</span></span>

[<span data-ttu-id="16916-158">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="16916-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="16916-159">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="16916-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="16916-160">Azure SQL 데이터베이스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="16916-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="16916-161">시작-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="16916-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="16916-162">중지-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="16916-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


