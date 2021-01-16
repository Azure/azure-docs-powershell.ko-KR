---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341793"
---
# <span data-ttu-id="14289-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="14289-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="14289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14289-102">SYNOPSIS</span></span>
<span data-ttu-id="14289-103">블록체인 멤버에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="14289-104">구문</span><span class="sxs-lookup"><span data-stu-id="14289-104">SYNTAX</span></span>

### <span data-ttu-id="14289-105">RegenerateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="14289-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14289-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="14289-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14289-107">설명</span><span class="sxs-lookup"><span data-stu-id="14289-107">DESCRIPTION</span></span>
<span data-ttu-id="14289-108">블록체인 멤버에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="14289-109">예제</span><span class="sxs-lookup"><span data-stu-id="14289-109">EXAMPLES</span></span>

### <span data-ttu-id="14289-110">예제 1: 이름을 사용하여 트랜잭션 노드에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="14289-111">이 명령은 이름, 리소스 그룹을 사용하여 트랜잭션 노드에 대한 API 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="14289-112">예제 2: 트랜잭션 노드에 대한 API 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="14289-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="14289-113">이 명령은 ID를 사용하여 트랜잭션 노드에 대한 API 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="14289-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14289-114">PARAMETERS</span></span>

### <span data-ttu-id="14289-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="14289-115">-BlockchainMemberName</span></span>
<span data-ttu-id="14289-116">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="14289-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14289-117">-DefaultProfile</span></span>
<span data-ttu-id="14289-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14289-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14289-119">-InputObject</span></span>
<span data-ttu-id="14289-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="14289-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14289-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="14289-121">-KeyName</span></span>
<span data-ttu-id="14289-122">API 키 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="14289-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14289-123">-ResourceGroupName</span></span>
<span data-ttu-id="14289-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="14289-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14289-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="14289-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14289-126">-SubscriptionId</span></span>
<span data-ttu-id="14289-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14289-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="14289-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="14289-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="14289-129">-TransactionNodeName</span></span>
<span data-ttu-id="14289-130">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-130">Transaction node name.</span></span>

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

### <span data-ttu-id="14289-131">-Value</span><span class="sxs-lookup"><span data-stu-id="14289-131">-Value</span></span>
<span data-ttu-id="14289-132">API 키 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="14289-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14289-133">-Confirm</span></span>
<span data-ttu-id="14289-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="14289-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14289-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14289-135">-WhatIf</span></span>
<span data-ttu-id="14289-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="14289-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14289-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14289-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14289-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14289-138">CommonParameters</span></span>
<span data-ttu-id="14289-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14289-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14289-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14289-141">입력</span><span class="sxs-lookup"><span data-stu-id="14289-141">INPUTS</span></span>

### <span data-ttu-id="14289-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="14289-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="14289-143">출력</span><span class="sxs-lookup"><span data-stu-id="14289-143">OUTPUTS</span></span>

### <span data-ttu-id="14289-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="14289-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="14289-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14289-145">NOTES</span></span>

<span data-ttu-id="14289-146">별칭</span><span class="sxs-lookup"><span data-stu-id="14289-146">ALIASES</span></span>

<span data-ttu-id="14289-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="14289-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14289-148">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="14289-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14289-149">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14289-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14289-150">INPUTOBJECT: <IBlockchainIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="14289-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14289-151">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="14289-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="14289-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14289-153">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="14289-154">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="14289-155">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="14289-156">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14289-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="14289-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="14289-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="14289-158">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="14289-159">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14289-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="14289-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14289-160">RELATED LINKS</span></span>

