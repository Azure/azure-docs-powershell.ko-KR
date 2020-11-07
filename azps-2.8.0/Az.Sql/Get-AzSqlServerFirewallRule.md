---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: e6c6d48cbef24977ae6e2411749efbd913787b33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873911"
---
# <span data-ttu-id="47f12-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47f12-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="47f12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47f12-102">SYNOPSIS</span></span>
<span data-ttu-id="47f12-103">SQL 데이터베이스 서버에 대 한 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="47f12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47f12-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47f12-105">설명은</span><span class="sxs-lookup"><span data-stu-id="47f12-105">DESCRIPTION</span></span>
<span data-ttu-id="47f12-106">**AzSqlServerFirewallRule** Cmdlet은 Azure SQL 데이터베이스 서버에 대 한 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="47f12-107">방화벽 규칙의 이름을 지정 하는 경우이 cmdlet은 해당 특정 방화벽 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="47f12-108">예제의</span><span class="sxs-lookup"><span data-stu-id="47f12-108">EXAMPLES</span></span>

### <span data-ttu-id="47f12-109">예제 1: 서버에 대 한 모든 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="47f12-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="47f12-110">이 명령은 Server01 이라는 서버에 대 한 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="47f12-111">예제 2: 필터링을 사용 하 여 서버에 대 한 모든 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="47f12-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="47f12-112">이 명령은 "Rule"로 시작 하는 Server01 이라는 서버에 대 한 모든 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="47f12-113">변수</span><span class="sxs-lookup"><span data-stu-id="47f12-113">PARAMETERS</span></span>

### <span data-ttu-id="47f12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f12-114">-DefaultProfile</span></span>
<span data-ttu-id="47f12-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="47f12-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f12-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="47f12-116">-FirewallRuleName</span></span>
<span data-ttu-id="47f12-117">방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="47f12-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f12-118">-ResourceGroupName</span></span>
<span data-ttu-id="47f12-119">SQL Server에 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f12-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47f12-120">-ServerName</span></span>
<span data-ttu-id="47f12-121">SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-121">Specifies the name of the SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47f12-122">-확인</span><span class="sxs-lookup"><span data-stu-id="47f12-122">-Confirm</span></span>
<span data-ttu-id="47f12-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f12-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47f12-124">-WhatIf</span></span>
<span data-ttu-id="47f12-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47f12-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47f12-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f12-127">CommonParameters</span></span>
<span data-ttu-id="47f12-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47f12-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f12-129">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47f12-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f12-130">입력</span><span class="sxs-lookup"><span data-stu-id="47f12-130">INPUTS</span></span>

### <span data-ttu-id="47f12-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47f12-131">System.String</span></span>

## <span data-ttu-id="47f12-132">출력</span><span class="sxs-lookup"><span data-stu-id="47f12-132">OUTPUTS</span></span>

### <span data-ttu-id="47f12-133">FirewallRule. AzureSqlServerFirewallRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="47f12-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="47f12-134">상속자</span><span class="sxs-lookup"><span data-stu-id="47f12-134">NOTES</span></span>

## <span data-ttu-id="47f12-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47f12-135">RELATED LINKS</span></span>

[<span data-ttu-id="47f12-136">새로운 AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47f12-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="47f12-137">제거-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47f12-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="47f12-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="47f12-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="47f12-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="47f12-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


