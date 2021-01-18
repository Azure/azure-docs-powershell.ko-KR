---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493157"
---
# <span data-ttu-id="da09e-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da09e-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="da09e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da09e-102">SYNOPSIS</span></span>
<span data-ttu-id="da09e-103">새 방화벽 규칙을 생성하거나 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="da09e-104">구문</span><span class="sxs-lookup"><span data-stu-id="da09e-104">SYNTAX</span></span>

### <span data-ttu-id="da09e-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="da09e-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da09e-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="da09e-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da09e-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="da09e-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="da09e-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="da09e-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="da09e-109">설명</span><span class="sxs-lookup"><span data-stu-id="da09e-109">DESCRIPTION</span></span>
<span data-ttu-id="da09e-110">새 방화벽 규칙을 생성하거나 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="da09e-111">예제</span><span class="sxs-lookup"><span data-stu-id="da09e-111">EXAMPLES</span></span>

### <span data-ttu-id="da09e-112">예제 1: 이름으로 PostgreSql 방화벽 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="da09e-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="da09e-113">이 cmdlet은 PostgreSql 방화벽 규칙을 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="da09e-114">예제 2: ID로 PostgreSql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="da09e-115">이러한 cmdlet은 ID에 의해 PostgreSql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="da09e-116">예제 3: -ClientIPAddress로 PostgreSql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="da09e-117">이러한 cmdlet은 -ClientIPAddress에 의해 PostgreSql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="da09e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da09e-118">PARAMETERS</span></span>

### <span data-ttu-id="da09e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da09e-119">-AsJob</span></span>
<span data-ttu-id="da09e-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="da09e-120">Run the command as a job</span></span>

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

### <span data-ttu-id="da09e-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="da09e-121">-ClientIPAddress</span></span>
<span data-ttu-id="da09e-122">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="da09e-123">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da09e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da09e-124">-DefaultProfile</span></span>
<span data-ttu-id="da09e-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da09e-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="da09e-126">-EndIPAddress</span></span>
<span data-ttu-id="da09e-127">서버 방화벽 규칙의 최종 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="da09e-128">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da09e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da09e-129">-InputObject</span></span>
<span data-ttu-id="da09e-130">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="da09e-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da09e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="da09e-131">-Name</span></span>
<span data-ttu-id="da09e-132">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="da09e-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="da09e-133">-NoWait</span></span>
<span data-ttu-id="da09e-134">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="da09e-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da09e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da09e-135">-ResourceGroupName</span></span>
<span data-ttu-id="da09e-136">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-136">The name of the resource group.</span></span>
<span data-ttu-id="da09e-137">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="da09e-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da09e-138">-ServerName</span></span>
<span data-ttu-id="da09e-139">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-139">The name of the server.</span></span>

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

### <span data-ttu-id="da09e-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="da09e-140">-StartIPAddress</span></span>
<span data-ttu-id="da09e-141">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="da09e-142">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="da09e-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da09e-143">-SubscriptionId</span></span>
<span data-ttu-id="da09e-144">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="da09e-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da09e-145">-Confirm</span></span>
<span data-ttu-id="da09e-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da09e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da09e-147">-WhatIf</span></span>
<span data-ttu-id="da09e-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="da09e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da09e-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da09e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da09e-150">CommonParameters</span></span>
<span data-ttu-id="da09e-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da09e-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da09e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da09e-153">입력</span><span class="sxs-lookup"><span data-stu-id="da09e-153">INPUTS</span></span>

### <span data-ttu-id="da09e-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="da09e-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="da09e-155">출력</span><span class="sxs-lookup"><span data-stu-id="da09e-155">OUTPUTS</span></span>

### <span data-ttu-id="da09e-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da09e-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="da09e-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da09e-157">NOTES</span></span>

<span data-ttu-id="da09e-158">별칭</span><span class="sxs-lookup"><span data-stu-id="da09e-158">ALIASES</span></span>

<span data-ttu-id="da09e-159">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="da09e-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="da09e-160">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="da09e-161">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="da09e-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="da09e-162">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="da09e-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="da09e-163">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="da09e-164">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="da09e-165">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="da09e-166">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="da09e-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="da09e-167">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="da09e-168">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="da09e-169">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="da09e-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="da09e-171">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="da09e-172">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="da09e-173">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da09e-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="da09e-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da09e-174">RELATED LINKS</span></span>

