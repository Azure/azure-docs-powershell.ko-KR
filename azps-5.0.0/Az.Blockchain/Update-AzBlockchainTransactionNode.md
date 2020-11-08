---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216918"
---
# <span data-ttu-id="535cd-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="535cd-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="535cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="535cd-102">SYNOPSIS</span></span>
<span data-ttu-id="535cd-103">트랜잭션 노드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-103">Update the transaction node.</span></span>

## <span data-ttu-id="535cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="535cd-104">SYNTAX</span></span>

### <span data-ttu-id="535cd-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="535cd-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="535cd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="535cd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="535cd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="535cd-107">DESCRIPTION</span></span>
<span data-ttu-id="535cd-108">트랜잭션 노드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-108">Update the transaction node.</span></span>

## <span data-ttu-id="535cd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="535cd-109">EXAMPLES</span></span>

### <span data-ttu-id="535cd-110">예제 1: transcation 노드 업데이트</span><span class="sxs-lookup"><span data-stu-id="535cd-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="535cd-111">이 명령은 트랜잭션 노드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="535cd-112">예제 2: transcation 노드 업데이트</span><span class="sxs-lookup"><span data-stu-id="535cd-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="535cd-113">이 명령은 트랜잭션 노드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="535cd-114">변수</span><span class="sxs-lookup"><span data-stu-id="535cd-114">PARAMETERS</span></span>

### <span data-ttu-id="535cd-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="535cd-115">-BlockchainMemberName</span></span>
<span data-ttu-id="535cd-116">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="535cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535cd-117">-DefaultProfile</span></span>
<span data-ttu-id="535cd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="535cd-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="535cd-119">-FirewallRule</span></span>
<span data-ttu-id="535cd-120">방화벽 규칙을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="535cd-121">생성 하려면 FIREWALLRULE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="535cd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="535cd-122">-InputObject</span></span>
<span data-ttu-id="535cd-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="535cd-124">-이름</span><span class="sxs-lookup"><span data-stu-id="535cd-124">-Name</span></span>
<span data-ttu-id="535cd-125">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-125">Transaction node name.</span></span>

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

### <span data-ttu-id="535cd-126">-암호</span><span class="sxs-lookup"><span data-stu-id="535cd-126">-Password</span></span>
<span data-ttu-id="535cd-127">트랜잭션 노드 dns 끝점 기본 인증 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="535cd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="535cd-128">-ResourceGroupName</span></span>
<span data-ttu-id="535cd-129">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="535cd-130">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="535cd-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="535cd-131">-SubscriptionId</span></span>
<span data-ttu-id="535cd-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="535cd-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="535cd-134">-확인</span><span class="sxs-lookup"><span data-stu-id="535cd-134">-Confirm</span></span>
<span data-ttu-id="535cd-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="535cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="535cd-136">-WhatIf</span></span>
<span data-ttu-id="535cd-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="535cd-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="535cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535cd-139">CommonParameters</span></span>
<span data-ttu-id="535cd-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535cd-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="535cd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535cd-142">입력</span><span class="sxs-lookup"><span data-stu-id="535cd-142">INPUTS</span></span>

### <span data-ttu-id="535cd-143">IBlockchainIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="535cd-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="535cd-144">출력</span><span class="sxs-lookup"><span data-stu-id="535cd-144">OUTPUTS</span></span>

### <span data-ttu-id="535cd-145">Api20180601Preview. ITransactionNode에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="535cd-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="535cd-146">상속자</span><span class="sxs-lookup"><span data-stu-id="535cd-146">NOTES</span></span>

<span data-ttu-id="535cd-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="535cd-147">ALIASES</span></span>

<span data-ttu-id="535cd-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="535cd-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="535cd-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="535cd-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="535cd-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="535cd-151">FIREWALLRULE <IFirewallRule [] >: 방화벽 규칙을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="535cd-152">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 끝 IP 주소를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="535cd-153">`[RuleName <String>]`: 방화벽 규칙의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="535cd-154">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="535cd-155">INPUTOBJECT <IBlockchainIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="535cd-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="535cd-156">`[BlockchainMemberName <String>]`: Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="535cd-157">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="535cd-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="535cd-158">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="535cd-159">`[OperationId <String>]`: 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="535cd-160">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="535cd-161">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="535cd-162">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="535cd-163">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="535cd-164">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535cd-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="535cd-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="535cd-165">RELATED LINKS</span></span>

