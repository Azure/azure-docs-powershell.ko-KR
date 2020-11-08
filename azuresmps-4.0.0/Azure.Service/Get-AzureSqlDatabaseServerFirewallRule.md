---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045572"
---
# <span data-ttu-id="d50a2-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d50a2-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="d50a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d50a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d50a2-103">Azure SQL 데이터베이스 서버에 대 한 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="d50a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d50a2-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d50a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d50a2-105">DESCRIPTION</span></span>
<span data-ttu-id="d50a2-106">**AzureSqlDatabaseServerFirewallRule** Cmdlet은 Azure SQL 데이터베이스 서버의 인스턴스에 대 한 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="d50a2-107">이름을 기준으로 방화벽 규칙을 지정 하는 경우이 cmdlet은 해당 방화벽 규칙에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="d50a2-108">그렇지 않으면 cmdlet이 지정 된 Azure SQL 데이터베이스 서버의 모든 방화벽 규칙에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="d50a2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d50a2-109">EXAMPLES</span></span>

### <span data-ttu-id="d50a2-110">예제 1: 서버에서 모든 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="d50a2-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="d50a2-111">이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버의 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="d50a2-112">예제 2: 이름을 사용 하 여 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="d50a2-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="d50a2-113">이 명령은 lpqd0zbr8y 이라는 서버에서 FirewallRule24 이라는 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="d50a2-114">변수</span><span class="sxs-lookup"><span data-stu-id="d50a2-114">PARAMETERS</span></span>

### <span data-ttu-id="d50a2-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="d50a2-115">-Profile</span></span>
<span data-ttu-id="d50a2-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d50a2-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d50a2-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d50a2-118">-RuleName</span></span>
<span data-ttu-id="d50a2-119">이 cmdlet이 가져오는 방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d50a2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d50a2-120">-ServerName</span></span>
<span data-ttu-id="d50a2-121">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-121">Specifies the name of a server.</span></span>
<span data-ttu-id="d50a2-122">이 cmdlet은이 매개 변수에서 지정 하는 서버에서 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="d50a2-123">정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50a2-124">CommonParameters</span></span>
<span data-ttu-id="d50a2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d50a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50a2-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d50a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50a2-127">입력</span><span class="sxs-lookup"><span data-stu-id="d50a2-127">INPUTS</span></span>

### <span data-ttu-id="d50a2-128">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="d50a2-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="d50a2-129">출력</span><span class="sxs-lookup"><span data-stu-id="d50a2-129">OUTPUTS</span></span>

### <span data-ttu-id="d50a2-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="d50a2-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="d50a2-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d50a2-131">NOTES</span></span>

## <span data-ttu-id="d50a2-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d50a2-132">RELATED LINKS</span></span>

[<span data-ttu-id="d50a2-133">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="d50a2-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="d50a2-134">방화벽 규칙 목록 표시</span><span class="sxs-lookup"><span data-stu-id="d50a2-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="d50a2-135">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="d50a2-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="d50a2-136">새로운 AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d50a2-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="d50a2-137">제거-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d50a2-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="d50a2-138">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d50a2-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


