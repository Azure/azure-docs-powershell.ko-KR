---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226260"
---
# <span data-ttu-id="a5b08-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="a5b08-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="a5b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b08-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b08-103">트랜잭션 노드를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="a5b08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5b08-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5b08-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5b08-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b08-106">트랜잭션 노드를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="a5b08-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5b08-107">EXAMPLES</span></span>

### <span data-ttu-id="a5b08-108">예제 1: blockchain 트랜잭션 노드 만들기</span><span class="sxs-lookup"><span data-stu-id="a5b08-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="a5b08-109">이 명령은 blockchain 트랜잭션 노드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="a5b08-110">변수</span><span class="sxs-lookup"><span data-stu-id="a5b08-110">PARAMETERS</span></span>

### <span data-ttu-id="a5b08-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5b08-111">-AsJob</span></span>
<span data-ttu-id="a5b08-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a5b08-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a5b08-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="a5b08-113">-BlockchainMemberName</span></span>
<span data-ttu-id="a5b08-114">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="a5b08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b08-115">-DefaultProfile</span></span>
<span data-ttu-id="a5b08-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b08-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="a5b08-117">-FirewallRule</span></span>
<span data-ttu-id="a5b08-118">방화벽 규칙을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="a5b08-119">생성 하려면 FIREWALLRULE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a5b08-120">-위치</span><span class="sxs-lookup"><span data-stu-id="a5b08-120">-Location</span></span>
<span data-ttu-id="a5b08-121">트랜잭션 노드 위치를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="a5b08-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a5b08-122">-Name</span></span>
<span data-ttu-id="a5b08-123">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-123">Transaction node name.</span></span>

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

### <span data-ttu-id="a5b08-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a5b08-124">-NoWait</span></span>
<span data-ttu-id="a5b08-125">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a5b08-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a5b08-126">-암호</span><span class="sxs-lookup"><span data-stu-id="a5b08-126">-Password</span></span>
<span data-ttu-id="a5b08-127">트랜잭션 노드 dns 끝점 기본 인증 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="a5b08-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b08-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5b08-129">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a5b08-130">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a5b08-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5b08-131">-SubscriptionId</span></span>
<span data-ttu-id="a5b08-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5b08-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a5b08-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a5b08-134">-Confirm</span></span>
<span data-ttu-id="a5b08-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b08-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b08-136">-WhatIf</span></span>
<span data-ttu-id="a5b08-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b08-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b08-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b08-139">CommonParameters</span></span>
<span data-ttu-id="a5b08-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b08-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5b08-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b08-142">입력</span><span class="sxs-lookup"><span data-stu-id="a5b08-142">INPUTS</span></span>

## <span data-ttu-id="a5b08-143">출력</span><span class="sxs-lookup"><span data-stu-id="a5b08-143">OUTPUTS</span></span>

### <span data-ttu-id="a5b08-144">Api20180601Preview. ITransactionNode에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a5b08-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="a5b08-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a5b08-145">NOTES</span></span>

<span data-ttu-id="a5b08-146">별칭과</span><span class="sxs-lookup"><span data-stu-id="a5b08-146">ALIASES</span></span>

<span data-ttu-id="a5b08-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a5b08-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a5b08-148">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a5b08-149">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5b08-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a5b08-150">FIREWALLRULE <IFirewallRule [] >: 방화벽 규칙을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="a5b08-151">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 끝 IP 주소를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="a5b08-152">`[RuleName <String>]`: 방화벽 규칙의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="a5b08-153">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b08-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="a5b08-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5b08-154">RELATED LINKS</span></span>

