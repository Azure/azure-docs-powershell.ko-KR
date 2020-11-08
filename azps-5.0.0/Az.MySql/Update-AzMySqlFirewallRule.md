---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226106"
---
# <span data-ttu-id="83600-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="83600-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="83600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83600-102">SYNOPSIS</span></span>
<span data-ttu-id="83600-103">새 방화벽 규칙을 만들거나 기존 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="83600-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83600-104">SYNTAX</span></span>

### <span data-ttu-id="83600-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="83600-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83600-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="83600-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83600-107">Clivipaddressid</span><span class="sxs-lookup"><span data-stu-id="83600-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83600-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83600-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83600-109">설명은</span><span class="sxs-lookup"><span data-stu-id="83600-109">DESCRIPTION</span></span>
<span data-ttu-id="83600-110">새 방화벽 규칙을 만들거나 기존 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="83600-111">예제의</span><span class="sxs-lookup"><span data-stu-id="83600-111">EXAMPLES</span></span>

### <span data-ttu-id="83600-112">예제 1: 이름별로 MySql 방화벽 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="83600-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="83600-113">이 cmdlet은 이름으로 MySql 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="83600-114">예제 2: id를 기준으로 MySql 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="83600-115">이러한 cmdlet은 id를 기준으로 MySql 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="83600-116">예제 3:-ClientIPAddress를 기준으로 MySql 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="83600-117">이러한 cmdlet은 MySql 방화벽 규칙을-ClientIPAddress로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="83600-118">변수</span><span class="sxs-lookup"><span data-stu-id="83600-118">PARAMETERS</span></span>

### <span data-ttu-id="83600-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83600-119">-AsJob</span></span>
<span data-ttu-id="83600-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="83600-120">Run the command as a job</span></span>

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

### <span data-ttu-id="83600-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="83600-121">-ClientIPAddress</span></span>
<span data-ttu-id="83600-122">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="83600-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="83600-123">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83600-124">-DefaultProfile</span></span>
<span data-ttu-id="83600-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="83600-126">-EndIPAddress</span></span>
<span data-ttu-id="83600-127">서버 방화벽 규칙의 끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="83600-128">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83600-129">-InputObject</span></span>
<span data-ttu-id="83600-130">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83600-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83600-131">-이름</span><span class="sxs-lookup"><span data-stu-id="83600-131">-Name</span></span>
<span data-ttu-id="83600-132">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="83600-133">-NoWait</span></span>
<span data-ttu-id="83600-134">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="83600-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="83600-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83600-135">-ResourceGroupName</span></span>
<span data-ttu-id="83600-136">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-136">The name of the resource group.</span></span>
<span data-ttu-id="83600-137">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-137">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83600-138">-ServerName</span></span>
<span data-ttu-id="83600-139">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="83600-140">-StartIPAddress</span></span>
<span data-ttu-id="83600-141">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="83600-142">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83600-143">-SubscriptionId</span></span>
<span data-ttu-id="83600-144">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-144">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-145">-확인</span><span class="sxs-lookup"><span data-stu-id="83600-145">-Confirm</span></span>
<span data-ttu-id="83600-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83600-147">-WhatIf</span></span>
<span data-ttu-id="83600-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83600-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83600-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83600-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83600-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83600-150">CommonParameters</span></span>
<span data-ttu-id="83600-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83600-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="83600-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83600-153">입력</span><span class="sxs-lookup"><span data-stu-id="83600-153">INPUTS</span></span>

### <span data-ttu-id="83600-154">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="83600-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="83600-155">출력</span><span class="sxs-lookup"><span data-stu-id="83600-155">OUTPUTS</span></span>

### <span data-ttu-id="83600-156">Api20171201. IFirewallRule에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83600-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="83600-157">상속자</span><span class="sxs-lookup"><span data-stu-id="83600-157">NOTES</span></span>

<span data-ttu-id="83600-158">별칭과</span><span class="sxs-lookup"><span data-stu-id="83600-158">ALIASES</span></span>

<span data-ttu-id="83600-159">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="83600-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83600-160">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83600-161">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="83600-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83600-162">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="83600-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83600-163">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="83600-164">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="83600-165">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="83600-166">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="83600-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83600-167">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="83600-168">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="83600-169">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="83600-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="83600-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="83600-171">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="83600-172">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="83600-173">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83600-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="83600-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83600-174">RELATED LINKS</span></span>

