---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045571"
---
# <span data-ttu-id="30330-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="30330-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="30330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30330-102">SYNOPSIS</span></span>
<span data-ttu-id="30330-103">Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30330-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="30330-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30330-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30330-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30330-105">DESCRIPTION</span></span>
<span data-ttu-id="30330-106">**AzureSqlDatabaseServer** cmdlet은 현재 구독에 있는 Azure SQL 데이터베이스 서버의 인스턴스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30330-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="30330-107">서버를 이름으로 지정 하면이 cmdlet은 해당 서버에 대 한 정보를 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30330-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="30330-108">그렇지 않으면 cmdlet이 모든 서버에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30330-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="30330-109">예제의</span><span class="sxs-lookup"><span data-stu-id="30330-109">EXAMPLES</span></span>

### <span data-ttu-id="30330-110">예제 1: 모든 서버에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="30330-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="30330-111">이 명령은 현재 구독에서 Azure SQL 데이터베이스 서버의 모든 인스턴스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30330-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="30330-112">예제 2: 특정 서버에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="30330-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="30330-113">이 명령은 lpqd0zbr8y 이라는 서버에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30330-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="30330-114">변수</span><span class="sxs-lookup"><span data-stu-id="30330-114">PARAMETERS</span></span>

### <span data-ttu-id="30330-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="30330-115">-Profile</span></span>
<span data-ttu-id="30330-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30330-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30330-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="30330-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30330-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30330-118">-ServerName</span></span>
<span data-ttu-id="30330-119">이 cmdlet이 제거할 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30330-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="30330-120">정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30330-120">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="30330-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30330-121">CommonParameters</span></span>
<span data-ttu-id="30330-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30330-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30330-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30330-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30330-124">입력</span><span class="sxs-lookup"><span data-stu-id="30330-124">INPUTS</span></span>

### <span data-ttu-id="30330-125">WindowsAzure. SqlDatabase. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="30330-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="30330-126">출력</span><span class="sxs-lookup"><span data-stu-id="30330-126">OUTPUTS</span></span>

### <span data-ttu-id="30330-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="30330-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="30330-128">상속자</span><span class="sxs-lookup"><span data-stu-id="30330-128">NOTES</span></span>

## <span data-ttu-id="30330-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30330-129">RELATED LINKS</span></span>

[<span data-ttu-id="30330-130">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="30330-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="30330-131">서버 목록 표시</span><span class="sxs-lookup"><span data-stu-id="30330-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="30330-132">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="30330-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="30330-133">새로운 AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="30330-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="30330-134">제거-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="30330-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="30330-135">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="30330-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


