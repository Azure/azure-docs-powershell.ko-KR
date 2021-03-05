---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: d8ef4378ed0032012a64d015855ca0287d608a6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989445"
---
# <span data-ttu-id="2fd31-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="2fd31-101">New-AzPeering</span></span>

## <span data-ttu-id="2fd31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fd31-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd31-103">새 피어링 ARM 리소스 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="2fd31-104">구문</span><span class="sxs-lookup"><span data-stu-id="2fd31-104">SYNTAX</span></span>

### <span data-ttu-id="2fd31-105">Exchange(기본값)</span><span class="sxs-lookup"><span data-stu-id="2fd31-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fd31-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="2fd31-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fd31-107">직접</span><span class="sxs-lookup"><span data-stu-id="2fd31-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fd31-108">설명</span><span class="sxs-lookup"><span data-stu-id="2fd31-108">DESCRIPTION</span></span>
<span data-ttu-id="2fd31-109">구독에 ARM 피어링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="2fd31-110">연결 개체 만들기에 대한 자세한 내용은 [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) 또는 [New-AzPeeringExchangeConnectionObject를](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2fd31-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="2fd31-111">예제</span><span class="sxs-lookup"><span data-stu-id="2fd31-111">EXAMPLES</span></span>

### <span data-ttu-id="2fd31-112">새 직접 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="2fd31-112">Create New Direct Peering</span></span>
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

<span data-ttu-id="2fd31-113">PeerAsn 65000을 사용하여 시애틀 시설에서 단일 연결로 새 Direct 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="2fd31-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="2fd31-114">새 Exchange 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="2fd31-114">Create New Exchange Peering</span></span>
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

<span data-ttu-id="2fd31-115">새 Exchange 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="2fd31-115">Create a new exchange peering</span></span>

### <span data-ttu-id="2fd31-116">레거시 피어링을 ARM 피어링으로 변환</span><span class="sxs-lookup"><span data-stu-id="2fd31-116">Convert Legacy Peering to ARM Peering</span></span>
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

## <span data-ttu-id="2fd31-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2fd31-117">PARAMETERS</span></span>

### <span data-ttu-id="2fd31-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fd31-118">-AsJob</span></span>
<span data-ttu-id="2fd31-119">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-119">Run in the background.</span></span>

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

### <span data-ttu-id="2fd31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd31-120">-DefaultProfile</span></span>
<span data-ttu-id="2fd31-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fd31-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="2fd31-122">-DirectConnection</span></span>
<span data-ttu-id="2fd31-123">이 명령에 대한 New-AzExchangePeeringConnection 파이프를 사용하여 새 직접 연결을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="2fd31-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="2fd31-124">-ExchangeConnection</span></span>
<span data-ttu-id="2fd31-125">이 명령에 대한 New-AzExchangePeeringConnection 새 Exchange 연결을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

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

### <span data-ttu-id="2fd31-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fd31-126">-InputObject</span></span>
<span data-ttu-id="2fd31-127">이 Get-AzLegacyPeering 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

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

### <span data-ttu-id="2fd31-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="2fd31-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="2fd31-129">피어링할 Microsoft 네트워크를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-129">Select the Microsoft network you want to peer with.</span></span>

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

### <span data-ttu-id="2fd31-130">-Name</span><span class="sxs-lookup"><span data-stu-id="2fd31-130">-Name</span></span>
<span data-ttu-id="2fd31-131">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2fd31-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="2fd31-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="2fd31-133">피어 Asn 리소스 ID. Get-AzPeerAsn ID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="2fd31-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="2fd31-134">-PeeringLocation</span></span>
<span data-ttu-id="2fd31-135">Azure 지역과 다른 물리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="2fd31-136">Get-AzPeeringLocation \<kind\> -Kind를 키로 사용하여 도시 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

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

### <span data-ttu-id="2fd31-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd31-137">-ResourceGroupName</span></span>
<span data-ttu-id="2fd31-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-138">The resource group name.</span></span>

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

### <span data-ttu-id="2fd31-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="2fd31-139">-Sku</span></span>
<span data-ttu-id="2fd31-140">명시적으로 Basic_Direct_Free 선택해야 Premium_Direct_Free 선택하거나 선택을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

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

### <span data-ttu-id="2fd31-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fd31-141">-Tag</span></span>
<span data-ttu-id="2fd31-142">Microsoft 피어링 서비스에 연결되는 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-142">The tags to associate with the Microsoft Peering Service.</span></span>

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

### <span data-ttu-id="2fd31-143">-확인</span><span class="sxs-lookup"><span data-stu-id="2fd31-143">-Confirm</span></span>
<span data-ttu-id="2fd31-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd31-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd31-145">-WhatIf</span></span>
<span data-ttu-id="2fd31-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fd31-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd31-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd31-148">CommonParameters</span></span>
<span data-ttu-id="2fd31-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2fd31-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd31-150">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fd31-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd31-151">입력</span><span class="sxs-lookup"><span data-stu-id="2fd31-151">INPUTS</span></span>

### <span data-ttu-id="2fd31-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2fd31-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="2fd31-153">출력</span><span class="sxs-lookup"><span data-stu-id="2fd31-153">OUTPUTS</span></span>

### <span data-ttu-id="2fd31-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="2fd31-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="2fd31-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2fd31-155">NOTES</span></span>

## <span data-ttu-id="2fd31-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fd31-156">RELATED LINKS</span></span>
