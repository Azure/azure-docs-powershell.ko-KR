---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181961"
---
# <span data-ttu-id="f85b0-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="f85b0-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="f85b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f85b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f85b0-103">블록체인 멤버에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="f85b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="f85b0-104">SYNTAX</span></span>

### <span data-ttu-id="f85b0-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="f85b0-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f85b0-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="f85b0-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f85b0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f85b0-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f85b0-108">목록</span><span class="sxs-lookup"><span data-stu-id="f85b0-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f85b0-109">설명</span><span class="sxs-lookup"><span data-stu-id="f85b0-109">DESCRIPTION</span></span>
<span data-ttu-id="f85b0-110">블록체인 멤버에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="f85b0-111">예제</span><span class="sxs-lookup"><span data-stu-id="f85b0-111">EXAMPLES</span></span>

### <span data-ttu-id="f85b0-112">예제 1: 블록체인 멤버 나열</span><span class="sxs-lookup"><span data-stu-id="f85b0-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f85b0-113">이 명령은 구독의 블록체인 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="f85b0-114">예제 2: 블록체인 멤버 나열</span><span class="sxs-lookup"><span data-stu-id="f85b0-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f85b0-115">이 명령은 리소스 그룹 아래에 블록체인 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="f85b0-116">예제 3: 블록체인 멤버 얻기</span><span class="sxs-lookup"><span data-stu-id="f85b0-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f85b0-117">이 명령은 리소스 그룹에서 블록체인 멤버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="f85b0-118">예제 4: 블록체인 멤버 얻기</span><span class="sxs-lookup"><span data-stu-id="f85b0-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="f85b0-119">이 명령은 리소스 그룹에서 블록체인 멤버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="f85b0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f85b0-120">PARAMETERS</span></span>

### <span data-ttu-id="f85b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85b0-121">-DefaultProfile</span></span>
<span data-ttu-id="f85b0-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f85b0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f85b0-123">-InputObject</span></span>
<span data-ttu-id="f85b0-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f85b0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f85b0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f85b0-125">-Name</span></span>
<span data-ttu-id="f85b0-126">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f85b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="f85b0-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f85b0-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f85b0-130">-SubscriptionId</span></span>
<span data-ttu-id="f85b0-131">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f85b0-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85b0-133">CommonParameters</span></span>
<span data-ttu-id="f85b0-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85b0-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f85b0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85b0-136">입력</span><span class="sxs-lookup"><span data-stu-id="f85b0-136">INPUTS</span></span>

### <span data-ttu-id="f85b0-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="f85b0-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="f85b0-138">출력</span><span class="sxs-lookup"><span data-stu-id="f85b0-138">OUTPUTS</span></span>

### <span data-ttu-id="f85b0-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="f85b0-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="f85b0-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f85b0-140">NOTES</span></span>

<span data-ttu-id="f85b0-141">별칭</span><span class="sxs-lookup"><span data-stu-id="f85b0-141">ALIASES</span></span>

<span data-ttu-id="f85b0-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f85b0-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f85b0-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f85b0-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f85b0-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f85b0-145">INPUTOBJECT: <IBlockchainIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f85b0-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f85b0-146">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="f85b0-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="f85b0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f85b0-148">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="f85b0-149">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="f85b0-150">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f85b0-151">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f85b0-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="f85b0-153">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="f85b0-154">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85b0-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="f85b0-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f85b0-155">RELATED LINKS</span></span>

