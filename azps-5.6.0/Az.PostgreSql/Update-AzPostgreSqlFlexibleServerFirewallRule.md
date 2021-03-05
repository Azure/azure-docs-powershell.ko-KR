---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 26f6da2cdbf7d12e4d4927fd14ffc6b58b539bef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974651"
---
# <span data-ttu-id="b6582-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6582-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="b6582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6582-102">SYNOPSIS</span></span>
<span data-ttu-id="b6582-103">새 방화벽 규칙을 만들고 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b6582-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6582-104">SYNTAX</span></span>

### <span data-ttu-id="b6582-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="b6582-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6582-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b6582-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6582-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6582-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6582-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b6582-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b6582-109">설명</span><span class="sxs-lookup"><span data-stu-id="b6582-109">DESCRIPTION</span></span>
<span data-ttu-id="b6582-110">새 방화벽 규칙을 만들고 기존 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="b6582-111">예제</span><span class="sxs-lookup"><span data-stu-id="b6582-111">EXAMPLES</span></span>

### <span data-ttu-id="b6582-112">예제 1: 이름으로 PostgreSql 방화벽 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="b6582-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b6582-113">이 cmdlet은 PostgreSql 방화벽 규칙을 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="b6582-114">예제 2: ID에 의해 PostgreSql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="b6582-115">이러한 cmdlet은 ID에 의해 PostgreSql 방화벽 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="b6582-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6582-116">PARAMETERS</span></span>

### <span data-ttu-id="b6582-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6582-117">-AsJob</span></span>
<span data-ttu-id="b6582-118">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b6582-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="b6582-119">-ClientIPAddress</span></span>
<span data-ttu-id="b6582-120">클라이언트가 서버 방화벽 규칙의 단일 IP를 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="b6582-121">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b6582-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6582-122">-DefaultProfile</span></span>
<span data-ttu-id="b6582-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6582-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="b6582-124">-EndIPAddress</span></span>
<span data-ttu-id="b6582-125">서버 방화벽 규칙의 최종 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="b6582-126">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b6582-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6582-127">-InputObject</span></span>
<span data-ttu-id="b6582-128">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b6582-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6582-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b6582-129">-Name</span></span>
<span data-ttu-id="b6582-130">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b6582-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b6582-131">-NoWait</span></span>
<span data-ttu-id="b6582-132">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="b6582-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b6582-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6582-133">-ResourceGroupName</span></span>
<span data-ttu-id="b6582-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-134">The name of the resource group.</span></span>
<span data-ttu-id="b6582-135">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b6582-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6582-136">-ServerName</span></span>
<span data-ttu-id="b6582-137">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-137">The name of the server.</span></span>

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

### <span data-ttu-id="b6582-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="b6582-138">-StartIPAddress</span></span>
<span data-ttu-id="b6582-139">서버 방화벽 규칙의 시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="b6582-140">IPv4 형식이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="b6582-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6582-141">-SubscriptionId</span></span>
<span data-ttu-id="b6582-142">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b6582-143">-확인</span><span class="sxs-lookup"><span data-stu-id="b6582-143">-Confirm</span></span>
<span data-ttu-id="b6582-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6582-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6582-145">-WhatIf</span></span>
<span data-ttu-id="b6582-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6582-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6582-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6582-148">CommonParameters</span></span>
<span data-ttu-id="b6582-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6582-150">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6582-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6582-151">입력</span><span class="sxs-lookup"><span data-stu-id="b6582-151">INPUTS</span></span>

### <span data-ttu-id="b6582-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b6582-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b6582-153">출력</span><span class="sxs-lookup"><span data-stu-id="b6582-153">OUTPUTS</span></span>

### <span data-ttu-id="b6582-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b6582-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="b6582-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6582-155">NOTES</span></span>

<span data-ttu-id="b6582-156">별칭</span><span class="sxs-lookup"><span data-stu-id="b6582-156">ALIASES</span></span>

<span data-ttu-id="b6582-157">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b6582-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6582-158">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6582-159">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6582-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6582-160">INPUTOBJECT <IPostgreSqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6582-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6582-161">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b6582-162">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b6582-163">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b6582-164">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b6582-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6582-165">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b6582-166">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b6582-167">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="b6582-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b6582-169">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b6582-170">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b6582-171">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6582-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b6582-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6582-172">RELATED LINKS</span></span>

