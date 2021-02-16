---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177956"
---
# <span data-ttu-id="f93db-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="f93db-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="f93db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f93db-102">SYNOPSIS</span></span>
<span data-ttu-id="f93db-103">블록체인 멤버를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-103">Create a blockchain member.</span></span>

## <span data-ttu-id="f93db-104">구문</span><span class="sxs-lookup"><span data-stu-id="f93db-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f93db-105">설명</span><span class="sxs-lookup"><span data-stu-id="f93db-105">DESCRIPTION</span></span>
<span data-ttu-id="f93db-106">블록체인 멤버를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-106">Create a blockchain member.</span></span>

## <span data-ttu-id="f93db-107">예제</span><span class="sxs-lookup"><span data-stu-id="f93db-107">EXAMPLES</span></span>

### <span data-ttu-id="f93db-108">예제 1: 새 블록체인 멤버 만들기</span><span class="sxs-lookup"><span data-stu-id="f93db-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f93db-109">이 명령은 새 블록체인 멤버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="f93db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f93db-110">PARAMETERS</span></span>

### <span data-ttu-id="f93db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f93db-111">-AsJob</span></span>
<span data-ttu-id="f93db-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="f93db-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f93db-113">-컨소시엄</span><span class="sxs-lookup"><span data-stu-id="f93db-113">-Consortium</span></span>
<span data-ttu-id="f93db-114">블록체인 멤버에 대한 컨소시엄을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="f93db-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="f93db-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="f93db-116">관리되는 컨소시엄 관리 계정 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="f93db-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="f93db-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="f93db-118">컨소시엄에서 멤버의 표시 이름을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="f93db-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="f93db-119">-ConsortiumRole</span></span>
<span data-ttu-id="f93db-120">컨소시엄에서 멤버의 역할을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="f93db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93db-121">-DefaultProfile</span></span>
<span data-ttu-id="f93db-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f93db-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="f93db-123">-FirewallRule</span></span>
<span data-ttu-id="f93db-124">방화벽 규칙을 얻거나 설정하여 생성합니다. FIREWALLRULE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f93db-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="f93db-125">-Location</span><span class="sxs-lookup"><span data-stu-id="f93db-125">-Location</span></span>
<span data-ttu-id="f93db-126">블록체인 서비스의 GEO 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="f93db-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f93db-127">-Name</span></span>
<span data-ttu-id="f93db-128">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="f93db-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f93db-129">-NoWait</span></span>
<span data-ttu-id="f93db-130">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="f93db-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f93db-131">-Password</span><span class="sxs-lookup"><span data-stu-id="f93db-131">-Password</span></span>
<span data-ttu-id="f93db-132">블록체인 멤버의 기본 인증 암호를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="f93db-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f93db-133">-Protocol</span></span>
<span data-ttu-id="f93db-134">블록체인 프로토콜을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="f93db-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f93db-135">-ResourceGroupName</span></span>
<span data-ttu-id="f93db-136">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f93db-137">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f93db-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="f93db-138">-Sku</span></span>
<span data-ttu-id="f93db-139">SKU 이름을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="f93db-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="f93db-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f93db-140">-SkuTier</span></span>
<span data-ttu-id="f93db-141">SKU 계층을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="f93db-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="f93db-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f93db-142">-SubscriptionId</span></span>
<span data-ttu-id="f93db-143">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f93db-144">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f93db-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="f93db-145">-Tag</span></span>
<span data-ttu-id="f93db-146">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="f93db-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f93db-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="f93db-148">노드 용량을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="f93db-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f93db-149">-Confirm</span></span>
<span data-ttu-id="f93db-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f93db-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f93db-151">-WhatIf</span></span>
<span data-ttu-id="f93db-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f93db-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f93db-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f93db-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93db-154">CommonParameters</span></span>
<span data-ttu-id="f93db-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93db-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f93db-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93db-157">입력</span><span class="sxs-lookup"><span data-stu-id="f93db-157">INPUTS</span></span>

## <span data-ttu-id="f93db-158">출력</span><span class="sxs-lookup"><span data-stu-id="f93db-158">OUTPUTS</span></span>

### <span data-ttu-id="f93db-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="f93db-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="f93db-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f93db-160">NOTES</span></span>

<span data-ttu-id="f93db-161">별칭</span><span class="sxs-lookup"><span data-stu-id="f93db-161">ALIASES</span></span>

<span data-ttu-id="f93db-162">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f93db-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f93db-163">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f93db-164">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f93db-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f93db-165">FIREWALLRULE <IFirewallRule[]>: 방화벽 규칙을 얻거나 설정</span><span class="sxs-lookup"><span data-stu-id="f93db-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="f93db-166">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 끝 IP 주소를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="f93db-167">`[RuleName <String>]`: 방화벽 규칙의 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="f93db-168">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 갖거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f93db-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="f93db-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f93db-169">RELATED LINKS</span></span>

