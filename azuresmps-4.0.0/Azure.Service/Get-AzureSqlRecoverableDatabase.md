---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046559"
---
# <span data-ttu-id="78c7f-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="78c7f-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="78c7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="78c7f-103">지정 된 서버에서 복구 가능한 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="78c7f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78c7f-104">SYNTAX</span></span>

### <span data-ttu-id="78c7f-105">AllDatabasesOnGivenServer (기본값)</span><span class="sxs-lookup"><span data-stu-id="78c7f-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="78c7f-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="78c7f-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="78c7f-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="78c7f-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="78c7f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="78c7f-108">DESCRIPTION</span></span>
<span data-ttu-id="78c7f-109">**AzureSqlRecoverableDatabase** cmdlet은 지정 된 서버에서 복구 가능한 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="78c7f-110">이 cmdlet은 복구 가능한 특정 데이터베이스 또는 서버의 복구 가능한 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="78c7f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="78c7f-111">EXAMPLES</span></span>

### <span data-ttu-id="78c7f-112">예제 1: 복구 가능한 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="78c7f-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="78c7f-113">이 명령은 Server01 이라는 서버의 복구 가능한 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="78c7f-114">예제 2: 복구 가능한 특정 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="78c7f-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="78c7f-115">이 명령은 Server01 이라는 서버에서 Database17 이라는 데이터베이스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="78c7f-116">변수</span><span class="sxs-lookup"><span data-stu-id="78c7f-116">PARAMETERS</span></span>

### <span data-ttu-id="78c7f-117">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="78c7f-117">-Database</span></span>
<span data-ttu-id="78c7f-118">이 cmdlet이 가져오는 복구 가능한 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78c7f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78c7f-119">-DatabaseName</span></span>
<span data-ttu-id="78c7f-120">이 cmdlet이 가져오는 복구 가능한 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c7f-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="78c7f-121">-Profile</span></span>
<span data-ttu-id="78c7f-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78c7f-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78c7f-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78c7f-124">-ServerName</span></span>
<span data-ttu-id="78c7f-125">이 cmdlet이 복구 가능한 데이터베이스를 가져오는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c7f-126">CommonParameters</span></span>
<span data-ttu-id="78c7f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c7f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c7f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c7f-129">입력</span><span class="sxs-lookup"><span data-stu-id="78c7f-129">INPUTS</span></span>

### <span data-ttu-id="78c7f-130">WindowsAzure를 RecoverableDatabase 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="78c7f-131">출력</span><span class="sxs-lookup"><span data-stu-id="78c7f-131">OUTPUTS</span></span>

### <span data-ttu-id="78c7f-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="78c7f-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="78c7f-133">상속자</span><span class="sxs-lookup"><span data-stu-id="78c7f-133">NOTES</span></span>
* <span data-ttu-id="78c7f-134">이 cmdlet을 실행 하려면 인증서 기반 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="78c7f-135">이 cmdlet을 실행 하는 컴퓨터에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c7f-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="78c7f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78c7f-136">RELATED LINKS</span></span>

[<span data-ttu-id="78c7f-137">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="78c7f-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="78c7f-138">복구 가능한 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="78c7f-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="78c7f-139">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="78c7f-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="78c7f-140">시작-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="78c7f-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


