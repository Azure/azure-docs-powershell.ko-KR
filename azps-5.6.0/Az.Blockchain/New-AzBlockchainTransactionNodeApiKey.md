---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 418786855833164c3f9c15dcd2716ad00c8c6d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954875"
---
# <span data-ttu-id="49663-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="49663-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="49663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49663-102">SYNOPSIS</span></span>
<span data-ttu-id="49663-103">블록체인 멤버에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="49663-104">구문</span><span class="sxs-lookup"><span data-stu-id="49663-104">SYNTAX</span></span>

### <span data-ttu-id="49663-105">RegenerateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="49663-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49663-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="49663-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49663-107">설명</span><span class="sxs-lookup"><span data-stu-id="49663-107">DESCRIPTION</span></span>
<span data-ttu-id="49663-108">블록체인 멤버에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="49663-109">예제</span><span class="sxs-lookup"><span data-stu-id="49663-109">EXAMPLES</span></span>

### <span data-ttu-id="49663-110">예제 1: 이름을 사용하여 트랜잭션 노드에 대한 Api 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="49663-111">이 명령은 이름, 리소스 그룹을 사용하여 트랜잭션 노드에 대한 Api 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="49663-112">예제 2: 트랜잭션 노드에 대한 Api 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="49663-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="49663-113">이 명령은 ID를 사용하여 트랜잭션 노드에 대한 Api 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="49663-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49663-114">PARAMETERS</span></span>

### <span data-ttu-id="49663-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="49663-115">-BlockchainMemberName</span></span>
<span data-ttu-id="49663-116">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49663-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49663-117">-DefaultProfile</span></span>
<span data-ttu-id="49663-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49663-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49663-119">-InputObject</span></span>
<span data-ttu-id="49663-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="49663-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49663-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="49663-121">-KeyName</span></span>
<span data-ttu-id="49663-122">API 키 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="49663-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49663-123">-ResourceGroupName</span></span>
<span data-ttu-id="49663-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="49663-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49663-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49663-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49663-126">-SubscriptionId</span></span>
<span data-ttu-id="49663-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49663-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="49663-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49663-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="49663-129">-TransactionNodeName</span></span>
<span data-ttu-id="49663-130">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49663-131">-Value</span><span class="sxs-lookup"><span data-stu-id="49663-131">-Value</span></span>
<span data-ttu-id="49663-132">API 키 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="49663-133">-확인</span><span class="sxs-lookup"><span data-stu-id="49663-133">-Confirm</span></span>
<span data-ttu-id="49663-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49663-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49663-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49663-135">-WhatIf</span></span>
<span data-ttu-id="49663-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="49663-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49663-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49663-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49663-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49663-138">CommonParameters</span></span>
<span data-ttu-id="49663-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49663-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49663-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49663-141">입력</span><span class="sxs-lookup"><span data-stu-id="49663-141">INPUTS</span></span>

### <span data-ttu-id="49663-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="49663-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="49663-143">출력</span><span class="sxs-lookup"><span data-stu-id="49663-143">OUTPUTS</span></span>

### <span data-ttu-id="49663-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="49663-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="49663-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49663-145">NOTES</span></span>

<span data-ttu-id="49663-146">별칭</span><span class="sxs-lookup"><span data-stu-id="49663-146">ALIASES</span></span>

<span data-ttu-id="49663-147">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="49663-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49663-148">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="49663-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49663-149">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49663-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49663-150">INPUTOBJECT <IBlockchainIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="49663-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49663-151">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="49663-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="49663-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49663-153">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="49663-154">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="49663-155">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="49663-156">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49663-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="49663-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49663-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="49663-158">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="49663-159">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49663-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="49663-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49663-160">RELATED LINKS</span></span>

