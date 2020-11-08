---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045863"
---
# <span data-ttu-id="281f3-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="281f3-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="281f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="281f3-102">SYNOPSIS</span></span>
<span data-ttu-id="281f3-103">Azure SQL 데이터베이스 서버의 기존 방화벽 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="281f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="281f3-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="281f3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="281f3-105">DESCRIPTION</span></span>
<span data-ttu-id="281f3-106">**AzureSqlDatabaseServerFirewallRule** cmdlet은 지정 된 Azure SQL 데이터베이스 서버의 인스턴스에서 기존 방화벽 규칙의 시작 ip 주소 및 종료 ip 주소 값을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="281f3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="281f3-107">EXAMPLES</span></span>

### <span data-ttu-id="281f3-108">예제 1: 방화벽 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="281f3-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="281f3-109">이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버에서 FirewallRule24 이라는 방화벽 규칙의 시작 IP 주소 및 종료 IP 주소를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="281f3-110">변수</span><span class="sxs-lookup"><span data-stu-id="281f3-110">PARAMETERS</span></span>

### <span data-ttu-id="281f3-111">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="281f3-111">-EndIpAddress</span></span>
<span data-ttu-id="281f3-112">이 규칙에 대 한 IP 주소 범위의 끝 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-112">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="281f3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="281f3-113">-Force</span></span>
<span data-ttu-id="281f3-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="281f3-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="281f3-115">-Profile</span></span>
<span data-ttu-id="281f3-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="281f3-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="281f3-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="281f3-118">-RuleName</span></span>
<span data-ttu-id="281f3-119">이 cmdlet이 수정 하는 방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="281f3-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="281f3-120">-ServerName</span></span>
<span data-ttu-id="281f3-121">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-121">Specifies the name of a server.</span></span>
<span data-ttu-id="281f3-122">이 cmdlet은이 cmdlet이 지정 하는 서버에서 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="281f3-123">정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="281f3-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="281f3-124">-StartIpAddress</span></span>
<span data-ttu-id="281f3-125">방화벽 규칙에 대 한 IP 주소 범위의 시작 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="281f3-126">-확인</span><span class="sxs-lookup"><span data-stu-id="281f3-126">-Confirm</span></span>
<span data-ttu-id="281f3-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="281f3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="281f3-128">-WhatIf</span></span>
<span data-ttu-id="281f3-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="281f3-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="281f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281f3-131">CommonParameters</span></span>
<span data-ttu-id="281f3-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281f3-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="281f3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281f3-134">입력</span><span class="sxs-lookup"><span data-stu-id="281f3-134">INPUTS</span></span>

### <span data-ttu-id="281f3-135">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="281f3-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="281f3-136">출력</span><span class="sxs-lookup"><span data-stu-id="281f3-136">OUTPUTS</span></span>

### <span data-ttu-id="281f3-137">WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="281f3-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="281f3-138">상속자</span><span class="sxs-lookup"><span data-stu-id="281f3-138">NOTES</span></span>

## <span data-ttu-id="281f3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="281f3-139">RELATED LINKS</span></span>

[<span data-ttu-id="281f3-140">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="281f3-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="281f3-141">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="281f3-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="281f3-142">방화벽 규칙 설정</span><span class="sxs-lookup"><span data-stu-id="281f3-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="281f3-143">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="281f3-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="281f3-144">새로운 AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="281f3-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="281f3-145">제거-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="281f3-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


