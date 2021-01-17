---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489448"
---
# <span data-ttu-id="c07e9-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c07e9-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="c07e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c07e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c07e9-103">Azure SQL 데이터베이스 서버에서 방화벽 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="c07e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="c07e9-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c07e9-105">설명</span><span class="sxs-lookup"><span data-stu-id="c07e9-105">DESCRIPTION</span></span>
<span data-ttu-id="c07e9-106">**Set-AzSqlServerFirewallRule** cmdlet은 Azure SQL 데이터베이스 서버에서 방화벽 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="c07e9-107">예제</span><span class="sxs-lookup"><span data-stu-id="c07e9-107">EXAMPLES</span></span>

### <span data-ttu-id="c07e9-108">예제 1: 방화벽 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="c07e9-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="c07e9-109">이 명령은 Server01이라는 서버에서 Rule01이라는 방화벽 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="c07e9-110">이 명령은 시작 및 끝 IP 주소를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="c07e9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c07e9-111">PARAMETERS</span></span>

### <span data-ttu-id="c07e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07e9-112">-DefaultProfile</span></span>
<span data-ttu-id="c07e9-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c07e9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c07e9-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07e9-114">-EndIpAddress</span></span>
<span data-ttu-id="c07e9-115">이 규칙에 대한 IP 주소 범위의 끝 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07e9-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="c07e9-116">-FirewallRuleName</span></span>
<span data-ttu-id="c07e9-117">이 cmdlet이 수정하는 방화벽 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c07e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c07e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="c07e9-119">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c07e9-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c07e9-120">-ServerName</span></span>
<span data-ttu-id="c07e9-121">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c07e9-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c07e9-122">-StartIpAddress</span></span>
<span data-ttu-id="c07e9-123">방화벽 규칙에 대한 IP 주소 범위의 시작 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07e9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c07e9-124">-Confirm</span></span>
<span data-ttu-id="c07e9-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c07e9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c07e9-126">-WhatIf</span></span>
<span data-ttu-id="c07e9-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c07e9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c07e9-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c07e9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07e9-129">CommonParameters</span></span>
<span data-ttu-id="c07e9-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c07e9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07e9-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c07e9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07e9-132">입력</span><span class="sxs-lookup"><span data-stu-id="c07e9-132">INPUTS</span></span>

### <span data-ttu-id="c07e9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c07e9-133">System.String</span></span>

## <span data-ttu-id="c07e9-134">출력</span><span class="sxs-lookup"><span data-stu-id="c07e9-134">OUTPUTS</span></span>

### <span data-ttu-id="c07e9-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="c07e9-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="c07e9-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c07e9-136">NOTES</span></span>

## <span data-ttu-id="c07e9-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c07e9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c07e9-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c07e9-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="c07e9-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c07e9-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="c07e9-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c07e9-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="c07e9-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c07e9-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


