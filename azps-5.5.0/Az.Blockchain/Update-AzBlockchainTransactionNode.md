---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177892"
---
# <span data-ttu-id="199af-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="199af-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="199af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="199af-102">SYNOPSIS</span></span>
<span data-ttu-id="199af-103">트랜잭션 노드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-103">Update the transaction node.</span></span>

## <span data-ttu-id="199af-104">구문</span><span class="sxs-lookup"><span data-stu-id="199af-104">SYNTAX</span></span>

### <span data-ttu-id="199af-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="199af-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="199af-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="199af-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="199af-107">설명</span><span class="sxs-lookup"><span data-stu-id="199af-107">DESCRIPTION</span></span>
<span data-ttu-id="199af-108">트랜잭션 노드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-108">Update the transaction node.</span></span>

## <span data-ttu-id="199af-109">예제</span><span class="sxs-lookup"><span data-stu-id="199af-109">EXAMPLES</span></span>

### <span data-ttu-id="199af-110">예제 1: 변환 노드 업데이트</span><span class="sxs-lookup"><span data-stu-id="199af-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="199af-111">이 명령은 트랜잭션 노드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="199af-112">예제 2: 변환 노드 업데이트</span><span class="sxs-lookup"><span data-stu-id="199af-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="199af-113">이 명령은 트랜잭션 노드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="199af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="199af-114">PARAMETERS</span></span>

### <span data-ttu-id="199af-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="199af-115">-BlockchainMemberName</span></span>
<span data-ttu-id="199af-116">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="199af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199af-117">-DefaultProfile</span></span>
<span data-ttu-id="199af-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="199af-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="199af-119">-FirewallRule</span></span>
<span data-ttu-id="199af-120">방화벽 규칙을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="199af-121">구성을 위해 FIREWALLRULE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="199af-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="199af-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="199af-122">-InputObject</span></span>
<span data-ttu-id="199af-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="199af-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="199af-124">-Name</span><span class="sxs-lookup"><span data-stu-id="199af-124">-Name</span></span>
<span data-ttu-id="199af-125">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199af-126">-Password</span><span class="sxs-lookup"><span data-stu-id="199af-126">-Password</span></span>
<span data-ttu-id="199af-127">트랜잭션 노드 dns 엔드포인트 기본 인증 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="199af-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="199af-128">-ResourceGroupName</span></span>
<span data-ttu-id="199af-129">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="199af-130">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="199af-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="199af-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="199af-131">-SubscriptionId</span></span>
<span data-ttu-id="199af-132">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="199af-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="199af-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="199af-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="199af-134">-Confirm</span></span>
<span data-ttu-id="199af-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="199af-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="199af-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="199af-136">-WhatIf</span></span>
<span data-ttu-id="199af-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="199af-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="199af-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="199af-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="199af-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199af-139">CommonParameters</span></span>
<span data-ttu-id="199af-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199af-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="199af-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199af-142">입력</span><span class="sxs-lookup"><span data-stu-id="199af-142">INPUTS</span></span>

### <span data-ttu-id="199af-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="199af-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="199af-144">출력</span><span class="sxs-lookup"><span data-stu-id="199af-144">OUTPUTS</span></span>

### <span data-ttu-id="199af-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="199af-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="199af-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="199af-146">NOTES</span></span>

<span data-ttu-id="199af-147">별칭</span><span class="sxs-lookup"><span data-stu-id="199af-147">ALIASES</span></span>

<span data-ttu-id="199af-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="199af-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="199af-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="199af-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="199af-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="199af-151">FIREWALLRULE <IFirewallRule[]>: 방화벽 규칙을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="199af-152">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 끝 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="199af-153">`[RuleName <String>]`: 방화벽 규칙의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="199af-154">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 갖거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="199af-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="199af-155">INPUTOBJECT: <IBlockchainIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="199af-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="199af-156">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="199af-157">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="199af-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="199af-158">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="199af-159">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="199af-160">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="199af-161">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="199af-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="199af-162">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="199af-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="199af-163">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="199af-164">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="199af-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="199af-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="199af-165">RELATED LINKS</span></span>

