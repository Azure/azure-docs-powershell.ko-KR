---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200921"
---
# <span data-ttu-id="8dc88-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="8dc88-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="8dc88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc88-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc88-103">트랜잭션 노드의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="8dc88-104">구문</span><span class="sxs-lookup"><span data-stu-id="8dc88-104">SYNTAX</span></span>

### <span data-ttu-id="8dc88-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="8dc88-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8dc88-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8dc88-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8dc88-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8dc88-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dc88-108">설명</span><span class="sxs-lookup"><span data-stu-id="8dc88-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc88-109">트랜잭션 노드의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="8dc88-110">예제</span><span class="sxs-lookup"><span data-stu-id="8dc88-110">EXAMPLES</span></span>

### <span data-ttu-id="8dc88-111">예제 1: 블록체인 멤버에 대한 트랜잭션 노드 나열</span><span class="sxs-lookup"><span data-stu-id="8dc88-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="8dc88-112">이 명령은 블록체인 멤버에 대한 트랜잭션 노드를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="8dc88-113">예제 2: 트랜잭션 노드를 얻게</span><span class="sxs-lookup"><span data-stu-id="8dc88-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="8dc88-114">이 명령은 트랜잭션 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="8dc88-115">예제 3: 트랜잭션 노드를 얻게</span><span class="sxs-lookup"><span data-stu-id="8dc88-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="8dc88-116">이 명령은 트랜잭션 노드를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="8dc88-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc88-117">PARAMETERS</span></span>

### <span data-ttu-id="8dc88-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="8dc88-118">-BlockchainMemberName</span></span>
<span data-ttu-id="8dc88-119">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="8dc88-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc88-120">-DefaultProfile</span></span>
<span data-ttu-id="8dc88-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc88-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc88-122">-InputObject</span></span>
<span data-ttu-id="8dc88-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8dc88-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8dc88-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8dc88-124">-Name</span></span>
<span data-ttu-id="8dc88-125">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-125">Transaction node name.</span></span>

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

### <span data-ttu-id="8dc88-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc88-126">-ResourceGroupName</span></span>
<span data-ttu-id="8dc88-127">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8dc88-128">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8dc88-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8dc88-129">-SubscriptionId</span></span>
<span data-ttu-id="8dc88-130">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8dc88-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8dc88-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc88-132">CommonParameters</span></span>
<span data-ttu-id="8dc88-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc88-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8dc88-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc88-135">입력</span><span class="sxs-lookup"><span data-stu-id="8dc88-135">INPUTS</span></span>

### <span data-ttu-id="8dc88-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="8dc88-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="8dc88-137">출력</span><span class="sxs-lookup"><span data-stu-id="8dc88-137">OUTPUTS</span></span>

### <span data-ttu-id="8dc88-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="8dc88-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="8dc88-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8dc88-139">NOTES</span></span>

<span data-ttu-id="8dc88-140">별칭</span><span class="sxs-lookup"><span data-stu-id="8dc88-140">ALIASES</span></span>

<span data-ttu-id="8dc88-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8dc88-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8dc88-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8dc88-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8dc88-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8dc88-144">INPUTOBJECT: <IBlockchainIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8dc88-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8dc88-145">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="8dc88-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8dc88-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8dc88-147">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="8dc88-148">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="8dc88-149">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8dc88-150">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8dc88-151">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="8dc88-152">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="8dc88-153">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc88-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="8dc88-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dc88-154">RELATED LINKS</span></span>

