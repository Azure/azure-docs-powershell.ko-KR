---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309321"
---
# <span data-ttu-id="2d9bb-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="2d9bb-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="2d9bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d9bb-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9bb-103">Blockchain 구성원에 대 한 API 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="2d9bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d9bb-104">SYNTAX</span></span>

### <span data-ttu-id="2d9bb-105">RegenerateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="2d9bb-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2d9bb-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2d9bb-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d9bb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2d9bb-107">DESCRIPTION</span></span>
<span data-ttu-id="2d9bb-108">Blockchain 구성원에 대 한 API 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="2d9bb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2d9bb-109">EXAMPLES</span></span>

### <span data-ttu-id="2d9bb-110">예제 1: 이름을 사용 하 여 blockchain 구성원에 대해 Api 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="2d9bb-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="2d9bb-111">이 명령은 이름, 리소스 그룹을 사용 하 여 blockchain 구성원에 대 한 Api 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="2d9bb-112">예제 2: idenity를 사용 하 여 blockchain 구성원에 대 한 Api 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="2d9bb-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="2d9bb-113">이 명령은 id를 사용 하 여 blockchain 구성원에 대 한 Api 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="2d9bb-114">변수</span><span class="sxs-lookup"><span data-stu-id="2d9bb-114">PARAMETERS</span></span>

### <span data-ttu-id="2d9bb-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="2d9bb-115">-BlockchainMemberName</span></span>
<span data-ttu-id="2d9bb-116">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="2d9bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9bb-117">-DefaultProfile</span></span>
<span data-ttu-id="2d9bb-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d9bb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d9bb-119">-InputObject</span></span>
<span data-ttu-id="2d9bb-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2d9bb-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2d9bb-121">-KeyName</span></span>
<span data-ttu-id="2d9bb-122">API 키 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="2d9bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d9bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d9bb-124">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2d9bb-125">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2d9bb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d9bb-126">-SubscriptionId</span></span>
<span data-ttu-id="2d9bb-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2d9bb-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2d9bb-129">-값</span><span class="sxs-lookup"><span data-stu-id="2d9bb-129">-Value</span></span>
<span data-ttu-id="2d9bb-130">API 키 값을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="2d9bb-131">-확인</span><span class="sxs-lookup"><span data-stu-id="2d9bb-131">-Confirm</span></span>
<span data-ttu-id="2d9bb-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d9bb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d9bb-133">-WhatIf</span></span>
<span data-ttu-id="2d9bb-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d9bb-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d9bb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9bb-136">CommonParameters</span></span>
<span data-ttu-id="2d9bb-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9bb-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9bb-139">입력</span><span class="sxs-lookup"><span data-stu-id="2d9bb-139">INPUTS</span></span>

### <span data-ttu-id="2d9bb-140">IBlockchainIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="2d9bb-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="2d9bb-141">출력</span><span class="sxs-lookup"><span data-stu-id="2d9bb-141">OUTPUTS</span></span>

### <span data-ttu-id="2d9bb-142">Api20180601Preview. i a PowerShell. i a i. IApiKey</span><span class="sxs-lookup"><span data-stu-id="2d9bb-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="2d9bb-143">상속자</span><span class="sxs-lookup"><span data-stu-id="2d9bb-143">NOTES</span></span>

<span data-ttu-id="2d9bb-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="2d9bb-144">ALIASES</span></span>

<span data-ttu-id="2d9bb-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2d9bb-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2d9bb-146">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2d9bb-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2d9bb-148">INPUTOBJECT <IBlockchainIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2d9bb-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2d9bb-149">`[BlockchainMemberName <String>]`: Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="2d9bb-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="2d9bb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2d9bb-151">`[Location <String>]`: 위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="2d9bb-152">`[OperationId <String>]`: 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="2d9bb-153">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2d9bb-154">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2d9bb-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="2d9bb-156">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="2d9bb-157">`[TransactionNodeName <String>]`: 트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9bb-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="2d9bb-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d9bb-158">RELATED LINKS</span></span>

