---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183972"
---
# <span data-ttu-id="41b00-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41b00-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="41b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41b00-102">SYNOPSIS</span></span>
<span data-ttu-id="41b00-103">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="41b00-104">구문</span><span class="sxs-lookup"><span data-stu-id="41b00-104">SYNTAX</span></span>

### <span data-ttu-id="41b00-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="41b00-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41b00-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="41b00-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41b00-107">설명</span><span class="sxs-lookup"><span data-stu-id="41b00-107">DESCRIPTION</span></span>
<span data-ttu-id="41b00-108">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="41b00-109">예제</span><span class="sxs-lookup"><span data-stu-id="41b00-109">EXAMPLES</span></span>

### <span data-ttu-id="41b00-110">예제 1: 이름으로 PostgreSql Virtual Network 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="41b00-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="41b00-111">이 cmdlet은 PostgreSql Virtual Network 규칙을 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="41b00-112">예제 2: ID로 PostgreSql Virtual Network 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="41b00-113">이러한 cmdlet은 ID에 의해 PostgreSql Virtual Network 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="41b00-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41b00-114">PARAMETERS</span></span>

### <span data-ttu-id="41b00-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41b00-115">-AsJob</span></span>
<span data-ttu-id="41b00-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="41b00-116">Run the command as a job</span></span>

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

### <span data-ttu-id="41b00-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b00-117">-DefaultProfile</span></span>
<span data-ttu-id="41b00-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41b00-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="41b00-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="41b00-120">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만드면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="41b00-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41b00-121">-InputObject</span></span>
<span data-ttu-id="41b00-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="41b00-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41b00-123">-Name</span><span class="sxs-lookup"><span data-stu-id="41b00-123">-Name</span></span>
<span data-ttu-id="41b00-124">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-124">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b00-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="41b00-125">-NoWait</span></span>
<span data-ttu-id="41b00-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="41b00-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="41b00-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41b00-127">-PassThru</span></span>
<span data-ttu-id="41b00-128">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="41b00-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b00-129">-ResourceGroupName</span></span>
<span data-ttu-id="41b00-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-130">The name of the resource group.</span></span>
<span data-ttu-id="41b00-131">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b00-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="41b00-132">-ServerName</span></span>
<span data-ttu-id="41b00-133">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b00-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="41b00-134">-SubnetId</span></span>
<span data-ttu-id="41b00-135">가상 ARM 서브넷의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="41b00-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41b00-136">-SubscriptionId</span></span>
<span data-ttu-id="41b00-137">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-137">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b00-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41b00-138">-Confirm</span></span>
<span data-ttu-id="41b00-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41b00-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b00-140">-WhatIf</span></span>
<span data-ttu-id="41b00-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="41b00-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41b00-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41b00-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b00-143">CommonParameters</span></span>
<span data-ttu-id="41b00-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b00-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41b00-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b00-146">입력</span><span class="sxs-lookup"><span data-stu-id="41b00-146">INPUTS</span></span>

### <span data-ttu-id="41b00-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="41b00-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="41b00-148">출력</span><span class="sxs-lookup"><span data-stu-id="41b00-148">OUTPUTS</span></span>

### <span data-ttu-id="41b00-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41b00-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="41b00-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="41b00-150">NOTES</span></span>

<span data-ttu-id="41b00-151">별칭</span><span class="sxs-lookup"><span data-stu-id="41b00-151">ALIASES</span></span>

<span data-ttu-id="41b00-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="41b00-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41b00-153">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41b00-154">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41b00-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41b00-155">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="41b00-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41b00-156">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="41b00-157">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="41b00-158">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="41b00-159">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="41b00-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41b00-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="41b00-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="41b00-162">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="41b00-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="41b00-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="41b00-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="41b00-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b00-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="41b00-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41b00-167">RELATED LINKS</span></span>

