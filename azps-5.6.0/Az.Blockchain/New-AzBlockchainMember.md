---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: 15af3a6bb7e80020cd014bfbdd8ff944cafd187a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009355"
---
# <span data-ttu-id="b2be4-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="b2be4-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="b2be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2be4-102">SYNOPSIS</span></span>
<span data-ttu-id="b2be4-103">블록체인 멤버를 만드소서.</span><span class="sxs-lookup"><span data-stu-id="b2be4-103">Create a blockchain member.</span></span>

## <span data-ttu-id="b2be4-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2be4-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2be4-105">설명</span><span class="sxs-lookup"><span data-stu-id="b2be4-105">DESCRIPTION</span></span>
<span data-ttu-id="b2be4-106">블록체인 멤버를 만드소서.</span><span class="sxs-lookup"><span data-stu-id="b2be4-106">Create a blockchain member.</span></span>

## <span data-ttu-id="b2be4-107">예제</span><span class="sxs-lookup"><span data-stu-id="b2be4-107">EXAMPLES</span></span>

### <span data-ttu-id="b2be4-108">예제 1: 새 블록체인 멤버 만들기</span><span class="sxs-lookup"><span data-stu-id="b2be4-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="b2be4-109">이 명령은 새 블록체인 멤버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="b2be4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b2be4-110">PARAMETERS</span></span>

### <span data-ttu-id="b2be4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2be4-111">-AsJob</span></span>
<span data-ttu-id="b2be4-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b2be4-113">-Consortium</span><span class="sxs-lookup"><span data-stu-id="b2be4-113">-Consortium</span></span>
<span data-ttu-id="b2be4-114">블록체인 멤버에 대한 컨소시엄을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="b2be4-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="b2be4-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="b2be4-116">관리되는 컨소시엄 관리 계정 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="b2be4-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="b2be4-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="b2be4-118">컨소시엄에서 멤버의 표시 이름을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="b2be4-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="b2be4-119">-ConsortiumRole</span></span>
<span data-ttu-id="b2be4-120">컨소시엄에서 멤버의 역할을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="b2be4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2be4-121">-DefaultProfile</span></span>
<span data-ttu-id="b2be4-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2be4-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="b2be4-123">-FirewallRule</span></span>
<span data-ttu-id="b2be4-124">방화벽 규칙을 얻거나 설정하여 구성하기 위해 방화벽RULE 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b2be4-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="b2be4-125">-Location</span><span class="sxs-lookup"><span data-stu-id="b2be4-125">-Location</span></span>
<span data-ttu-id="b2be4-126">블록체인 서비스의 GEO 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="b2be4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b2be4-127">-Name</span></span>
<span data-ttu-id="b2be4-128">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="b2be4-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b2be4-129">-NoWait</span></span>
<span data-ttu-id="b2be4-130">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="b2be4-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b2be4-131">-Password</span><span class="sxs-lookup"><span data-stu-id="b2be4-131">-Password</span></span>
<span data-ttu-id="b2be4-132">블록체인 멤버의 기본 인증 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="b2be4-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b2be4-133">-Protocol</span></span>
<span data-ttu-id="b2be4-134">블록체인 프로토콜을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="b2be4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2be4-135">-ResourceGroupName</span></span>
<span data-ttu-id="b2be4-136">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b2be4-137">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b2be4-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="b2be4-138">-Sku</span></span>
<span data-ttu-id="b2be4-139">Sku 이름을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="b2be4-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="b2be4-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b2be4-140">-SkuTier</span></span>
<span data-ttu-id="b2be4-141">Sku 계층을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="b2be4-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="b2be4-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2be4-142">-SubscriptionId</span></span>
<span data-ttu-id="b2be4-143">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b2be4-144">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b2be4-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2be4-145">-Tag</span></span>
<span data-ttu-id="b2be4-146">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="b2be4-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b2be4-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="b2be4-148">노드 용량을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="b2be4-149">-확인</span><span class="sxs-lookup"><span data-stu-id="b2be4-149">-Confirm</span></span>
<span data-ttu-id="b2be4-150">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2be4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2be4-151">-WhatIf</span></span>
<span data-ttu-id="b2be4-152">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2be4-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2be4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2be4-154">CommonParameters</span></span>
<span data-ttu-id="b2be4-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2be4-156">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2be4-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2be4-157">입력</span><span class="sxs-lookup"><span data-stu-id="b2be4-157">INPUTS</span></span>

## <span data-ttu-id="b2be4-158">출력</span><span class="sxs-lookup"><span data-stu-id="b2be4-158">OUTPUTS</span></span>

### <span data-ttu-id="b2be4-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="b2be4-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="b2be4-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2be4-160">NOTES</span></span>

<span data-ttu-id="b2be4-161">별칭</span><span class="sxs-lookup"><span data-stu-id="b2be4-161">ALIASES</span></span>

<span data-ttu-id="b2be4-162">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b2be4-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2be4-163">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2be4-164">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2be4-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2be4-165">FIREWALLRULE <IFirewallRule[]>: 방화벽 규칙을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="b2be4-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="b2be4-166">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 엔드 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="b2be4-167">`[RuleName <String>]`: 방화벽 규칙의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="b2be4-168">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2be4-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="b2be4-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2be4-169">RELATED LINKS</span></span>

