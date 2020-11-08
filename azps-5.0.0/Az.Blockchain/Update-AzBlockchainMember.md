---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216418"
---
# <span data-ttu-id="37b5a-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="37b5a-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="37b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="37b5a-103">Blockchain 구성원을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-103">Update a blockchain member.</span></span>

## <span data-ttu-id="37b5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37b5a-104">SYNTAX</span></span>

### <span data-ttu-id="37b5a-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="37b5a-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="37b5a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="37b5a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="37b5a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="37b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="37b5a-108">Blockchain 구성원을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-108">Update a blockchain member.</span></span>

## <span data-ttu-id="37b5a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="37b5a-109">EXAMPLES</span></span>

### <span data-ttu-id="37b5a-110">예제 1: blockchain 구성원 업데이트</span><span class="sxs-lookup"><span data-stu-id="37b5a-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="37b5a-111">이 명령은 blockchain 구성원을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="37b5a-112">예제 2: blockchain 구성원 업데이트</span><span class="sxs-lookup"><span data-stu-id="37b5a-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="37b5a-113">이 명령은 blockchain 구성원을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="37b5a-114">변수</span><span class="sxs-lookup"><span data-stu-id="37b5a-114">PARAMETERS</span></span>

### <span data-ttu-id="37b5a-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="37b5a-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="37b5a-116">관리 되는 컨소시엄 관리 계정 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="37b5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b5a-117">-DefaultProfile</span></span>
<span data-ttu-id="37b5a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37b5a-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="37b5a-119">-FirewallRule</span></span>
<span data-ttu-id="37b5a-120">방화벽 규칙을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="37b5a-121">생성 하려면 FIREWALLRULE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="37b5a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b5a-122">-InputObject</span></span>
<span data-ttu-id="37b5a-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="37b5a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="37b5a-124">-Name</span></span>
<span data-ttu-id="37b5a-125">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-125">Blockchain member name.</span></span>

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

### <span data-ttu-id="37b5a-126">-암호</span><span class="sxs-lookup"><span data-stu-id="37b5a-126">-Password</span></span>
<span data-ttu-id="37b5a-127">트랜잭션 노드 dns 끝점 기본 인증 암호를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="37b5a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b5a-128">-ResourceGroupName</span></span>
<span data-ttu-id="37b5a-129">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="37b5a-130">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="37b5a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37b5a-131">-SubscriptionId</span></span>
<span data-ttu-id="37b5a-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="37b5a-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="37b5a-134">태그</span><span class="sxs-lookup"><span data-stu-id="37b5a-134">-Tag</span></span>
<span data-ttu-id="37b5a-135">서비스의 태그로, 리소스를 설명 하는 키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="37b5a-136">-확인</span><span class="sxs-lookup"><span data-stu-id="37b5a-136">-Confirm</span></span>
<span data-ttu-id="37b5a-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b5a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b5a-138">-WhatIf</span></span>
<span data-ttu-id="37b5a-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b5a-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b5a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b5a-141">CommonParameters</span></span>
<span data-ttu-id="37b5a-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b5a-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="37b5a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b5a-144">입력</span><span class="sxs-lookup"><span data-stu-id="37b5a-144">INPUTS</span></span>

### <span data-ttu-id="37b5a-145">IBlockchainIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="37b5a-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="37b5a-146">출력</span><span class="sxs-lookup"><span data-stu-id="37b5a-146">OUTPUTS</span></span>

### <span data-ttu-id="37b5a-147">Api20180601Preview. IBlockchainMember에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="37b5a-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="37b5a-148">상속자</span><span class="sxs-lookup"><span data-stu-id="37b5a-148">NOTES</span></span>

<span data-ttu-id="37b5a-149">별칭과</span><span class="sxs-lookup"><span data-stu-id="37b5a-149">ALIASES</span></span>

<span data-ttu-id="37b5a-150">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="37b5a-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37b5a-151">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37b5a-152">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="37b5a-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37b5a-153">FIREWALLRULE <IFirewallRule [] >: 방화벽 규칙을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="37b5a-154">`[EndIPAddress <String>]`: 방화벽 규칙 범위의 끝 IP 주소를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="37b5a-155">`[RuleName <String>]`: 방화벽 규칙의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="37b5a-156">`[StartIPAddress <String>]`: 방화벽 규칙 범위의 시작 IP 주소를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="37b5a-157">INPUTOBJECT <IBlockchainIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37b5a-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37b5a-158">`[BlockchainMemberName <String>]`: Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="37b5a-159">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="37b5a-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37b5a-160">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="37b5a-161">`[OperationId <String>]`: 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="37b5a-162">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="37b5a-163">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="37b5a-164">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="37b5a-165">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="37b5a-166">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37b5a-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="37b5a-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37b5a-167">RELATED LINKS</span></span>

