---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226809"
---
# <span data-ttu-id="b4c65-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b4c65-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="b4c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4c65-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c65-103">새 방화벽 규칙을 만들거나 기존 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b4c65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4c65-104">SYNTAX</span></span>

### <span data-ttu-id="b4c65-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4c65-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4c65-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b4c65-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4c65-107">Clivipaddressid</span><span class="sxs-lookup"><span data-stu-id="b4c65-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b4c65-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b4c65-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b4c65-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b4c65-109">DESCRIPTION</span></span>
<span data-ttu-id="b4c65-110">새 방화벽 규칙을 만들거나 기존 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b4c65-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b4c65-111">EXAMPLES</span></span>

### <span data-ttu-id="b4c65-112">예제 1: \ \ 방화벽 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="b4c65-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="b4c65-113">이 명령은이을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="b4c65-114">예제 2: id를 기준으로 해를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b4c65-115">Cmdlet이 id를 기준으로 해를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="b4c65-116">예제 3: ClientIPAddress를 기준으로 4 번의 방화벽 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="b4c65-117">Cmdlet이 ClientIPAddress를 통해이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="b4c65-118">변수</span><span class="sxs-lookup"><span data-stu-id="b4c65-118">PARAMETERS</span></span>

### <span data-ttu-id="b4c65-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4c65-119">-AsJob</span></span>
<span data-ttu-id="b4c65-120">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b4c65-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b4c65-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b4c65-121">-ClientIPAddress</span></span>
<span data-ttu-id="b4c65-122">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b4c65-123">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b4c65-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c65-124">-DefaultProfile</span></span>
<span data-ttu-id="b4c65-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4c65-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b4c65-126">-EndIPAddress</span></span>
<span data-ttu-id="b4c65-127">서버 방화벽 규칙의 끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b4c65-128">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b4c65-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4c65-129">-InputObject</span></span>
<span data-ttu-id="b4c65-130">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4c65-131">-이름</span><span class="sxs-lookup"><span data-stu-id="b4c65-131">-Name</span></span>
<span data-ttu-id="b4c65-132">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b4c65-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b4c65-133">-NoWait</span></span>
<span data-ttu-id="b4c65-134">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b4c65-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b4c65-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c65-135">-ResourceGroupName</span></span>
<span data-ttu-id="b4c65-136">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b4c65-137">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b4c65-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4c65-138">-ServerName</span></span>
<span data-ttu-id="b4c65-139">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-139">The name of the server.</span></span>

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

### <span data-ttu-id="b4c65-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b4c65-140">-StartIPAddress</span></span>
<span data-ttu-id="b4c65-141">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b4c65-142">IPv4 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b4c65-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4c65-143">-SubscriptionId</span></span>
<span data-ttu-id="b4c65-144">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b4c65-145">-확인</span><span class="sxs-lookup"><span data-stu-id="b4c65-145">-Confirm</span></span>
<span data-ttu-id="b4c65-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4c65-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4c65-147">-WhatIf</span></span>
<span data-ttu-id="b4c65-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4c65-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4c65-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c65-150">CommonParameters</span></span>
<span data-ttu-id="b4c65-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c65-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4c65-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c65-153">입력</span><span class="sxs-lookup"><span data-stu-id="b4c65-153">INPUTS</span></span>

### <span data-ttu-id="b4c65-154">IMariaDbIdentity (Microsoft. PowerShell. m b.</span><span class="sxs-lookup"><span data-stu-id="b4c65-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="b4c65-155">출력</span><span class="sxs-lookup"><span data-stu-id="b4c65-155">OUTPUTS</span></span>

### <span data-ttu-id="b4c65-156">Microsoft. Api20180601Preview. IFirewallRule에 대 한. b a r i.</span><span class="sxs-lookup"><span data-stu-id="b4c65-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="b4c65-157">상속자</span><span class="sxs-lookup"><span data-stu-id="b4c65-157">NOTES</span></span>

<span data-ttu-id="b4c65-158">별칭과</span><span class="sxs-lookup"><span data-stu-id="b4c65-158">ALIASES</span></span>

<span data-ttu-id="b4c65-159">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b4c65-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4c65-160">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4c65-161">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4c65-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4c65-162">INPUTOBJECT <IMariaDbIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b4c65-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b4c65-163">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b4c65-164">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b4c65-165">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b4c65-166">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b4c65-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b4c65-167">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b4c65-168">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b4c65-169">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b4c65-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b4c65-171">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b4c65-172">`[SubscriptionId <String>]`: Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="b4c65-173">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4c65-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b4c65-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4c65-174">RELATED LINKS</span></span>

