---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341817"
---
# <span data-ttu-id="913e3-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="913e3-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="913e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913e3-102">SYNOPSIS</span></span>
<span data-ttu-id="913e3-103">트랜잭션 노드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="913e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="913e3-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="913e3-105">설명</span><span class="sxs-lookup"><span data-stu-id="913e3-105">DESCRIPTION</span></span>
<span data-ttu-id="913e3-106">트랜잭션 노드를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="913e3-107">예제</span><span class="sxs-lookup"><span data-stu-id="913e3-107">EXAMPLES</span></span>

### <span data-ttu-id="913e3-108">예제 1: 블록체인 트랜잭션 노드 만들기</span><span class="sxs-lookup"><span data-stu-id="913e3-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="913e3-109">이 명령은 블록체인 트랜잭션 노드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="913e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="913e3-110">PARAMETERS</span></span>

### <span data-ttu-id="913e3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="913e3-111">-AsJob</span></span>
<span data-ttu-id="913e3-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="913e3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="913e3-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="913e3-113">-BlockchainMemberName</span></span>
<span data-ttu-id="913e3-114">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="913e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913e3-115">-DefaultProfile</span></span>
<span data-ttu-id="913e3-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913e3-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="913e3-117">-FirewallRule</span></span>
<span data-ttu-id="913e3-118">방화벽 규칙을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="913e3-119">구성을 위해 FIREWALLRULE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="913e3-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="913e3-120">-Location</span><span class="sxs-lookup"><span data-stu-id="913e3-120">-Location</span></span>
<span data-ttu-id="913e3-121">트랜잭션 노드 위치를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="913e3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="913e3-122">-Name</span></span>
<span data-ttu-id="913e3-123">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-123">Transaction node name.</span></span>

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

### <span data-ttu-id="913e3-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="913e3-124">-NoWait</span></span>
<span data-ttu-id="913e3-125">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="913e3-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="913e3-126">-Password</span><span class="sxs-lookup"><span data-stu-id="913e3-126">-Password</span></span>
<span data-ttu-id="913e3-127">트랜잭션 노드 dns 엔드포인트 기본 인증 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="913e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="913e3-129">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="913e3-130">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="913e3-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="913e3-131">-SubscriptionId</span></span>
<span data-ttu-id="913e3-132">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="913e3-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="913e3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="913e3-134">-Confirm</span></span>
<span data-ttu-id="913e3-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913e3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913e3-136">-WhatIf</span></span>
<span data-ttu-id="913e3-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="913e3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="913e3-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913e3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913e3-139">CommonParameters</span></span>
<span data-ttu-id="913e3-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913e3-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="913e3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913e3-142">입력</span><span class="sxs-lookup"><span data-stu-id="913e3-142">INPUTS</span></span>

## <span data-ttu-id="913e3-143">출력</span><span class="sxs-lookup"><span data-stu-id="913e3-143">OUTPUTS</span></span>

### <span data-ttu-id="913e3-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="913e3-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="913e3-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="913e3-145">NOTES</span></span>

<span data-ttu-id="913e3-146">별칭</span><span class="sxs-lookup"><span data-stu-id="913e3-146">ALIASES</span></span>

<span data-ttu-id="913e3-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="913e3-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="913e3-148">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="913e3-149">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="913e3-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="913e3-150">FIREWALLRULE <IFirewallRule[]>: 방화벽 규칙을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="913e3-151">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 끝 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="913e3-152">`[RuleName <String>]`: 방화벽 규칙의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="913e3-153">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 갖거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="913e3-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="913e3-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="913e3-154">RELATED LINKS</span></span>

