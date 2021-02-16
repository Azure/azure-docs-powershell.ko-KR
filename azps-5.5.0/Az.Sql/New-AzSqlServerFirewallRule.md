---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178369"
---
# <span data-ttu-id="ac244-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ac244-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="ac244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac244-102">SYNOPSIS</span></span>
<span data-ttu-id="ac244-103">SQL 데이터베이스 서버에 대한 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="ac244-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac244-104">SYNTAX</span></span>

### <span data-ttu-id="ac244-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac244-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac244-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac244-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac244-107">설명</span><span class="sxs-lookup"><span data-stu-id="ac244-107">DESCRIPTION</span></span>
<span data-ttu-id="ac244-108">**New-AzSqlServerFirewallRule** cmdlet은 지정된 Azure SQL 데이터베이스 서버에 대한 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="ac244-109">예제</span><span class="sxs-lookup"><span data-stu-id="ac244-109">EXAMPLES</span></span>

### <span data-ttu-id="ac244-110">예제 1: 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ac244-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="ac244-111">이 명령은 Server01이라는 서버에 Rule01이라는 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="ac244-112">규칙에는 지정된 시작 및 끝 IP 주소가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="ac244-113">예제 2: 모든 Azure IP 주소가 서버에 액세스할 수 있도록 하는 방화벽 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ac244-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="ac244-114">이 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 Server01이라는 서버에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="ac244-115">*AllowAllAzureIPs* 매개 변수가 사용 됐기 때문에 방화벽 규칙은 모든 Azure IP 주소가 서버에 액세스할 수 있도록 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="ac244-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac244-116">PARAMETERS</span></span>

### <span data-ttu-id="ac244-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="ac244-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="ac244-118">이 방화벽 규칙은 모든 Azure IP 주소가 서버에 액세스할 수 있도록 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="ac244-119">*FirewallRuleName,* *StartIpAddress* 및 *EndIpAddress* 매개 변수를 사용하려는 경우 이 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-119">You cannot use this parameter if you intend to use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="ac244-120">Azure IP가 서버에 액세스할 수 있도록 허용하려는 경우 *FirewallRuleName,* *StartIpAddress 및 EndIpAddress* 매개  변수를 사용하지 않는 별도의 cmdlet 호출에 이 매개 변수를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac244-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac244-121">-DefaultProfile</span></span>
<span data-ttu-id="ac244-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ac244-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac244-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ac244-123">-EndIpAddress</span></span>
<span data-ttu-id="ac244-124">이 규칙에 대한 IP 주소 범위의 끝 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac244-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="ac244-125">-FirewallRuleName</span></span>
<span data-ttu-id="ac244-126">새 방화벽 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac244-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac244-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac244-128">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ac244-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ac244-129">-ServerName</span></span>
<span data-ttu-id="ac244-130">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-130">Specifies the name of a server.</span></span>
<span data-ttu-id="ac244-131">정식 DNS 이름이 아닌 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="ac244-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ac244-132">-StartIpAddress</span></span>
<span data-ttu-id="ac244-133">방화벽 규칙에 대한 IP 주소 범위의 시작 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac244-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac244-134">-Confirm</span></span>
<span data-ttu-id="ac244-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac244-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac244-136">-WhatIf</span></span>
<span data-ttu-id="ac244-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ac244-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac244-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac244-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac244-139">CommonParameters</span></span>
<span data-ttu-id="ac244-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac244-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac244-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac244-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac244-142">입력</span><span class="sxs-lookup"><span data-stu-id="ac244-142">INPUTS</span></span>

### <span data-ttu-id="ac244-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ac244-143">System.String</span></span>

## <span data-ttu-id="ac244-144">출력</span><span class="sxs-lookup"><span data-stu-id="ac244-144">OUTPUTS</span></span>

### <span data-ttu-id="ac244-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="ac244-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="ac244-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac244-146">NOTES</span></span>

## <span data-ttu-id="ac244-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac244-147">RELATED LINKS</span></span>

[<span data-ttu-id="ac244-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ac244-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ac244-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ac244-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ac244-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ac244-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ac244-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ac244-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


