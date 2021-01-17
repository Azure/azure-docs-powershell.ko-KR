---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 7779a5405f50fe87f7a9e631b40cbdc8cb40fe5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491855"
---
# <span data-ttu-id="5274b-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5274b-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="5274b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5274b-102">SYNOPSIS</span></span>
<span data-ttu-id="5274b-103">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="5274b-104">구문</span><span class="sxs-lookup"><span data-stu-id="5274b-104">SYNTAX</span></span>

### <span data-ttu-id="5274b-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="5274b-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5274b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5274b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5274b-107">설명</span><span class="sxs-lookup"><span data-stu-id="5274b-107">DESCRIPTION</span></span>
<span data-ttu-id="5274b-108">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="5274b-109">예제</span><span class="sxs-lookup"><span data-stu-id="5274b-109">EXAMPLES</span></span>

### <span data-ttu-id="5274b-110">예제 1: 이름으로 MySql Virtual Network 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="5274b-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="5274b-111">이 cmdlet은 이름으로 MySql Virtual Network 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="5274b-112">예제 2: ID로 MySql Virtual Network 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="5274b-113">이러한 cmdlet은 ID에 의해 MySql Virtual Network 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="5274b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5274b-114">PARAMETERS</span></span>

### <span data-ttu-id="5274b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5274b-115">-AsJob</span></span>
<span data-ttu-id="5274b-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="5274b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5274b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5274b-117">-DefaultProfile</span></span>
<span data-ttu-id="5274b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5274b-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5274b-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="5274b-120">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만드면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="5274b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5274b-121">-InputObject</span></span>
<span data-ttu-id="5274b-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5274b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5274b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5274b-123">-Name</span></span>
<span data-ttu-id="5274b-124">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="5274b-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5274b-125">-NoWait</span></span>
<span data-ttu-id="5274b-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="5274b-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5274b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5274b-127">-PassThru</span></span>
<span data-ttu-id="5274b-128">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5274b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5274b-129">-ResourceGroupName</span></span>
<span data-ttu-id="5274b-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-130">The name of the resource group.</span></span>
<span data-ttu-id="5274b-131">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5274b-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5274b-132">-ServerName</span></span>
<span data-ttu-id="5274b-133">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-133">The name of the server.</span></span>

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

### <span data-ttu-id="5274b-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5274b-134">-SubnetId</span></span>
<span data-ttu-id="5274b-135">가상 ARM 서브넷의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="5274b-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5274b-136">-SubscriptionId</span></span>
<span data-ttu-id="5274b-137">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5274b-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5274b-138">-Confirm</span></span>
<span data-ttu-id="5274b-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5274b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5274b-140">-WhatIf</span></span>
<span data-ttu-id="5274b-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5274b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5274b-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5274b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5274b-143">CommonParameters</span></span>
<span data-ttu-id="5274b-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5274b-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5274b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5274b-146">입력</span><span class="sxs-lookup"><span data-stu-id="5274b-146">INPUTS</span></span>

### <span data-ttu-id="5274b-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5274b-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5274b-148">출력</span><span class="sxs-lookup"><span data-stu-id="5274b-148">OUTPUTS</span></span>

### <span data-ttu-id="5274b-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5274b-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="5274b-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5274b-150">NOTES</span></span>

<span data-ttu-id="5274b-151">별칭</span><span class="sxs-lookup"><span data-stu-id="5274b-151">ALIASES</span></span>

<span data-ttu-id="5274b-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5274b-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5274b-153">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5274b-154">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5274b-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5274b-155">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5274b-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5274b-156">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5274b-157">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5274b-158">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5274b-159">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="5274b-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5274b-160">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="5274b-161">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5274b-162">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5274b-163">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="5274b-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5274b-165">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5274b-166">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5274b-167">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5274b-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5274b-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5274b-168">RELATED LINKS</span></span>

