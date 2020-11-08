---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226268"
---
# <span data-ttu-id="33191-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="33191-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="33191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33191-102">SYNOPSIS</span></span>
<span data-ttu-id="33191-103">트랜잭션 노드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33191-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="33191-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33191-104">SYNTAX</span></span>

### <span data-ttu-id="33191-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="33191-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="33191-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="33191-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="33191-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="33191-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="33191-108">설명은</span><span class="sxs-lookup"><span data-stu-id="33191-108">DESCRIPTION</span></span>
<span data-ttu-id="33191-109">트랜잭션 노드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33191-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="33191-110">예제의</span><span class="sxs-lookup"><span data-stu-id="33191-110">EXAMPLES</span></span>

### <span data-ttu-id="33191-111">예제 1: blockchain 구성원에 대 한 트랜잭션 노드 나열</span><span class="sxs-lookup"><span data-stu-id="33191-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="33191-112">이 명령은 blockchain 구성원에 대 한 트랜잭션 노드를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="33191-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="33191-113">예제 2: 트랜잭션 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="33191-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="33191-114">이 명령은 트랜잭션 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33191-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="33191-115">예제 3: 트랜잭션 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="33191-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="33191-116">이 명령은 트랜잭션 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33191-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="33191-117">변수</span><span class="sxs-lookup"><span data-stu-id="33191-117">PARAMETERS</span></span>

### <span data-ttu-id="33191-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="33191-118">-BlockchainMemberName</span></span>
<span data-ttu-id="33191-119">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="33191-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33191-120">-DefaultProfile</span></span>
<span data-ttu-id="33191-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33191-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33191-122">-InputObject</span></span>
<span data-ttu-id="33191-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33191-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="33191-124">-이름</span><span class="sxs-lookup"><span data-stu-id="33191-124">-Name</span></span>
<span data-ttu-id="33191-125">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33191-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33191-126">-ResourceGroupName</span></span>
<span data-ttu-id="33191-127">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="33191-128">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33191-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="33191-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33191-129">-SubscriptionId</span></span>
<span data-ttu-id="33191-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33191-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="33191-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33191-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33191-132">CommonParameters</span></span>
<span data-ttu-id="33191-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33191-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33191-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33191-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33191-135">입력</span><span class="sxs-lookup"><span data-stu-id="33191-135">INPUTS</span></span>

### <span data-ttu-id="33191-136">IBlockchainIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="33191-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="33191-137">출력</span><span class="sxs-lookup"><span data-stu-id="33191-137">OUTPUTS</span></span>

### <span data-ttu-id="33191-138">Api20180601Preview. ITransactionNode에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33191-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="33191-139">상속자</span><span class="sxs-lookup"><span data-stu-id="33191-139">NOTES</span></span>

<span data-ttu-id="33191-140">별칭과</span><span class="sxs-lookup"><span data-stu-id="33191-140">ALIASES</span></span>

<span data-ttu-id="33191-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="33191-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="33191-142">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="33191-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="33191-143">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="33191-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="33191-144">INPUTOBJECT <IBlockchainIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="33191-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="33191-145">`[BlockchainMemberName <String>]`: Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="33191-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="33191-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="33191-147">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="33191-148">`[OperationId <String>]`: 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="33191-149">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="33191-150">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33191-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="33191-151">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33191-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="33191-152">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="33191-153">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33191-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="33191-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33191-154">RELATED LINKS</span></span>

