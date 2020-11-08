---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049157"
---
# <span data-ttu-id="58355-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="58355-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="58355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58355-102">SYNOPSIS</span></span>
<span data-ttu-id="58355-103">트랜잭션 노드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58355-103">Delete the transaction node.</span></span>

## <span data-ttu-id="58355-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58355-104">SYNTAX</span></span>

### <span data-ttu-id="58355-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="58355-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="58355-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="58355-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="58355-107">설명은</span><span class="sxs-lookup"><span data-stu-id="58355-107">DESCRIPTION</span></span>
<span data-ttu-id="58355-108">트랜잭션 노드를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58355-108">Delete the transaction node.</span></span>

## <span data-ttu-id="58355-109">예제의</span><span class="sxs-lookup"><span data-stu-id="58355-109">EXAMPLES</span></span>

### <span data-ttu-id="58355-110">예제 1: 트랜잭션 노드 제거</span><span class="sxs-lookup"><span data-stu-id="58355-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="58355-111">이 명령은 트랜잭션 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58355-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="58355-112">예제 2: 트랜잭션 노드 제거</span><span class="sxs-lookup"><span data-stu-id="58355-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="58355-113">이 명령은 트랜잭션 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58355-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="58355-114">변수</span><span class="sxs-lookup"><span data-stu-id="58355-114">PARAMETERS</span></span>

### <span data-ttu-id="58355-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58355-115">-AsJob</span></span>
<span data-ttu-id="58355-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="58355-116">Run the command as a job</span></span>

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

### <span data-ttu-id="58355-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="58355-117">-BlockchainMemberName</span></span>
<span data-ttu-id="58355-118">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-118">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58355-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58355-119">-DefaultProfile</span></span>
<span data-ttu-id="58355-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58355-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58355-121">-InputObject</span></span>
<span data-ttu-id="58355-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58355-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58355-123">-이름</span><span class="sxs-lookup"><span data-stu-id="58355-123">-Name</span></span>
<span data-ttu-id="58355-124">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58355-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="58355-125">-NoWait</span></span>
<span data-ttu-id="58355-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="58355-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="58355-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58355-127">-PassThru</span></span>
<span data-ttu-id="58355-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58355-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="58355-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58355-129">-ResourceGroupName</span></span>
<span data-ttu-id="58355-130">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="58355-131">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58355-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58355-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58355-132">-SubscriptionId</span></span>
<span data-ttu-id="58355-133">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58355-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="58355-134">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-134">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58355-135">-확인</span><span class="sxs-lookup"><span data-stu-id="58355-135">-Confirm</span></span>
<span data-ttu-id="58355-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58355-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58355-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58355-137">-WhatIf</span></span>
<span data-ttu-id="58355-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58355-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58355-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58355-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58355-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58355-140">CommonParameters</span></span>
<span data-ttu-id="58355-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58355-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58355-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58355-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58355-143">입력</span><span class="sxs-lookup"><span data-stu-id="58355-143">INPUTS</span></span>

### <span data-ttu-id="58355-144">IBlockchainIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="58355-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="58355-145">출력</span><span class="sxs-lookup"><span data-stu-id="58355-145">OUTPUTS</span></span>

### <span data-ttu-id="58355-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="58355-146">System.Boolean</span></span>

## <span data-ttu-id="58355-147">상속자</span><span class="sxs-lookup"><span data-stu-id="58355-147">NOTES</span></span>

<span data-ttu-id="58355-148">별칭과</span><span class="sxs-lookup"><span data-stu-id="58355-148">ALIASES</span></span>

<span data-ttu-id="58355-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="58355-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="58355-150">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58355-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58355-151">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="58355-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="58355-152">INPUTOBJECT <IBlockchainIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="58355-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="58355-153">`[BlockchainMemberName <String>]`: Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="58355-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="58355-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="58355-155">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="58355-156">`[OperationId <String>]`: 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="58355-157">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="58355-158">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58355-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="58355-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58355-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="58355-160">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="58355-161">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58355-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="58355-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58355-162">RELATED LINKS</span></span>

