---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cbb774e0a4bedb66a32839c069c305317c8e9f43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003856"
---
# <span data-ttu-id="3d8a9-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3d8a9-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="3d8a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8a9-103">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="3d8a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d8a9-104">SYNTAX</span></span>

### <span data-ttu-id="3d8a9-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="3d8a9-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d8a9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3d8a9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3d8a9-107">설명</span><span class="sxs-lookup"><span data-stu-id="3d8a9-107">DESCRIPTION</span></span>
<span data-ttu-id="3d8a9-108">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="3d8a9-109">예제</span><span class="sxs-lookup"><span data-stu-id="3d8a9-109">EXAMPLES</span></span>

### <span data-ttu-id="3d8a9-110">예제 1: MariaDB 가상 네트워크 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="3d8a9-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="3d8a9-111">이 명령은 가상 네트워크 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="3d8a9-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3d8a9-112">PARAMETERS</span></span>

### <span data-ttu-id="3d8a9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d8a9-113">-AsJob</span></span>
<span data-ttu-id="3d8a9-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3d8a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8a9-115">-DefaultProfile</span></span>
<span data-ttu-id="3d8a9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d8a9-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d8a9-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="3d8a9-118">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만드기</span><span class="sxs-lookup"><span data-stu-id="3d8a9-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="3d8a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d8a9-119">-InputObject</span></span>
<span data-ttu-id="3d8a9-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d8a9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3d8a9-121">-Name</span></span>
<span data-ttu-id="3d8a9-122">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-122">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="3d8a9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3d8a9-123">-NoWait</span></span>
<span data-ttu-id="3d8a9-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="3d8a9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3d8a9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d8a9-125">-PassThru</span></span>
<span data-ttu-id="3d8a9-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3d8a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d8a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="3d8a9-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3d8a9-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3d8a9-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d8a9-130">-ServerName</span></span>
<span data-ttu-id="3d8a9-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-131">The name of the server.</span></span>

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

### <span data-ttu-id="3d8a9-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3d8a9-132">-SubnetId</span></span>
<span data-ttu-id="3d8a9-133">가상 ARM 서브넷의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="3d8a9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d8a9-134">-SubscriptionId</span></span>
<span data-ttu-id="3d8a9-135">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="3d8a9-136">-확인</span><span class="sxs-lookup"><span data-stu-id="3d8a9-136">-Confirm</span></span>
<span data-ttu-id="3d8a9-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d8a9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d8a9-138">-WhatIf</span></span>
<span data-ttu-id="3d8a9-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d8a9-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d8a9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8a9-141">CommonParameters</span></span>
<span data-ttu-id="3d8a9-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8a9-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d8a9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8a9-144">입력</span><span class="sxs-lookup"><span data-stu-id="3d8a9-144">INPUTS</span></span>

### <span data-ttu-id="3d8a9-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="3d8a9-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="3d8a9-146">출력</span><span class="sxs-lookup"><span data-stu-id="3d8a9-146">OUTPUTS</span></span>

### <span data-ttu-id="3d8a9-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3d8a9-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="3d8a9-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d8a9-148">NOTES</span></span>

<span data-ttu-id="3d8a9-149">별칭</span><span class="sxs-lookup"><span data-stu-id="3d8a9-149">ALIASES</span></span>

<span data-ttu-id="3d8a9-150">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3d8a9-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d8a9-151">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d8a9-152">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d8a9-153">INPUTOBJECT <IMariaDbIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3d8a9-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d8a9-154">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3d8a9-155">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3d8a9-156">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3d8a9-157">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="3d8a9-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d8a9-158">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3d8a9-159">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3d8a9-160">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3d8a9-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3d8a9-162">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3d8a9-163">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="3d8a9-164">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8a9-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3d8a9-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d8a9-165">RELATED LINKS</span></span>

