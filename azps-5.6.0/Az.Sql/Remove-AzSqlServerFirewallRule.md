---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 0b76faf383e8cd3c70d6ff1e7e38de367850ac8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967355"
---
# <span data-ttu-id="10a60-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10a60-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="10a60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a60-102">SYNOPSIS</span></span>
<span data-ttu-id="10a60-103">데이터베이스 서버에서 방화벽 SQL 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="10a60-104">구문</span><span class="sxs-lookup"><span data-stu-id="10a60-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10a60-105">설명</span><span class="sxs-lookup"><span data-stu-id="10a60-105">DESCRIPTION</span></span>
<span data-ttu-id="10a60-106">**Remove-AzSqlServerFirewallRule** cmdlet은 지정된 Azure SQL 데이터베이스 서버에서 방화벽 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="10a60-107">예제</span><span class="sxs-lookup"><span data-stu-id="10a60-107">EXAMPLES</span></span>

### <span data-ttu-id="10a60-108">예제 1: 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="10a60-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="10a60-109">이 명령은 Server01이라는 서버에서 Rule01이라는 방화벽 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="10a60-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="10a60-110">PARAMETERS</span></span>

### <span data-ttu-id="10a60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a60-111">-DefaultProfile</span></span>
<span data-ttu-id="10a60-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="10a60-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10a60-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="10a60-113">-FirewallRuleName</span></span>
<span data-ttu-id="10a60-114">이 cmdlet이 삭제하는 방화벽 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="10a60-115">-Force</span><span class="sxs-lookup"><span data-stu-id="10a60-115">-Force</span></span>
<span data-ttu-id="10a60-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10a60-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a60-117">-ResourceGroupName</span></span>
<span data-ttu-id="10a60-118">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="10a60-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10a60-119">-ServerName</span></span>
<span data-ttu-id="10a60-120">서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="10a60-121">-확인</span><span class="sxs-lookup"><span data-stu-id="10a60-121">-Confirm</span></span>
<span data-ttu-id="10a60-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a60-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a60-123">-WhatIf</span></span>
<span data-ttu-id="10a60-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10a60-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a60-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a60-126">CommonParameters</span></span>
<span data-ttu-id="10a60-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10a60-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a60-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10a60-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a60-129">입력</span><span class="sxs-lookup"><span data-stu-id="10a60-129">INPUTS</span></span>

### <span data-ttu-id="10a60-130">System.String</span><span class="sxs-lookup"><span data-stu-id="10a60-130">System.String</span></span>

## <span data-ttu-id="10a60-131">출력</span><span class="sxs-lookup"><span data-stu-id="10a60-131">OUTPUTS</span></span>

### <span data-ttu-id="10a60-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="10a60-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="10a60-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10a60-133">NOTES</span></span>

## <span data-ttu-id="10a60-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10a60-134">RELATED LINKS</span></span>

[<span data-ttu-id="10a60-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10a60-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="10a60-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10a60-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="10a60-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10a60-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="10a60-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="10a60-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


