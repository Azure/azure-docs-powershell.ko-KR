---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383DD041-78DC-4170-9529-1FD6F13BC178
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29cbf01629ef772fc41436f3916a2077c1535329
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046106"
---
# <span data-ttu-id="96cc6-101">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96cc6-101">Remove-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="96cc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="96cc6-103">Azure SQL 데이터베이스 서버에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-103">Removes a firewall rule from an Azure SQL Database server.</span></span>

## <span data-ttu-id="96cc6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96cc6-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96cc6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="96cc6-106">**AzureSqlDatabaseServerFirewallRule** cmdlet은 현재 구독의 Azure SQL 데이터베이스 서버 인스턴스에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-106">The **Remove-AzureSqlDatabaseServerFirewallRule** cmdlet removes a firewall rule from an instance of Azure SQL Database Server in the current subscription.</span></span>

## <span data-ttu-id="96cc6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="96cc6-107">EXAMPLES</span></span>

### <span data-ttu-id="96cc6-108">예제 1: 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="96cc6-108">Example 1: Remove a rule</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="96cc6-109">이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버에서 FirewallRule24 이라는 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-109">This command removes the firewall rule named FirewallRule24 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="96cc6-110">변수</span><span class="sxs-lookup"><span data-stu-id="96cc6-110">PARAMETERS</span></span>

### <span data-ttu-id="96cc6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="96cc6-111">-Force</span></span>
<span data-ttu-id="96cc6-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96cc6-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="96cc6-113">-Profile</span></span>
<span data-ttu-id="96cc6-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96cc6-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96cc6-116">-RuleName</span><span class="sxs-lookup"><span data-stu-id="96cc6-116">-RuleName</span></span>
<span data-ttu-id="96cc6-117">이 cmdlet이 제거 하는 방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-117">Specifies the name of the firewall rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96cc6-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96cc6-118">-ServerName</span></span>
<span data-ttu-id="96cc6-119">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-119">Specifies the name of a server.</span></span>
<span data-ttu-id="96cc6-120">이 cmdlet은이 매개 변수에서 지정 하는 서버에서 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-120">This cmdlet removes a firewall rule from the server that this parameter specifies.</span></span>

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

### <span data-ttu-id="96cc6-121">-확인</span><span class="sxs-lookup"><span data-stu-id="96cc6-121">-Confirm</span></span>
<span data-ttu-id="96cc6-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cc6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96cc6-123">-WhatIf</span></span>
<span data-ttu-id="96cc6-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96cc6-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cc6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cc6-126">CommonParameters</span></span>
<span data-ttu-id="96cc6-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cc6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cc6-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cc6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cc6-129">입력</span><span class="sxs-lookup"><span data-stu-id="96cc6-129">INPUTS</span></span>

### <span data-ttu-id="96cc6-130">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="96cc6-130">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="96cc6-131">출력</span><span class="sxs-lookup"><span data-stu-id="96cc6-131">OUTPUTS</span></span>

## <span data-ttu-id="96cc6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="96cc6-132">NOTES</span></span>

## <span data-ttu-id="96cc6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96cc6-133">RELATED LINKS</span></span>

[<span data-ttu-id="96cc6-134">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="96cc6-134">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="96cc6-135">방화벽 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="96cc6-135">Delete Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505706.aspx)

[<span data-ttu-id="96cc6-136">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="96cc6-136">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="96cc6-137">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96cc6-137">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="96cc6-138">새로운 AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96cc6-138">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="96cc6-139">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="96cc6-139">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


