---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 54678dd00a0edae4af3a90c84e1c930c1c032e84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972128"
---
# <span data-ttu-id="65d1a-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="65d1a-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="65d1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="65d1a-103">블록체인 멤버를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="65d1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="65d1a-104">SYNTAX</span></span>

### <span data-ttu-id="65d1a-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="65d1a-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65d1a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="65d1a-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65d1a-107">설명</span><span class="sxs-lookup"><span data-stu-id="65d1a-107">DESCRIPTION</span></span>
<span data-ttu-id="65d1a-108">블록체인 멤버를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="65d1a-109">예제</span><span class="sxs-lookup"><span data-stu-id="65d1a-109">EXAMPLES</span></span>

### <span data-ttu-id="65d1a-110">예제 1: 블록체인 멤버 제거</span><span class="sxs-lookup"><span data-stu-id="65d1a-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="65d1a-111">이 명령은 블록체인 멤버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="65d1a-112">예제 2: 블록체인 멤버 제거</span><span class="sxs-lookup"><span data-stu-id="65d1a-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="65d1a-113">이 명령은 블록체인 멤버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="65d1a-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65d1a-114">PARAMETERS</span></span>

### <span data-ttu-id="65d1a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65d1a-115">-AsJob</span></span>
<span data-ttu-id="65d1a-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="65d1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d1a-117">-DefaultProfile</span></span>
<span data-ttu-id="65d1a-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d1a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65d1a-119">-InputObject</span></span>
<span data-ttu-id="65d1a-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="65d1a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="65d1a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="65d1a-121">-Name</span></span>
<span data-ttu-id="65d1a-122">블록체인 멤버 이름</span><span class="sxs-lookup"><span data-stu-id="65d1a-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d1a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="65d1a-123">-NoWait</span></span>
<span data-ttu-id="65d1a-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="65d1a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="65d1a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65d1a-125">-PassThru</span></span>
<span data-ttu-id="65d1a-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="65d1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="65d1a-128">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="65d1a-129">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="65d1a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65d1a-130">-SubscriptionId</span></span>
<span data-ttu-id="65d1a-131">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="65d1a-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="65d1a-133">-확인</span><span class="sxs-lookup"><span data-stu-id="65d1a-133">-Confirm</span></span>
<span data-ttu-id="65d1a-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d1a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d1a-135">-WhatIf</span></span>
<span data-ttu-id="65d1a-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d1a-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d1a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d1a-138">CommonParameters</span></span>
<span data-ttu-id="65d1a-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d1a-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65d1a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d1a-141">입력</span><span class="sxs-lookup"><span data-stu-id="65d1a-141">INPUTS</span></span>

### <span data-ttu-id="65d1a-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="65d1a-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="65d1a-143">출력</span><span class="sxs-lookup"><span data-stu-id="65d1a-143">OUTPUTS</span></span>

### <span data-ttu-id="65d1a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65d1a-144">System.Boolean</span></span>

## <span data-ttu-id="65d1a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65d1a-145">NOTES</span></span>

<span data-ttu-id="65d1a-146">별칭</span><span class="sxs-lookup"><span data-stu-id="65d1a-146">ALIASES</span></span>

<span data-ttu-id="65d1a-147">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="65d1a-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65d1a-148">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65d1a-149">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="65d1a-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65d1a-150">INPUTOBJECT <IBlockchainIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="65d1a-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="65d1a-151">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="65d1a-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="65d1a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65d1a-153">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="65d1a-154">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="65d1a-155">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="65d1a-156">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="65d1a-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="65d1a-158">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="65d1a-159">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65d1a-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="65d1a-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65d1a-160">RELATED LINKS</span></span>

