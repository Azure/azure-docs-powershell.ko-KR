---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 2365cb4f6dedeb0620a2bdb1c1549eb0cd25d0c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992399"
---
# <span data-ttu-id="51804-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51804-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="51804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51804-102">SYNOPSIS</span></span>
<span data-ttu-id="51804-103">Azure SQL 데이터베이스 서버에서 방화벽 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="51804-104">구문</span><span class="sxs-lookup"><span data-stu-id="51804-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51804-105">설명</span><span class="sxs-lookup"><span data-stu-id="51804-105">DESCRIPTION</span></span>
<span data-ttu-id="51804-106">**Set-AzSqlServerFirewallRule** cmdlet은 Azure SQL 데이터베이스 서버에서 방화벽 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="51804-107">예제</span><span class="sxs-lookup"><span data-stu-id="51804-107">EXAMPLES</span></span>

### <span data-ttu-id="51804-108">예제 1: 방화벽 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="51804-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="51804-109">이 명령은 Server01이라는 서버에서 Rule01이라는 방화벽 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="51804-110">명령은 시작 및 끝 IP 주소를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="51804-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="51804-111">PARAMETERS</span></span>

### <span data-ttu-id="51804-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51804-112">-DefaultProfile</span></span>
<span data-ttu-id="51804-113">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="51804-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51804-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="51804-114">-EndIpAddress</span></span>
<span data-ttu-id="51804-115">이 규칙에 대한 IP 주소 범위의 끝 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="51804-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="51804-116">-FirewallRuleName</span></span>
<span data-ttu-id="51804-117">이 cmdlet이 수정하는 방화벽 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="51804-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51804-118">-ResourceGroupName</span></span>
<span data-ttu-id="51804-119">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="51804-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="51804-120">-ServerName</span></span>
<span data-ttu-id="51804-121">서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="51804-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="51804-122">-StartIpAddress</span></span>
<span data-ttu-id="51804-123">방화벽 규칙에 대한 IP 주소 범위의 시작 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="51804-124">-확인</span><span class="sxs-lookup"><span data-stu-id="51804-124">-Confirm</span></span>
<span data-ttu-id="51804-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="51804-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51804-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51804-126">-WhatIf</span></span>
<span data-ttu-id="51804-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="51804-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51804-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51804-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51804-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51804-129">CommonParameters</span></span>
<span data-ttu-id="51804-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51804-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51804-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51804-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51804-132">입력</span><span class="sxs-lookup"><span data-stu-id="51804-132">INPUTS</span></span>

### <span data-ttu-id="51804-133">System.String</span><span class="sxs-lookup"><span data-stu-id="51804-133">System.String</span></span>

## <span data-ttu-id="51804-134">출력</span><span class="sxs-lookup"><span data-stu-id="51804-134">OUTPUTS</span></span>

### <span data-ttu-id="51804-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="51804-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="51804-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51804-136">NOTES</span></span>

## <span data-ttu-id="51804-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51804-137">RELATED LINKS</span></span>

[<span data-ttu-id="51804-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51804-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="51804-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51804-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="51804-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51804-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="51804-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="51804-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


