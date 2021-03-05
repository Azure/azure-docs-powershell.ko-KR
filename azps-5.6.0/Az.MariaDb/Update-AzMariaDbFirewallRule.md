---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 850b1cfae70abb3e1225f9ff7bcda937dc0f0db4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003883"
---
# <span data-ttu-id="e81ba-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e81ba-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="e81ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e81ba-102">SYNOPSIS</span></span>
<span data-ttu-id="e81ba-103">새 방화벽 규칙을 만들고 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="e81ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="e81ba-104">SYNTAX</span></span>

### <span data-ttu-id="e81ba-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e81ba-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e81ba-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="e81ba-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e81ba-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e81ba-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e81ba-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e81ba-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e81ba-109">설명</span><span class="sxs-lookup"><span data-stu-id="e81ba-109">DESCRIPTION</span></span>
<span data-ttu-id="e81ba-110">새 방화벽 규칙을 만들고 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="e81ba-111">예제</span><span class="sxs-lookup"><span data-stu-id="e81ba-111">EXAMPLES</span></span>

### <span data-ttu-id="e81ba-112">예제 1: MariaDB 방화벽 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="e81ba-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="e81ba-113">이 명령은 MariaDB 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="e81ba-114">예제 2: ID에 의해 MariaDB 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="e81ba-115">cmdlet은 ID에 의해 MariaDB 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="e81ba-116">예제 3: -ClientIPAddress에 의해 MariaDB 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="e81ba-117">cmdlet은 -ClientIPAddress에 의해 MariaDB 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="e81ba-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e81ba-118">PARAMETERS</span></span>

### <span data-ttu-id="e81ba-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e81ba-119">-AsJob</span></span>
<span data-ttu-id="e81ba-120">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-120">Run the command as a job</span></span>

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

### <span data-ttu-id="e81ba-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="e81ba-121">-ClientIPAddress</span></span>
<span data-ttu-id="e81ba-122">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="e81ba-123">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e81ba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81ba-124">-DefaultProfile</span></span>
<span data-ttu-id="e81ba-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e81ba-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="e81ba-126">-EndIPAddress</span></span>
<span data-ttu-id="e81ba-127">서버 방화벽 규칙의 최종 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="e81ba-128">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e81ba-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e81ba-129">-InputObject</span></span>
<span data-ttu-id="e81ba-130">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e81ba-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e81ba-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e81ba-131">-Name</span></span>
<span data-ttu-id="e81ba-132">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="e81ba-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e81ba-133">-NoWait</span></span>
<span data-ttu-id="e81ba-134">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="e81ba-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e81ba-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e81ba-135">-ResourceGroupName</span></span>
<span data-ttu-id="e81ba-136">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e81ba-137">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e81ba-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e81ba-138">-ServerName</span></span>
<span data-ttu-id="e81ba-139">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-139">The name of the server.</span></span>

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

### <span data-ttu-id="e81ba-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="e81ba-140">-StartIPAddress</span></span>
<span data-ttu-id="e81ba-141">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="e81ba-142">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="e81ba-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e81ba-143">-SubscriptionId</span></span>
<span data-ttu-id="e81ba-144">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e81ba-145">-확인</span><span class="sxs-lookup"><span data-stu-id="e81ba-145">-Confirm</span></span>
<span data-ttu-id="e81ba-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81ba-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81ba-147">-WhatIf</span></span>
<span data-ttu-id="e81ba-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e81ba-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81ba-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81ba-150">CommonParameters</span></span>
<span data-ttu-id="e81ba-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81ba-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e81ba-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81ba-153">입력</span><span class="sxs-lookup"><span data-stu-id="e81ba-153">INPUTS</span></span>

### <span data-ttu-id="e81ba-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="e81ba-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="e81ba-155">출력</span><span class="sxs-lookup"><span data-stu-id="e81ba-155">OUTPUTS</span></span>

### <span data-ttu-id="e81ba-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e81ba-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="e81ba-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e81ba-157">NOTES</span></span>

<span data-ttu-id="e81ba-158">별칭</span><span class="sxs-lookup"><span data-stu-id="e81ba-158">ALIASES</span></span>

<span data-ttu-id="e81ba-159">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e81ba-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e81ba-160">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e81ba-161">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e81ba-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e81ba-162">INPUTOBJECT <IMariaDbIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e81ba-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e81ba-163">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e81ba-164">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e81ba-165">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e81ba-166">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e81ba-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e81ba-167">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e81ba-168">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e81ba-169">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e81ba-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e81ba-171">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e81ba-172">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="e81ba-173">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e81ba-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e81ba-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e81ba-174">RELATED LINKS</span></span>

