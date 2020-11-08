---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218497"
---
# <span data-ttu-id="79530-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="79530-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="79530-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79530-102">SYNOPSIS</span></span>
<span data-ttu-id="79530-103">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="79530-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79530-104">SYNTAX</span></span>

### <span data-ttu-id="79530-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="79530-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="79530-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="79530-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79530-107">설명은</span><span class="sxs-lookup"><span data-stu-id="79530-107">DESCRIPTION</span></span>
<span data-ttu-id="79530-108">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="79530-109">예제의</span><span class="sxs-lookup"><span data-stu-id="79530-109">EXAMPLES</span></span>

### <span data-ttu-id="79530-110">예제 1: 이름으로 PostgreSql 가상 네트워크 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="79530-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="79530-111">이 cmdlet은 이름으로 가상 네트워크 규칙을 PostgreSql 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="79530-112">예제 2: id를 기준으로 PostgreSql 가상 네트워크 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="79530-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="79530-113">이러한 cmdlet은 id를 기준으로 PostgreSql 가상 네트워크 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="79530-114">변수</span><span class="sxs-lookup"><span data-stu-id="79530-114">PARAMETERS</span></span>

### <span data-ttu-id="79530-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79530-115">-AsJob</span></span>
<span data-ttu-id="79530-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="79530-116">Run the command as a job</span></span>

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

### <span data-ttu-id="79530-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79530-117">-DefaultProfile</span></span>
<span data-ttu-id="79530-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79530-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="79530-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="79530-120">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79530-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="79530-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79530-121">-InputObject</span></span>
<span data-ttu-id="79530-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79530-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="79530-123">-이름</span><span class="sxs-lookup"><span data-stu-id="79530-123">-Name</span></span>
<span data-ttu-id="79530-124">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="79530-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="79530-125">-NoWait</span></span>
<span data-ttu-id="79530-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="79530-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="79530-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79530-127">-PassThru</span></span>
<span data-ttu-id="79530-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="79530-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79530-129">-ResourceGroupName</span></span>
<span data-ttu-id="79530-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-130">The name of the resource group.</span></span>
<span data-ttu-id="79530-131">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="79530-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79530-132">-ServerName</span></span>
<span data-ttu-id="79530-133">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-133">The name of the server.</span></span>

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

### <span data-ttu-id="79530-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="79530-134">-SubnetId</span></span>
<span data-ttu-id="79530-135">가상 네트워크 서브넷의 ARM 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="79530-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79530-136">-SubscriptionId</span></span>
<span data-ttu-id="79530-137">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="79530-138">-확인</span><span class="sxs-lookup"><span data-stu-id="79530-138">-Confirm</span></span>
<span data-ttu-id="79530-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79530-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79530-140">-WhatIf</span></span>
<span data-ttu-id="79530-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79530-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79530-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79530-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79530-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79530-143">CommonParameters</span></span>
<span data-ttu-id="79530-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79530-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79530-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79530-146">입력</span><span class="sxs-lookup"><span data-stu-id="79530-146">INPUTS</span></span>

### <span data-ttu-id="79530-147">PostgreSql. IPostgreSqlIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="79530-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="79530-148">출력</span><span class="sxs-lookup"><span data-stu-id="79530-148">OUTPUTS</span></span>

### <span data-ttu-id="79530-149">PostgreSql. Api20171201. IVirtualNetworkRule에 대 한</span><span class="sxs-lookup"><span data-stu-id="79530-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="79530-150">상속자</span><span class="sxs-lookup"><span data-stu-id="79530-150">NOTES</span></span>

<span data-ttu-id="79530-151">별칭과</span><span class="sxs-lookup"><span data-stu-id="79530-151">ALIASES</span></span>

<span data-ttu-id="79530-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="79530-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="79530-153">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="79530-154">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="79530-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="79530-155">INPUTOBJECT <IPostgreSqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="79530-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="79530-156">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="79530-157">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="79530-158">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="79530-159">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="79530-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="79530-160">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="79530-161">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="79530-162">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="79530-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="79530-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="79530-164">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="79530-165">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="79530-166">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79530-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="79530-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79530-167">RELATED LINKS</span></span>

