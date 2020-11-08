---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226276"
---
# <span data-ttu-id="672da-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="672da-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="672da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="672da-102">SYNOPSIS</span></span>
<span data-ttu-id="672da-103">Blockchain 구성원에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="672da-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="672da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="672da-104">SYNTAX</span></span>

### <span data-ttu-id="672da-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="672da-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="672da-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="672da-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="672da-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="672da-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="672da-108">목록</span><span class="sxs-lookup"><span data-stu-id="672da-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="672da-109">설명은</span><span class="sxs-lookup"><span data-stu-id="672da-109">DESCRIPTION</span></span>
<span data-ttu-id="672da-110">Blockchain 구성원에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="672da-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="672da-111">예제의</span><span class="sxs-lookup"><span data-stu-id="672da-111">EXAMPLES</span></span>

### <span data-ttu-id="672da-112">예제 1: List blockchain 구성원</span><span class="sxs-lookup"><span data-stu-id="672da-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="672da-113">이 명령은 구독 아래에 blockchain 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="672da-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="672da-114">예제 2: List blockchain 구성원</span><span class="sxs-lookup"><span data-stu-id="672da-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="672da-115">이 명령은 리소스 그룹 아래에 blockchain 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="672da-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="672da-116">예제 3: blockchain 구성원 가져오기</span><span class="sxs-lookup"><span data-stu-id="672da-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="672da-117">이 명령은 리소스 그룹 아래에 있는 blockchain 구성원을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="672da-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="672da-118">예제 4: blockchain 구성원 가져오기</span><span class="sxs-lookup"><span data-stu-id="672da-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="672da-119">이 명령은 리소스 그룹 아래에 있는 blockchain 구성원을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="672da-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="672da-120">변수</span><span class="sxs-lookup"><span data-stu-id="672da-120">PARAMETERS</span></span>

### <span data-ttu-id="672da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672da-121">-DefaultProfile</span></span>
<span data-ttu-id="672da-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="672da-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="672da-123">-InputObject</span></span>
<span data-ttu-id="672da-124">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="672da-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="672da-125">-이름</span><span class="sxs-lookup"><span data-stu-id="672da-125">-Name</span></span>
<span data-ttu-id="672da-126">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="672da-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672da-127">-ResourceGroupName</span></span>
<span data-ttu-id="672da-128">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="672da-129">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="672da-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="672da-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="672da-130">-SubscriptionId</span></span>
<span data-ttu-id="672da-131">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="672da-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="672da-132">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="672da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672da-133">CommonParameters</span></span>
<span data-ttu-id="672da-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="672da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672da-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="672da-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672da-136">입력</span><span class="sxs-lookup"><span data-stu-id="672da-136">INPUTS</span></span>

### <span data-ttu-id="672da-137">IBlockchainIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="672da-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="672da-138">출력</span><span class="sxs-lookup"><span data-stu-id="672da-138">OUTPUTS</span></span>

### <span data-ttu-id="672da-139">Api20180601Preview. IBlockchainMember에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="672da-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="672da-140">상속자</span><span class="sxs-lookup"><span data-stu-id="672da-140">NOTES</span></span>

<span data-ttu-id="672da-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="672da-141">ALIASES</span></span>

<span data-ttu-id="672da-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="672da-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="672da-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="672da-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="672da-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="672da-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="672da-145">INPUTOBJECT <IBlockchainIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="672da-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="672da-146">`[BlockchainMemberName <String>]`: Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="672da-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="672da-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="672da-148">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="672da-149">`[OperationId <String>]`: 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="672da-150">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="672da-151">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="672da-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="672da-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="672da-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="672da-153">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="672da-154">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="672da-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="672da-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="672da-155">RELATED LINKS</span></span>

