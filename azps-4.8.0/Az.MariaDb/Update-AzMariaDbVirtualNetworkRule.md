---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214452"
---
# <span data-ttu-id="1b861-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1b861-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="1b861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b861-102">SYNOPSIS</span></span>
<span data-ttu-id="1b861-103">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="1b861-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b861-104">SYNTAX</span></span>

### <span data-ttu-id="1b861-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1b861-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1b861-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1b861-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1b861-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1b861-107">DESCRIPTION</span></span>
<span data-ttu-id="1b861-108">기존 가상 네트워크 규칙을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="1b861-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1b861-109">EXAMPLES</span></span>

### <span data-ttu-id="1b861-110">예제 1: \ \ 가상 네트워크 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="1b861-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="1b861-111">이 명령은 가상 네트워크 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="1b861-112">변수</span><span class="sxs-lookup"><span data-stu-id="1b861-112">PARAMETERS</span></span>

### <span data-ttu-id="1b861-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b861-113">-AsJob</span></span>
<span data-ttu-id="1b861-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1b861-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1b861-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b861-115">-DefaultProfile</span></span>
<span data-ttu-id="1b861-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b861-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1b861-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="1b861-118">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="1b861-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b861-119">-InputObject</span></span>
<span data-ttu-id="1b861-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b861-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1b861-121">-Name</span></span>
<span data-ttu-id="1b861-122">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="1b861-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b861-123">-NoWait</span></span>
<span data-ttu-id="1b861-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1b861-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b861-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b861-125">-PassThru</span></span>
<span data-ttu-id="1b861-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1b861-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b861-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b861-128">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1b861-129">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1b861-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1b861-130">-ServerName</span></span>
<span data-ttu-id="1b861-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-131">The name of the server.</span></span>

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

### <span data-ttu-id="1b861-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1b861-132">-SubnetId</span></span>
<span data-ttu-id="1b861-133">가상 네트워크 서브넷의 ARM 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-133">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b861-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b861-134">-SubscriptionId</span></span>
<span data-ttu-id="1b861-135">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="1b861-136">-확인</span><span class="sxs-lookup"><span data-stu-id="1b861-136">-Confirm</span></span>
<span data-ttu-id="1b861-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b861-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b861-138">-WhatIf</span></span>
<span data-ttu-id="1b861-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b861-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b861-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b861-141">CommonParameters</span></span>
<span data-ttu-id="1b861-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b861-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1b861-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b861-144">입력</span><span class="sxs-lookup"><span data-stu-id="1b861-144">INPUTS</span></span>

### <span data-ttu-id="1b861-145">IMariaDbIdentity (Microsoft. PowerShell. m b.</span><span class="sxs-lookup"><span data-stu-id="1b861-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="1b861-146">출력</span><span class="sxs-lookup"><span data-stu-id="1b861-146">OUTPUTS</span></span>

### <span data-ttu-id="1b861-147">Microsoft. Api20180601Preview. IVirtualNetworkRule에 대 한. b a r i.</span><span class="sxs-lookup"><span data-stu-id="1b861-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="1b861-148">상속자</span><span class="sxs-lookup"><span data-stu-id="1b861-148">NOTES</span></span>

<span data-ttu-id="1b861-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="1b861-149">ALIASES</span></span>

<span data-ttu-id="1b861-150">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1b861-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1b861-151">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b861-152">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1b861-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1b861-153">INPUTOBJECT <IMariaDbIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1b861-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1b861-154">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1b861-155">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1b861-156">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1b861-157">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="1b861-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1b861-158">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1b861-159">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1b861-160">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1b861-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1b861-162">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1b861-163">`[SubscriptionId <String>]`: Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="1b861-164">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b861-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1b861-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b861-165">RELATED LINKS</span></span>

