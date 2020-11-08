---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048637"
---
# <span data-ttu-id="658d6-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="658d6-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="658d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="658d6-102">SYNOPSIS</span></span>
<span data-ttu-id="658d6-103">SQL 데이터베이스 서버에서 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="658d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="658d6-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="658d6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="658d6-105">DESCRIPTION</span></span>
<span data-ttu-id="658d6-106">**AzSqlServerFirewallRule** cmdlet은 지정 된 Azure SQL 데이터베이스 서버에서 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="658d6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="658d6-107">EXAMPLES</span></span>

### <span data-ttu-id="658d6-108">예제 1: 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="658d6-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="658d6-109">이 명령은 Server01 이라는 서버에서 Rule01 이라는 방화벽 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="658d6-110">변수</span><span class="sxs-lookup"><span data-stu-id="658d6-110">PARAMETERS</span></span>

### <span data-ttu-id="658d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658d6-111">-DefaultProfile</span></span>
<span data-ttu-id="658d6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="658d6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="658d6-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="658d6-113">-FirewallRuleName</span></span>
<span data-ttu-id="658d6-114">이 cmdlet이 삭제 하는 방화벽 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658d6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="658d6-115">-Force</span></span>
<span data-ttu-id="658d6-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658d6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="658d6-117">-ResourceGroupName</span></span>
<span data-ttu-id="658d6-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="658d6-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="658d6-119">-ServerName</span></span>
<span data-ttu-id="658d6-120">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="658d6-121">-확인</span><span class="sxs-lookup"><span data-stu-id="658d6-121">-Confirm</span></span>
<span data-ttu-id="658d6-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="658d6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="658d6-123">-WhatIf</span></span>
<span data-ttu-id="658d6-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="658d6-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="658d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658d6-126">CommonParameters</span></span>
<span data-ttu-id="658d6-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="658d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658d6-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="658d6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658d6-129">입력</span><span class="sxs-lookup"><span data-stu-id="658d6-129">INPUTS</span></span>

### <span data-ttu-id="658d6-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="658d6-130">System.String</span></span>

## <span data-ttu-id="658d6-131">출력</span><span class="sxs-lookup"><span data-stu-id="658d6-131">OUTPUTS</span></span>

### <span data-ttu-id="658d6-132">FirewallRule. AzureSqlServerFirewallRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="658d6-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="658d6-133">상속자</span><span class="sxs-lookup"><span data-stu-id="658d6-133">NOTES</span></span>

## <span data-ttu-id="658d6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="658d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="658d6-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="658d6-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="658d6-136">새로운 AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="658d6-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="658d6-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="658d6-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="658d6-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="658d6-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


