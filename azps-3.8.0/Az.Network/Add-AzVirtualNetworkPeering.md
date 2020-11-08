---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: a63f6c2bc57bfc4d1a82861c6b25bd5c8a6e1383
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042534"
---
# <span data-ttu-id="6e706-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e706-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="6e706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e706-102">SYNOPSIS</span></span>
<span data-ttu-id="6e706-103">두 가상 네트워크 간에 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="6e706-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e706-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e706-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e706-105">DESCRIPTION</span></span>
<span data-ttu-id="6e706-106">**Add-AzVirtualNetworkPeering** cmdlet은 두 가상 네트워크 간에 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="6e706-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6e706-107">EXAMPLES</span></span>

### <span data-ttu-id="6e706-108">예제 1: 같은 지역에 있는 두 가상 네트워크 간에 피어 링 만들기</span><span class="sxs-lookup"><span data-stu-id="6e706-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="6e706-109">피어 링 연결이 작동 하려면 vnet1에서 vnet2로, 그리고 그 반대의 경우에는 피어 링 링크를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="6e706-110">예제 2: 서로 다른 지역의 두 가상 네트워크 간에 피어 링 만들기</span><span class="sxs-lookup"><span data-stu-id="6e706-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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

<span data-ttu-id="6e706-111">미국 서쪽 중부의 ' myVnet1 '은 캐나다 중부의 ' myVnet2 ' peered.</span><span class="sxs-lookup"><span data-stu-id="6e706-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="6e706-112">변수</span><span class="sxs-lookup"><span data-stu-id="6e706-112">PARAMETERS</span></span>

### <span data-ttu-id="6e706-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="6e706-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="6e706-114">이 cmdlet이 원격 가상 네트워크의 가상 머신에서 전달 된 트래픽을 허용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="6e706-115">-Allow게이트웨이 전송</span><span class="sxs-lookup"><span data-stu-id="6e706-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="6e706-116">원격 가상 네트워크의이 가상 네트워크에 대 한 링크에서 네트워크 연결을 사용할 수 있도록 허용 하는 플래그</span><span class="sxs-lookup"><span data-stu-id="6e706-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="6e706-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e706-117">-AsJob</span></span>
<span data-ttu-id="6e706-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6e706-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e706-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="6e706-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="6e706-120">이 cmdlet이 연결 된 가상 네트워크 공간의 가상 컴퓨터를 차단 하 여 로컬 가상 네트워크 공간의 모든 가상 컴퓨터에 액세스할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="6e706-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e706-121">-DefaultProfile</span></span>
<span data-ttu-id="6e706-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e706-123">-이름</span><span class="sxs-lookup"><span data-stu-id="6e706-123">-Name</span></span>
<span data-ttu-id="6e706-124">가상 네트워크 피어 링의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="6e706-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6e706-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="6e706-126">원격 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-126">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="6e706-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="6e706-127">-UseRemoteGateways</span></span>
<span data-ttu-id="6e706-128">이 cmdlet이이 가상 네트워크에서 원격 게이트웨이를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="6e706-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6e706-129">-VirtualNetwork</span></span>
<span data-ttu-id="6e706-130">부모 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="6e706-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e706-131">CommonParameters</span></span>
<span data-ttu-id="6e706-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e706-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e706-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e706-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e706-134">입력</span><span class="sxs-lookup"><span data-stu-id="6e706-134">INPUTS</span></span>

### <span data-ttu-id="6e706-135">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6e706-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="6e706-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e706-136">System.String</span></span>

## <span data-ttu-id="6e706-137">출력</span><span class="sxs-lookup"><span data-stu-id="6e706-137">OUTPUTS</span></span>

### <span data-ttu-id="6e706-138">PSVirtualNetworkPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6e706-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="6e706-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6e706-139">NOTES</span></span>

## <span data-ttu-id="6e706-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e706-140">RELATED LINKS</span></span>

[<span data-ttu-id="6e706-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6e706-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="6e706-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e706-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="6e706-143">제거-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e706-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="6e706-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6e706-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
