---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: a63f6c2bc57bfc4d1a82861c6b25bd5c8a6e1383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491819"
---
# <span data-ttu-id="627b9-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="627b9-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="627b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="627b9-102">SYNOPSIS</span></span>
<span data-ttu-id="627b9-103">두 가상 네트워크 간에 피어링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="627b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="627b9-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="627b9-105">설명</span><span class="sxs-lookup"><span data-stu-id="627b9-105">DESCRIPTION</span></span>
<span data-ttu-id="627b9-106">**Add-AzVirtualNetworkPeering** cmdlet은 두 가상 네트워크 간에 피어링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="627b9-107">예제</span><span class="sxs-lookup"><span data-stu-id="627b9-107">EXAMPLES</span></span>

### <span data-ttu-id="627b9-108">예제 1: 동일한 지역에 있는 두 가상 네트워크 간에 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="627b9-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="627b9-109">피어링이 작동하려면 vnet1에서 vnet2로 또는 그 반대로 피어링 링크를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="627b9-110">예제 2: 서로 다른 지역에 있는 두 가상 네트워크 간에 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="627b9-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location canadacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="627b9-111">미국 중서부의 'myVnet1'은 캐나다 중부의 'myVnet2'와 피어링됩니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="627b9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="627b9-112">PARAMETERS</span></span>

### <span data-ttu-id="627b9-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="627b9-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="627b9-114">이 cmdlet이 원격 가상 네트워크의 가상 머신에서 전달된 트래픽을 허용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="627b9-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="627b9-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="627b9-116">이 가상 네트워크에 대한 원격 가상 네트워크의 링크에서 gatewayLinks를 사용할 수 있도록 허용하는 플래그</span><span class="sxs-lookup"><span data-stu-id="627b9-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="627b9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="627b9-117">-AsJob</span></span>
<span data-ttu-id="627b9-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="627b9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="627b9-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="627b9-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="627b9-120">이 cmdlet이 연결된 가상 네트워크 공간의 가상 머신을 차단하여 로컬 가상 네트워크 공간의 모든 가상 머신에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="627b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627b9-121">-DefaultProfile</span></span>
<span data-ttu-id="627b9-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="627b9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="627b9-123">-Name</span></span>
<span data-ttu-id="627b9-124">가상 네트워크 피어링의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b9-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="627b9-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="627b9-126">원격 가상 네트워크의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="627b9-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="627b9-127">-UseRemoteGateways</span></span>
<span data-ttu-id="627b9-128">이 cmdlet이 이 가상 네트워크의 원격 게이트웨이를 허용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="627b9-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="627b9-129">-VirtualNetwork</span></span>
<span data-ttu-id="627b9-130">부모 가상 네트워크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-130">Specifies the parent virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="627b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627b9-131">CommonParameters</span></span>
<span data-ttu-id="627b9-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="627b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627b9-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="627b9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627b9-134">입력</span><span class="sxs-lookup"><span data-stu-id="627b9-134">INPUTS</span></span>

### <span data-ttu-id="627b9-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="627b9-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="627b9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="627b9-136">System.String</span></span>

## <span data-ttu-id="627b9-137">출력</span><span class="sxs-lookup"><span data-stu-id="627b9-137">OUTPUTS</span></span>

### <span data-ttu-id="627b9-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="627b9-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="627b9-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="627b9-139">NOTES</span></span>

## <span data-ttu-id="627b9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="627b9-140">RELATED LINKS</span></span>

[<span data-ttu-id="627b9-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="627b9-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="627b9-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="627b9-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="627b9-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="627b9-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="627b9-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="627b9-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
