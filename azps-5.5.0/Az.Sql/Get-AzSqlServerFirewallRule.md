---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201505"
---
# <span data-ttu-id="ee9eb-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ee9eb-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="ee9eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee9eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9eb-103">SQL 데이터베이스 서버에 대한 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="ee9eb-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee9eb-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee9eb-105">설명</span><span class="sxs-lookup"><span data-stu-id="ee9eb-105">DESCRIPTION</span></span>
<span data-ttu-id="ee9eb-106">**Get-AzSqlServerFirewallRule** cmdlet은 Azure SQL Database 서버에 대한 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="ee9eb-107">방화벽 규칙의 이름을 지정하면 이 cmdlet은 해당 특정 방화벽 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="ee9eb-108">예제</span><span class="sxs-lookup"><span data-stu-id="ee9eb-108">EXAMPLES</span></span>

### <span data-ttu-id="ee9eb-109">예제 1: 서버에 대한 모든 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="ee9eb-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="ee9eb-110">이 명령은 Server01이라는 서버에 대한 모든 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="ee9eb-111">예제 2: 필터링을 사용하여 서버에 대한 모든 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="ee9eb-111">Example 2: Get all rules for a server using filtering</span></span>
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

<span data-ttu-id="ee9eb-112">이 명령은 "규칙"으로 시작하는 Server01 서버에 대한 모든 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="ee9eb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee9eb-113">PARAMETERS</span></span>

### <span data-ttu-id="ee9eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9eb-114">-DefaultProfile</span></span>
<span data-ttu-id="ee9eb-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ee9eb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee9eb-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="ee9eb-116">-FirewallRuleName</span></span>
<span data-ttu-id="ee9eb-117">방화벽 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9eb-118">-ResourceGroupName</span></span>
<span data-ttu-id="ee9eb-119">리소스 그룹이 할당된 리소스 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="ee9eb-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ee9eb-120">-ServerName</span></span>
<span data-ttu-id="ee9eb-121">이름의 이름을 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="ee9eb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee9eb-122">-Confirm</span></span>
<span data-ttu-id="ee9eb-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee9eb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee9eb-124">-WhatIf</span></span>
<span data-ttu-id="ee9eb-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ee9eb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee9eb-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee9eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9eb-127">CommonParameters</span></span>
<span data-ttu-id="ee9eb-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9eb-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee9eb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9eb-130">입력</span><span class="sxs-lookup"><span data-stu-id="ee9eb-130">INPUTS</span></span>

### <span data-ttu-id="ee9eb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ee9eb-131">System.String</span></span>

## <span data-ttu-id="ee9eb-132">출력</span><span class="sxs-lookup"><span data-stu-id="ee9eb-132">OUTPUTS</span></span>

### <span data-ttu-id="ee9eb-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="ee9eb-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="ee9eb-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee9eb-134">NOTES</span></span>

## <span data-ttu-id="ee9eb-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee9eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="ee9eb-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ee9eb-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ee9eb-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ee9eb-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ee9eb-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ee9eb-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ee9eb-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ee9eb-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


