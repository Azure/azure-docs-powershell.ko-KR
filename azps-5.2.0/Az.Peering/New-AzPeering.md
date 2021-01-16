---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354314"
---
# <span data-ttu-id="9cad1-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="9cad1-101">New-AzPeering</span></span>

## <span data-ttu-id="9cad1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cad1-102">SYNOPSIS</span></span>
<span data-ttu-id="9cad1-103">새 피어링 리소스 ARM 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="9cad1-104">구문</span><span class="sxs-lookup"><span data-stu-id="9cad1-104">SYNTAX</span></span>

### <span data-ttu-id="9cad1-105">Exchange(기본값)</span><span class="sxs-lookup"><span data-stu-id="9cad1-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cad1-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="9cad1-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cad1-107">직접</span><span class="sxs-lookup"><span data-stu-id="9cad1-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cad1-108">설명</span><span class="sxs-lookup"><span data-stu-id="9cad1-108">DESCRIPTION</span></span>
<span data-ttu-id="9cad1-109">구독에 ARM 피어링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="9cad1-110">연결 개체 만들기에 대한 자세한 내용은 [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) 또는 [New-AzPeeringExchangeConnectionObject를](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9cad1-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="9cad1-111">예제</span><span class="sxs-lookup"><span data-stu-id="9cad1-111">EXAMPLES</span></span>

### <span data-ttu-id="9cad1-112">새 직접 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="9cad1-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="9cad1-113">PeerAsn 65000을 사용하여 시애틀 시설에서 단일 연결로 새 직접 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="9cad1-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="9cad1-114">새 Exchange 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="9cad1-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="9cad1-115">새 Exchange 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="9cad1-115">Create a new exchange peering</span></span>

### <span data-ttu-id="9cad1-116">레거시 피어링을 ARM 피어링으로 변환</span><span class="sxs-lookup"><span data-stu-id="9cad1-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="9cad1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cad1-117">PARAMETERS</span></span>

### <span data-ttu-id="9cad1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cad1-118">-AsJob</span></span>
<span data-ttu-id="9cad1-119">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-119">Run in the background.</span></span>

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

### <span data-ttu-id="9cad1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cad1-120">-DefaultProfile</span></span>
<span data-ttu-id="9cad1-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cad1-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="9cad1-122">-DirectConnection</span></span>
<span data-ttu-id="9cad1-123">다음 명령을 사용하여 새 직접 New-AzExchangePeeringConnection 이 명령에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="9cad1-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="9cad1-124">-ExchangeConnection</span></span>
<span data-ttu-id="9cad1-125">다음 명령을 사용하여 새 Exchange New-AzExchangePeeringConnection 이 명령에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="9cad1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cad1-126">-InputObject</span></span>
<span data-ttu-id="9cad1-127">이 Get-AzLegacyPeering 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="9cad1-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="9cad1-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="9cad1-129">피어링하려는 Microsoft 네트워크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-129">Select the Microsoft network you want to peer with.</span></span>

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

### <span data-ttu-id="9cad1-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9cad1-130">-Name</span></span>
<span data-ttu-id="9cad1-131">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="9cad1-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="9cad1-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="9cad1-133">피어 Asn 리소스 ID입니다. Get-AzPeerAsn 사용하여 ID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="9cad1-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="9cad1-134">-PeeringLocation</span></span>
<span data-ttu-id="9cad1-135">Azure 지역과 다른 물리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="9cad1-136">Get-AzPeeringLocation \<kind\> -Kind를 사용하여 도시 이름을 키로 사용</span><span class="sxs-lookup"><span data-stu-id="9cad1-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="9cad1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cad1-137">-ResourceGroupName</span></span>
<span data-ttu-id="9cad1-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-138">The resource group name.</span></span>

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

### <span data-ttu-id="9cad1-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="9cad1-139">-Sku</span></span>
<span data-ttu-id="9cad1-140">다른 Basic_Direct_Free 명시적으로 지정하지 Premium_Direct_Free 경우 또는 선택을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="9cad1-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cad1-141">-Tag</span></span>
<span data-ttu-id="9cad1-142">Microsoft 피어링 서비스에 연결하기 위해 사용할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="9cad1-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cad1-143">-Confirm</span></span>
<span data-ttu-id="9cad1-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cad1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cad1-145">-WhatIf</span></span>
<span data-ttu-id="9cad1-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9cad1-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cad1-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cad1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cad1-148">CommonParameters</span></span>
<span data-ttu-id="9cad1-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cad1-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9cad1-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cad1-151">입력</span><span class="sxs-lookup"><span data-stu-id="9cad1-151">INPUTS</span></span>

### <span data-ttu-id="9cad1-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="9cad1-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="9cad1-153">출력</span><span class="sxs-lookup"><span data-stu-id="9cad1-153">OUTPUTS</span></span>

### <span data-ttu-id="9cad1-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="9cad1-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="9cad1-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9cad1-155">NOTES</span></span>

## <span data-ttu-id="9cad1-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cad1-156">RELATED LINKS</span></span>