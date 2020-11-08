---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045570"
---
# <span data-ttu-id="d9813-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="d9813-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="d9813-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9813-102">SYNOPSIS</span></span>
<span data-ttu-id="d9813-103">Azure SQL 데이터베이스 서버에 대 한 할당량 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="d9813-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9813-104">SYNTAX</span></span>

### <span data-ttu-id="d9813-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="d9813-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d9813-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="d9813-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9813-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d9813-107">DESCRIPTION</span></span>
<span data-ttu-id="d9813-108">**AzureSqlDatabaseServerQuota** cmdlet은 지정 된 Azure SQL 데이터베이스 서버의 인스턴스에 대 한 할당량 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="d9813-109">연결 컨텍스트 또는 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="d9813-110">할당량 이름을 지정 하지 않으면이 cmdlet은 서버에 대 한 모든 할당량 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="d9813-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d9813-111">EXAMPLES</span></span>

### <span data-ttu-id="d9813-112">예제 1: 특정 할당량에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9813-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="d9813-113">이 명령은 $Context 변수에 저장 된 연결에서 지정한 Azure SQL 데이터베이스 서버에서 Premium_Databases 라는 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="d9813-114">예제 2: 모든 할당량에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9813-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="d9813-115">이 명령은 연결 $Context에 지정 된 서버에서 모든 할당량 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="d9813-116">변수</span><span class="sxs-lookup"><span data-stu-id="d9813-116">PARAMETERS</span></span>

### <span data-ttu-id="d9813-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="d9813-117">-ConnectionContext</span></span>
<span data-ttu-id="d9813-118">서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-118">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="d9813-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="d9813-119">-Profile</span></span>
<span data-ttu-id="d9813-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9813-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9813-122">-QuotaName</span><span class="sxs-lookup"><span data-stu-id="d9813-122">-QuotaName</span></span>
<span data-ttu-id="d9813-123">이 cmdlet이 가져오는 할당량 값의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9813-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d9813-124">-ServerName</span></span>
<span data-ttu-id="d9813-125">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-125">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="d9813-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9813-126">CommonParameters</span></span>
<span data-ttu-id="d9813-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9813-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9813-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9813-129">입력</span><span class="sxs-lookup"><span data-stu-id="d9813-129">INPUTS</span></span>

## <span data-ttu-id="d9813-130">출력</span><span class="sxs-lookup"><span data-stu-id="d9813-130">OUTPUTS</span></span>

### <span data-ttu-id="d9813-131">WindowsAzure. SqlDatabase?. ServerQuota []</span><span class="sxs-lookup"><span data-stu-id="d9813-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="d9813-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d9813-132">NOTES</span></span>
* <span data-ttu-id="d9813-133">인증:이 cmdlet은 SQL Server 인증 또는 인증서 기반 인증을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9813-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="d9813-134">인증 설정에 대 한 예제는 New-AzureSqlDatabaseServerContext cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d9813-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="d9813-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9813-135">RELATED LINKS</span></span>

[<span data-ttu-id="d9813-136">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="d9813-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="d9813-137">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="d9813-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="d9813-138">새로운 AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="d9813-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


