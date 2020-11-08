---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 9bbf7b8540de15f79b93cbb3a7fe90f5ad14ee18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041859"
---
# <span data-ttu-id="bf7a4-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="bf7a4-101">New-AzPeering</span></span>

## <span data-ttu-id="bf7a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="bf7a4-103">새 피어 링 ARM 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="bf7a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf7a4-104">SYNTAX</span></span>

### <span data-ttu-id="bf7a4-105">Exchange (기본값)</span><span class="sxs-lookup"><span data-stu-id="bf7a4-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf7a4-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="bf7a4-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf7a4-107">Dm</span><span class="sxs-lookup"><span data-stu-id="bf7a4-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]> -Sku <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf7a4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bf7a4-108">DESCRIPTION</span></span>
<span data-ttu-id="bf7a4-109">구독에 대 한 ARM 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="bf7a4-110">Connection 개체를 만드는 방법에 대 한 자세한 내용은 [AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) 또는 [AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="bf7a4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bf7a4-111">EXAMPLES</span></span>

### <span data-ttu-id="bf7a4-112">새 직접 피어 링 만들기</span><span class="sxs-lookup"><span data-stu-id="bf7a4-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="bf7a4-113">PeerAsn 65000를 사용 하 여 시애틀 시설에서 단일 연결을 사용 하 여 새 직접 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="bf7a4-114">새 Exchange 피어 링 만들기</span><span class="sxs-lookup"><span data-stu-id="bf7a4-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="bf7a4-115">새 exchange 피어 링 만들기</span><span class="sxs-lookup"><span data-stu-id="bf7a4-115">Create a new exchange peering</span></span>

### <span data-ttu-id="bf7a4-116">레거시 피어 링을 ARM 피어 링으로 변환</span><span class="sxs-lookup"><span data-stu-id="bf7a4-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="bf7a4-117">변수</span><span class="sxs-lookup"><span data-stu-id="bf7a4-117">PARAMETERS</span></span>

### <span data-ttu-id="bf7a4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf7a4-118">-AsJob</span></span>
<span data-ttu-id="bf7a4-119">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-119">Run in the background.</span></span>

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

### <span data-ttu-id="bf7a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf7a4-120">-DefaultProfile</span></span>
<span data-ttu-id="bf7a4-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="bf7a4-122">-DirectConnection</span></span>
<span data-ttu-id="bf7a4-123">New-AzExchangePeeringConnection 및 파이프를 사용 하 여이 명령에 대 한 새 직접 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="bf7a4-124">-ExchangeConnection</span></span>
<span data-ttu-id="bf7a4-125">New-AzExchangePeeringConnection를 사용 하 여 새 Exchange 연결을 만들고이 명령에 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf7a4-126">-InputObject</span></span>
<span data-ttu-id="bf7a4-127">이 개체를 검색 하려면 Get-AzLegacyPeering를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-128">-이름</span><span class="sxs-lookup"><span data-stu-id="bf7a4-128">-Name</span></span>
<span data-ttu-id="bf7a4-129">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-129">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-130">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="bf7a4-130">-PeerAsnResourceId</span></span>
<span data-ttu-id="bf7a4-131">피어 Asn 리소스 Id입니다. Get-AzPeerAsn를 사용 하 여 Id를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-131">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-132">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="bf7a4-132">-PeeringLocation</span></span>
<span data-ttu-id="bf7a4-133">Azure 지역과는 다른 실제 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-133">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="bf7a4-134">Get-AzPeeringLocation Kind \< \> 는 도시 이름을 키로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-134">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf7a4-135">-ResourceGroupName</span></span>
<span data-ttu-id="bf7a4-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="bf7a4-137">-Sku</span></span>
<span data-ttu-id="bf7a4-138">다른 옵션을 명시적으로 선택 하지 않는 한 Basic_Direct_Free 또는 Premium_Direct_Free를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-138">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-139">태그</span><span class="sxs-lookup"><span data-stu-id="bf7a4-139">-Tag</span></span>
<span data-ttu-id="bf7a4-140">Microsoft 피어 링 서비스와 연결할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-140">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a4-141">-확인</span><span class="sxs-lookup"><span data-stu-id="bf7a4-141">-Confirm</span></span>
<span data-ttu-id="bf7a4-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf7a4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf7a4-143">-WhatIf</span></span>
<span data-ttu-id="bf7a4-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf7a4-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf7a4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf7a4-146">CommonParameters</span></span>
<span data-ttu-id="bf7a4-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf7a4-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf7a4-149">입력</span><span class="sxs-lookup"><span data-stu-id="bf7a4-149">INPUTS</span></span>

### <span data-ttu-id="bf7a4-150">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-150">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="bf7a4-151">출력</span><span class="sxs-lookup"><span data-stu-id="bf7a4-151">OUTPUTS</span></span>

### <span data-ttu-id="bf7a4-152">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf7a4-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="bf7a4-153">상속자</span><span class="sxs-lookup"><span data-stu-id="bf7a4-153">NOTES</span></span>

## <span data-ttu-id="bf7a4-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf7a4-154">RELATED LINKS</span></span>
