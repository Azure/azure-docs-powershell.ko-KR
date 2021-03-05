---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: 78d3d6449eb5a487c6c4a8a60a732c30fa502600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965120"
---
# <span data-ttu-id="7b99f-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="7b99f-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="7b99f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b99f-102">SYNOPSIS</span></span>
<span data-ttu-id="7b99f-103">트랜잭션 노드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="7b99f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b99f-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b99f-105">설명</span><span class="sxs-lookup"><span data-stu-id="7b99f-105">DESCRIPTION</span></span>
<span data-ttu-id="7b99f-106">트랜잭션 노드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="7b99f-107">예제</span><span class="sxs-lookup"><span data-stu-id="7b99f-107">EXAMPLES</span></span>

### <span data-ttu-id="7b99f-108">예제 1: 블록체인 트랜잭션 노드 만들기</span><span class="sxs-lookup"><span data-stu-id="7b99f-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="7b99f-109">이 명령은 블록체인 트랜잭션 노드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="7b99f-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b99f-110">PARAMETERS</span></span>

### <span data-ttu-id="7b99f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b99f-111">-AsJob</span></span>
<span data-ttu-id="7b99f-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="7b99f-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="7b99f-113">-BlockchainMemberName</span></span>
<span data-ttu-id="7b99f-114">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="7b99f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b99f-115">-DefaultProfile</span></span>
<span data-ttu-id="7b99f-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b99f-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="7b99f-117">-FirewallRule</span></span>
<span data-ttu-id="7b99f-118">방화벽 규칙을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="7b99f-119">구성을 위해 FIREWALLRULE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7b99f-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b99f-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7b99f-120">-Location</span></span>
<span data-ttu-id="7b99f-121">트랜잭션 노드 위치를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="7b99f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7b99f-122">-Name</span></span>
<span data-ttu-id="7b99f-123">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b99f-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7b99f-124">-NoWait</span></span>
<span data-ttu-id="7b99f-125">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="7b99f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7b99f-126">-Password</span><span class="sxs-lookup"><span data-stu-id="7b99f-126">-Password</span></span>
<span data-ttu-id="7b99f-127">트랜잭션 노드 dns 엔드포인트 기본 인증 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="7b99f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b99f-128">-ResourceGroupName</span></span>
<span data-ttu-id="7b99f-129">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7b99f-130">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7b99f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b99f-131">-SubscriptionId</span></span>
<span data-ttu-id="7b99f-132">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7b99f-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-133">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b99f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="7b99f-134">-Confirm</span></span>
<span data-ttu-id="7b99f-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b99f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b99f-136">-WhatIf</span></span>
<span data-ttu-id="7b99f-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b99f-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b99f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b99f-139">CommonParameters</span></span>
<span data-ttu-id="7b99f-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b99f-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b99f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b99f-142">입력</span><span class="sxs-lookup"><span data-stu-id="7b99f-142">INPUTS</span></span>

## <span data-ttu-id="7b99f-143">출력</span><span class="sxs-lookup"><span data-stu-id="7b99f-143">OUTPUTS</span></span>

### <span data-ttu-id="7b99f-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="7b99f-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="7b99f-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b99f-145">NOTES</span></span>

<span data-ttu-id="7b99f-146">별칭</span><span class="sxs-lookup"><span data-stu-id="7b99f-146">ALIASES</span></span>

<span data-ttu-id="7b99f-147">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7b99f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b99f-148">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b99f-149">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b99f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b99f-150">FIREWALLRULE <IFirewallRule[]>: 방화벽 규칙을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="7b99f-151">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 엔드 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="7b99f-152">`[RuleName <String>]`: 방화벽 규칙의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="7b99f-153">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b99f-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="7b99f-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b99f-154">RELATED LINKS</span></span>

