---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491866"
---
# <span data-ttu-id="af9b8-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="af9b8-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="af9b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="af9b8-103">기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="af9b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="af9b8-104">SYNTAX</span></span>

### <span data-ttu-id="af9b8-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="af9b8-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="af9b8-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="af9b8-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="af9b8-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="af9b8-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="af9b8-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="af9b8-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="af9b8-109">설명</span><span class="sxs-lookup"><span data-stu-id="af9b8-109">DESCRIPTION</span></span>
<span data-ttu-id="af9b8-110">기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="af9b8-111">예제</span><span class="sxs-lookup"><span data-stu-id="af9b8-111">EXAMPLES</span></span>

### <span data-ttu-id="af9b8-112">예제 1: 이름으로 MySql 방화벽 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="af9b8-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="af9b8-113">이 cmdlet은 이름으로 MySql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="af9b8-114">예제 2: ID로 MySql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="af9b8-115">이러한 cmdlet은 ID에 의해 MySql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="af9b8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af9b8-116">PARAMETERS</span></span>

### <span data-ttu-id="af9b8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af9b8-117">-AsJob</span></span>
<span data-ttu-id="af9b8-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="af9b8-118">Run the command as a job</span></span>

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

### <span data-ttu-id="af9b8-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="af9b8-119">-ClientIPAddress</span></span>
<span data-ttu-id="af9b8-120">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="af9b8-121">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="af9b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9b8-122">-DefaultProfile</span></span>
<span data-ttu-id="af9b8-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9b8-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="af9b8-124">-EndIPAddress</span></span>
<span data-ttu-id="af9b8-125">서버 방화벽 규칙의 최종 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="af9b8-126">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="af9b8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af9b8-127">-InputObject</span></span>
<span data-ttu-id="af9b8-128">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="af9b8-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="af9b8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="af9b8-129">-Name</span></span>
<span data-ttu-id="af9b8-130">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="af9b8-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="af9b8-131">-NoWait</span></span>
<span data-ttu-id="af9b8-132">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="af9b8-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="af9b8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9b8-133">-ResourceGroupName</span></span>
<span data-ttu-id="af9b8-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-134">The name of the resource group.</span></span>
<span data-ttu-id="af9b8-135">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="af9b8-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af9b8-136">-ServerName</span></span>
<span data-ttu-id="af9b8-137">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-137">The name of the server.</span></span>

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

### <span data-ttu-id="af9b8-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="af9b8-138">-StartIPAddress</span></span>
<span data-ttu-id="af9b8-139">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="af9b8-140">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="af9b8-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af9b8-141">-SubscriptionId</span></span>
<span data-ttu-id="af9b8-142">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="af9b8-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af9b8-143">-Confirm</span></span>
<span data-ttu-id="af9b8-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9b8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9b8-145">-WhatIf</span></span>
<span data-ttu-id="af9b8-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="af9b8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9b8-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9b8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9b8-148">CommonParameters</span></span>
<span data-ttu-id="af9b8-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9b8-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af9b8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9b8-151">입력</span><span class="sxs-lookup"><span data-stu-id="af9b8-151">INPUTS</span></span>

### <span data-ttu-id="af9b8-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="af9b8-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="af9b8-153">출력</span><span class="sxs-lookup"><span data-stu-id="af9b8-153">OUTPUTS</span></span>

### <span data-ttu-id="af9b8-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="af9b8-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="af9b8-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af9b8-155">NOTES</span></span>

<span data-ttu-id="af9b8-156">별칭</span><span class="sxs-lookup"><span data-stu-id="af9b8-156">ALIASES</span></span>

<span data-ttu-id="af9b8-157">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="af9b8-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af9b8-158">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af9b8-159">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="af9b8-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af9b8-160">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="af9b8-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af9b8-161">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="af9b8-162">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="af9b8-163">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="af9b8-164">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="af9b8-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af9b8-165">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="af9b8-166">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="af9b8-167">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="af9b8-168">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="af9b8-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="af9b8-170">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="af9b8-171">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="af9b8-172">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af9b8-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="af9b8-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af9b8-173">RELATED LINKS</span></span>

