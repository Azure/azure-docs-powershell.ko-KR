---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363231"
---
# <span data-ttu-id="78139-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="78139-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="78139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78139-102">SYNOPSIS</span></span>
<span data-ttu-id="78139-103">트랜잭션 노드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="78139-103">Delete the transaction node.</span></span>

## <span data-ttu-id="78139-104">구문</span><span class="sxs-lookup"><span data-stu-id="78139-104">SYNTAX</span></span>

### <span data-ttu-id="78139-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="78139-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="78139-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="78139-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78139-107">설명</span><span class="sxs-lookup"><span data-stu-id="78139-107">DESCRIPTION</span></span>
<span data-ttu-id="78139-108">트랜잭션 노드를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="78139-108">Delete the transaction node.</span></span>

## <span data-ttu-id="78139-109">예제</span><span class="sxs-lookup"><span data-stu-id="78139-109">EXAMPLES</span></span>

### <span data-ttu-id="78139-110">예제 1: 트랜잭션 노드 제거</span><span class="sxs-lookup"><span data-stu-id="78139-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="78139-111">이 명령은 트랜잭션 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78139-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="78139-112">예제 2: 트랜잭션 노드 제거</span><span class="sxs-lookup"><span data-stu-id="78139-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="78139-113">이 명령은 트랜잭션 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78139-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="78139-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78139-114">PARAMETERS</span></span>

### <span data-ttu-id="78139-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78139-115">-AsJob</span></span>
<span data-ttu-id="78139-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="78139-116">Run the command as a job</span></span>

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

### <span data-ttu-id="78139-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="78139-117">-BlockchainMemberName</span></span>
<span data-ttu-id="78139-118">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="78139-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78139-119">-DefaultProfile</span></span>
<span data-ttu-id="78139-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78139-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78139-121">-InputObject</span></span>
<span data-ttu-id="78139-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="78139-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="78139-123">-Name</span><span class="sxs-lookup"><span data-stu-id="78139-123">-Name</span></span>
<span data-ttu-id="78139-124">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-124">Transaction node name.</span></span>

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

### <span data-ttu-id="78139-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="78139-125">-NoWait</span></span>
<span data-ttu-id="78139-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="78139-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="78139-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78139-127">-PassThru</span></span>
<span data-ttu-id="78139-128">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="78139-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="78139-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78139-129">-ResourceGroupName</span></span>
<span data-ttu-id="78139-130">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="78139-131">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78139-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="78139-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78139-132">-SubscriptionId</span></span>
<span data-ttu-id="78139-133">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="78139-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="78139-134">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="78139-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78139-135">-Confirm</span></span>
<span data-ttu-id="78139-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78139-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78139-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78139-137">-WhatIf</span></span>
<span data-ttu-id="78139-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="78139-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78139-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78139-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78139-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78139-140">CommonParameters</span></span>
<span data-ttu-id="78139-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78139-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78139-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78139-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78139-143">입력</span><span class="sxs-lookup"><span data-stu-id="78139-143">INPUTS</span></span>

### <span data-ttu-id="78139-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="78139-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="78139-145">출력</span><span class="sxs-lookup"><span data-stu-id="78139-145">OUTPUTS</span></span>

### <span data-ttu-id="78139-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78139-146">System.Boolean</span></span>

## <span data-ttu-id="78139-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78139-147">NOTES</span></span>

<span data-ttu-id="78139-148">별칭</span><span class="sxs-lookup"><span data-stu-id="78139-148">ALIASES</span></span>

<span data-ttu-id="78139-149">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="78139-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78139-150">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="78139-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78139-151">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="78139-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78139-152">INPUTOBJECT: <IBlockchainIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="78139-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78139-153">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="78139-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="78139-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78139-155">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="78139-156">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="78139-157">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="78139-158">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78139-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="78139-159">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="78139-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="78139-160">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="78139-161">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78139-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="78139-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78139-162">RELATED LINKS</span></span>

