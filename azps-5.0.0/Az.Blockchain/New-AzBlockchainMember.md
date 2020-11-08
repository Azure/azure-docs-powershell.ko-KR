---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226262"
---
# <span data-ttu-id="240d0-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="240d0-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="240d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="240d0-102">SYNOPSIS</span></span>
<span data-ttu-id="240d0-103">Blockchain 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-103">Create a blockchain member.</span></span>

## <span data-ttu-id="240d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="240d0-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="240d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="240d0-105">DESCRIPTION</span></span>
<span data-ttu-id="240d0-106">Blockchain 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-106">Create a blockchain member.</span></span>

## <span data-ttu-id="240d0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="240d0-107">EXAMPLES</span></span>

### <span data-ttu-id="240d0-108">예제 1: 새 blockchain 구성원 만들기</span><span class="sxs-lookup"><span data-stu-id="240d0-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="240d0-109">이 명령은 새 blockchain 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="240d0-110">변수</span><span class="sxs-lookup"><span data-stu-id="240d0-110">PARAMETERS</span></span>

### <span data-ttu-id="240d0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="240d0-111">-AsJob</span></span>
<span data-ttu-id="240d0-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="240d0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="240d0-113">-컨소시엄</span><span class="sxs-lookup"><span data-stu-id="240d0-113">-Consortium</span></span>
<span data-ttu-id="240d0-114">Blockchain 구성원에 대 한 컨소시엄을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="240d0-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="240d0-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="240d0-116">관리 되는 컨소시엄 관리 계정 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="240d0-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="240d0-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="240d0-118">컨소시엄의 구성원에 대 한 표시 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="240d0-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="240d0-119">-ConsortiumRole</span></span>
<span data-ttu-id="240d0-120">컨소시엄에서 구성원의 역할을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="240d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240d0-121">-DefaultProfile</span></span>
<span data-ttu-id="240d0-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="240d0-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="240d0-123">-FirewallRule</span></span>
<span data-ttu-id="240d0-124">생성할 방화벽 규칙을 가져오거나 설정 하 고, FIREWALLRULE 속성에 대 한 참고 섹션을 참조 하 고, 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="240d0-125">-위치</span><span class="sxs-lookup"><span data-stu-id="240d0-125">-Location</span></span>
<span data-ttu-id="240d0-126">Blockchain 서비스의 지리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="240d0-127">-이름</span><span class="sxs-lookup"><span data-stu-id="240d0-127">-Name</span></span>
<span data-ttu-id="240d0-128">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240d0-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="240d0-129">-NoWait</span></span>
<span data-ttu-id="240d0-130">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="240d0-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="240d0-131">-암호</span><span class="sxs-lookup"><span data-stu-id="240d0-131">-Password</span></span>
<span data-ttu-id="240d0-132">Blockchain 구성원의 기본 인증 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="240d0-133">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="240d0-133">-Protocol</span></span>
<span data-ttu-id="240d0-134">Blockchain 프로토콜을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240d0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240d0-135">-ResourceGroupName</span></span>
<span data-ttu-id="240d0-136">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="240d0-137">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="240d0-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="240d0-138">-Sku</span></span>
<span data-ttu-id="240d0-139">Sku 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="240d0-140">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="240d0-140">-SkuTier</span></span>
<span data-ttu-id="240d0-141">Sku 계층을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="240d0-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="240d0-142">-SubscriptionId</span></span>
<span data-ttu-id="240d0-143">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="240d0-144">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="240d0-145">태그</span><span class="sxs-lookup"><span data-stu-id="240d0-145">-Tag</span></span>
<span data-ttu-id="240d0-146">서비스의 태그로, 리소스를 설명 하는 키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="240d0-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="240d0-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="240d0-148">노드 용량을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240d0-149">-확인</span><span class="sxs-lookup"><span data-stu-id="240d0-149">-Confirm</span></span>
<span data-ttu-id="240d0-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="240d0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="240d0-151">-WhatIf</span></span>
<span data-ttu-id="240d0-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="240d0-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="240d0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240d0-154">CommonParameters</span></span>
<span data-ttu-id="240d0-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240d0-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="240d0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240d0-157">입력</span><span class="sxs-lookup"><span data-stu-id="240d0-157">INPUTS</span></span>

## <span data-ttu-id="240d0-158">출력</span><span class="sxs-lookup"><span data-stu-id="240d0-158">OUTPUTS</span></span>

### <span data-ttu-id="240d0-159">Api20180601Preview. IBlockchainMember에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="240d0-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="240d0-160">상속자</span><span class="sxs-lookup"><span data-stu-id="240d0-160">NOTES</span></span>

<span data-ttu-id="240d0-161">별칭과</span><span class="sxs-lookup"><span data-stu-id="240d0-161">ALIASES</span></span>

<span data-ttu-id="240d0-162">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="240d0-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="240d0-163">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="240d0-164">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="240d0-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="240d0-165">FIREWALLRULE <IFirewallRule [] >: 방화벽 규칙을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="240d0-166">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 끝 IP 주소를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="240d0-167">`[RuleName <String>]`: 방화벽 규칙의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="240d0-168">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="240d0-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="240d0-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="240d0-169">RELATED LINKS</span></span>

