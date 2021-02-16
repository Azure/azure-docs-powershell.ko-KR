---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402425"
---
# <span data-ttu-id="e1c12-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e1c12-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="e1c12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c12-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c12-103">복사 관계의 상태를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="e1c12-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1c12-104">SYNTAX</span></span>

### <span data-ttu-id="e1c12-105">ByServerNameOnly(기본값)</span><span class="sxs-lookup"><span data-stu-id="e1c12-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e1c12-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e1c12-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c12-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="e1c12-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e1c12-108">설명</span><span class="sxs-lookup"><span data-stu-id="e1c12-108">DESCRIPTION</span></span>
<span data-ttu-id="e1c12-109">**Get-AzureSqlDatabaseCopy** cmdlet은 하나 이상의 활성 복사 관계의 상태를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="e1c12-110">cmdlet을 실행한 후 이 cmdlet을 Start-AzureSqlDatabaseCopy Stop-AzureSqlDatabaseCopy 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="e1c12-111">특정 복사 관계, 모든 복사 관계 또는 특정 대상 서버의 모든 복사본과 같은 필터링된 복사 관계 목록을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="e1c12-112">원본 또는 대상 데이터베이스를 호스트하는 서버에서 이 cmdlet을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="e1c12-113">이 cmdlet은 동기식입니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="e1c12-114">cmdlet은 상태 개체를 반환할 때까지 Azure PowerShell 콘솔을 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="e1c12-115">*PartnerServer 및* *PartnerDatabase* 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="e1c12-116">매개 변수를 지정하지 않으면 이 cmdlet은 결과 테이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="e1c12-117">특정 데이터베이스에 대한 상태만 확인하려면 두 매개 변수를 모두 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="e1c12-118">예제</span><span class="sxs-lookup"><span data-stu-id="e1c12-118">EXAMPLES</span></span>

### <span data-ttu-id="e1c12-119">예제 1: 데이터베이스의 복사 상태 확인</span><span class="sxs-lookup"><span data-stu-id="e1c12-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="e1c12-120">이 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="e1c12-121">*PartnerServer 매개* 변수는 이 명령을 bk0b8kf658 서버로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="e1c12-122">예제 2: serverGet 서버의 모든 복사본 상태 확인</span><span class="sxs-lookup"><span data-stu-id="e1c12-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="e1c12-123">이 명령은 lpqd0zbr8y라는 서버에서 모든 활성 복사본의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="e1c12-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1c12-124">PARAMETERS</span></span>

### <span data-ttu-id="e1c12-125">-Database</span><span class="sxs-lookup"><span data-stu-id="e1c12-125">-Database</span></span>
<span data-ttu-id="e1c12-126">원본 Azure SQL 데이터베이스를 나타내는 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="e1c12-127">이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1c12-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e1c12-128">-DatabaseCopy</span></span>
<span data-ttu-id="e1c12-129">데이터베이스를 나타내는 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="e1c12-130">이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="e1c12-131">이 매개 변수는 파이프라인 입력을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="e1c12-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1c12-132">-DatabaseName</span></span>
<span data-ttu-id="e1c12-133">원본 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="e1c12-134">이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1c12-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="e1c12-135">-PartnerDatabase</span></span>
<span data-ttu-id="e1c12-136">보조 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="e1c12-137">이 데이터베이스를 동적 관리 sys.dm_database_copies 찾을 수 없는 경우 이 cmdlet은 빈 상태 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="e1c12-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="e1c12-138">-PartnerServer</span></span>
<span data-ttu-id="e1c12-139">대상 데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="e1c12-140">이 서버가 동적 관리 sys.dm_database_copies 없는 경우 이 cmdlet은 빈 상태 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="e1c12-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="e1c12-141">-Profile</span></span>
<span data-ttu-id="e1c12-142">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1c12-143">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1c12-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e1c12-144">-ServerName</span></span>
<span data-ttu-id="e1c12-145">데이터베이스 복사본이 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="e1c12-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c12-146">CommonParameters</span></span>
<span data-ttu-id="e1c12-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c12-148">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e1c12-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c12-149">입력</span><span class="sxs-lookup"><span data-stu-id="e1c12-149">INPUTS</span></span>

### <span data-ttu-id="e1c12-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e1c12-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="e1c12-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="e1c12-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="e1c12-152">출력</span><span class="sxs-lookup"><span data-stu-id="e1c12-152">OUTPUTS</span></span>

### <span data-ttu-id="e1c12-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e1c12-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="e1c12-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1c12-154">NOTES</span></span>
* <span data-ttu-id="e1c12-155">인증: 이 cmdlet에는 인증서 기반 인증이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e1c12-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="e1c12-156">인증서 기반 인증을 사용하여 현재 구독을 설정하는 방법의 예제는 New-AzureSqlDatabaseServerContext cmdlet을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e1c12-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="e1c12-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1c12-157">RELATED LINKS</span></span>

[<span data-ttu-id="e1c12-158">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="e1c12-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e1c12-159">Azure SQL 데이터베이스에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="e1c12-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[<span data-ttu-id="e1c12-160">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e1c12-160">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="e1c12-161">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e1c12-161">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


