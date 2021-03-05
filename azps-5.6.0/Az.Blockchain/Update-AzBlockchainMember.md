---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 833e660980d82c32667d166dbeed4520686d1124
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975579"
---
# <span data-ttu-id="1cb8e-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="1cb8e-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="1cb8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb8e-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb8e-103">블록체인 멤버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-103">Update a blockchain member.</span></span>

## <span data-ttu-id="1cb8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1cb8e-104">SYNTAX</span></span>

### <span data-ttu-id="1cb8e-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="1cb8e-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb8e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1cb8e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1cb8e-107">설명</span><span class="sxs-lookup"><span data-stu-id="1cb8e-107">DESCRIPTION</span></span>
<span data-ttu-id="1cb8e-108">블록체인 멤버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-108">Update a blockchain member.</span></span>

## <span data-ttu-id="1cb8e-109">예제</span><span class="sxs-lookup"><span data-stu-id="1cb8e-109">EXAMPLES</span></span>

### <span data-ttu-id="1cb8e-110">예제 1: 블록체인 멤버 업데이트</span><span class="sxs-lookup"><span data-stu-id="1cb8e-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="1cb8e-111">이 명령은 블록체인 멤버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="1cb8e-112">예제 2: 블록체인 멤버 업데이트</span><span class="sxs-lookup"><span data-stu-id="1cb8e-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="1cb8e-113">이 명령은 블록체인 멤버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="1cb8e-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1cb8e-114">PARAMETERS</span></span>

### <span data-ttu-id="1cb8e-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="1cb8e-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="1cb8e-116">관리되는 컨소시엄 관리 계정 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-116">Sets the managed consortium management account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb8e-117">-DefaultProfile</span></span>
<span data-ttu-id="1cb8e-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cb8e-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="1cb8e-119">-FirewallRule</span></span>
<span data-ttu-id="1cb8e-120">방화벽 규칙을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="1cb8e-121">구성을 위해 FIREWALLRULE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cb8e-122">-InputObject</span></span>
<span data-ttu-id="1cb8e-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1cb8e-124">-Name</span></span>
<span data-ttu-id="1cb8e-125">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8e-126">-Password</span><span class="sxs-lookup"><span data-stu-id="1cb8e-126">-Password</span></span>
<span data-ttu-id="1cb8e-127">트랜잭션 노드 dns 엔드포인트 기본 인증 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-127">Sets the transaction node dns endpoint basic auth password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb8e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1cb8e-129">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1cb8e-130">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1cb8e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1cb8e-131">-SubscriptionId</span></span>
<span data-ttu-id="1cb8e-132">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1cb8e-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1cb8e-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="1cb8e-134">-Tag</span></span>
<span data-ttu-id="1cb8e-135">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb8e-136">-확인</span><span class="sxs-lookup"><span data-stu-id="1cb8e-136">-Confirm</span></span>
<span data-ttu-id="1cb8e-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb8e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb8e-138">-WhatIf</span></span>
<span data-ttu-id="1cb8e-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb8e-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb8e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb8e-141">CommonParameters</span></span>
<span data-ttu-id="1cb8e-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb8e-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cb8e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb8e-144">입력</span><span class="sxs-lookup"><span data-stu-id="1cb8e-144">INPUTS</span></span>

### <span data-ttu-id="1cb8e-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="1cb8e-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="1cb8e-146">출력</span><span class="sxs-lookup"><span data-stu-id="1cb8e-146">OUTPUTS</span></span>

### <span data-ttu-id="1cb8e-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="1cb8e-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="1cb8e-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1cb8e-148">NOTES</span></span>

<span data-ttu-id="1cb8e-149">별칭</span><span class="sxs-lookup"><span data-stu-id="1cb8e-149">ALIASES</span></span>

<span data-ttu-id="1cb8e-150">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1cb8e-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1cb8e-151">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1cb8e-152">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1cb8e-153">FIREWALLRULE <IFirewallRule[]>: 방화벽 규칙을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="1cb8e-154">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 엔드 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="1cb8e-155">`[RuleName <String>]`: 방화벽 규칙의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="1cb8e-156">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="1cb8e-157">INPUTOBJECT <IBlockchainIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1cb8e-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1cb8e-158">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="1cb8e-159">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1cb8e-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1cb8e-160">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="1cb8e-161">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="1cb8e-162">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1cb8e-163">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1cb8e-164">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="1cb8e-165">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="1cb8e-166">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cb8e-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="1cb8e-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cb8e-167">RELATED LINKS</span></span>

