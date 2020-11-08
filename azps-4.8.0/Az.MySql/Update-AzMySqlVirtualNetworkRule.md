---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211620"
---
# <span data-ttu-id="4a97f-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4a97f-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="4a97f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a97f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a97f-103">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="4a97f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a97f-104">SYNTAX</span></span>

### <span data-ttu-id="4a97f-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4a97f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a97f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4a97f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a97f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4a97f-107">DESCRIPTION</span></span>
<span data-ttu-id="4a97f-108">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="4a97f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4a97f-109">EXAMPLES</span></span>

### <span data-ttu-id="4a97f-110">예제 1: 이름별로 MySql 가상 네트워크 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="4a97f-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="4a97f-111">이 cmdlet은 이름으로 MySql 가상 네트워크 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="4a97f-112">예제 2: id를 기준으로 MySql 가상 네트워크 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="4a97f-113">이러한 cmdlet은 id를 기준으로 MySql 가상 네트워크 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="4a97f-114">변수</span><span class="sxs-lookup"><span data-stu-id="4a97f-114">PARAMETERS</span></span>

### <span data-ttu-id="4a97f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a97f-115">-AsJob</span></span>
<span data-ttu-id="4a97f-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="4a97f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4a97f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a97f-117">-DefaultProfile</span></span>
<span data-ttu-id="4a97f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a97f-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4a97f-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="4a97f-120">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="4a97f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a97f-121">-InputObject</span></span>
<span data-ttu-id="4a97f-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a97f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="4a97f-123">-Name</span></span>
<span data-ttu-id="4a97f-124">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="4a97f-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4a97f-125">-NoWait</span></span>
<span data-ttu-id="4a97f-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="4a97f-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a97f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a97f-127">-PassThru</span></span>
<span data-ttu-id="4a97f-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a97f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a97f-129">-ResourceGroupName</span></span>
<span data-ttu-id="4a97f-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-130">The name of the resource group.</span></span>
<span data-ttu-id="4a97f-131">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4a97f-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a97f-132">-ServerName</span></span>
<span data-ttu-id="4a97f-133">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-133">The name of the server.</span></span>

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

### <span data-ttu-id="4a97f-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4a97f-134">-SubnetId</span></span>
<span data-ttu-id="4a97f-135">가상 네트워크 서브넷의 ARM 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="4a97f-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a97f-136">-SubscriptionId</span></span>
<span data-ttu-id="4a97f-137">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4a97f-138">-확인</span><span class="sxs-lookup"><span data-stu-id="4a97f-138">-Confirm</span></span>
<span data-ttu-id="4a97f-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a97f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a97f-140">-WhatIf</span></span>
<span data-ttu-id="4a97f-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a97f-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a97f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a97f-143">CommonParameters</span></span>
<span data-ttu-id="4a97f-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a97f-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a97f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a97f-146">입력</span><span class="sxs-lookup"><span data-stu-id="4a97f-146">INPUTS</span></span>

### <span data-ttu-id="4a97f-147">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="4a97f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4a97f-148">출력</span><span class="sxs-lookup"><span data-stu-id="4a97f-148">OUTPUTS</span></span>

### <span data-ttu-id="4a97f-149">Api20171201. IVirtualNetworkRule에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4a97f-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="4a97f-150">상속자</span><span class="sxs-lookup"><span data-stu-id="4a97f-150">NOTES</span></span>

<span data-ttu-id="4a97f-151">별칭과</span><span class="sxs-lookup"><span data-stu-id="4a97f-151">ALIASES</span></span>

<span data-ttu-id="4a97f-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4a97f-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a97f-153">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a97f-154">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a97f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a97f-155">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4a97f-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a97f-156">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4a97f-157">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4a97f-158">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4a97f-159">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="4a97f-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a97f-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4a97f-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4a97f-162">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="4a97f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4a97f-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4a97f-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4a97f-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a97f-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4a97f-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a97f-167">RELATED LINKS</span></span>

