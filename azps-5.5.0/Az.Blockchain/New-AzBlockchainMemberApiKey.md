---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177953"
---
# <span data-ttu-id="9e293-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="9e293-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="9e293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e293-102">SYNOPSIS</span></span>
<span data-ttu-id="9e293-103">블록체인 멤버에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="9e293-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e293-104">SYNTAX</span></span>

### <span data-ttu-id="9e293-105">RegenerateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="9e293-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9e293-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9e293-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9e293-107">설명</span><span class="sxs-lookup"><span data-stu-id="9e293-107">DESCRIPTION</span></span>
<span data-ttu-id="9e293-108">블록체인 멤버에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="9e293-109">예제</span><span class="sxs-lookup"><span data-stu-id="9e293-109">EXAMPLES</span></span>

### <span data-ttu-id="9e293-110">예제 1: 이름을 사용하여 블록체인 멤버에 대한 Api 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="9e293-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="9e293-111">이 명령은 이름, 리소스 그룹을 사용하여 블록체인 멤버에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="9e293-112">예제 2: ID를 사용하여 블록체인 멤버에 대한 API 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="9e293-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="9e293-113">이 명령은 ID를 사용하여 블록체인 멤버에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="9e293-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e293-114">PARAMETERS</span></span>

### <span data-ttu-id="9e293-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="9e293-115">-BlockchainMemberName</span></span>
<span data-ttu-id="9e293-116">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="9e293-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e293-117">-DefaultProfile</span></span>
<span data-ttu-id="9e293-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e293-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e293-119">-InputObject</span></span>
<span data-ttu-id="9e293-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="9e293-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e293-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9e293-121">-KeyName</span></span>
<span data-ttu-id="9e293-122">API 키 이름을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="9e293-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e293-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e293-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9e293-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9e293-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e293-126">-SubscriptionId</span></span>
<span data-ttu-id="9e293-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e293-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9e293-129">-Value</span><span class="sxs-lookup"><span data-stu-id="9e293-129">-Value</span></span>
<span data-ttu-id="9e293-130">API 키 값을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="9e293-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e293-131">-Confirm</span></span>
<span data-ttu-id="9e293-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e293-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e293-133">-WhatIf</span></span>
<span data-ttu-id="9e293-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9e293-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e293-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e293-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e293-136">CommonParameters</span></span>
<span data-ttu-id="9e293-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e293-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e293-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e293-139">입력</span><span class="sxs-lookup"><span data-stu-id="9e293-139">INPUTS</span></span>

### <span data-ttu-id="9e293-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="9e293-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="9e293-141">출력</span><span class="sxs-lookup"><span data-stu-id="9e293-141">OUTPUTS</span></span>

### <span data-ttu-id="9e293-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="9e293-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="9e293-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e293-143">NOTES</span></span>

<span data-ttu-id="9e293-144">별칭</span><span class="sxs-lookup"><span data-stu-id="9e293-144">ALIASES</span></span>

<span data-ttu-id="9e293-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9e293-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e293-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e293-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e293-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e293-148">INPUTOBJECT: <IBlockchainIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9e293-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e293-149">`[BlockchainMemberName <String>]`: 블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="9e293-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="9e293-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e293-151">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="9e293-152">`[OperationId <String>]`: 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="9e293-153">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9e293-154">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9e293-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="9e293-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="9e293-157">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e293-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="9e293-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e293-158">RELATED LINKS</span></span>

