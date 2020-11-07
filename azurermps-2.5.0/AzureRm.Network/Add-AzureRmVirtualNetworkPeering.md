---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: 1bf784a94d3f4a03c380f114064fa3f1e399e379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883013"
---
# <span data-ttu-id="744b3-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744b3-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="744b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="744b3-102">SYNOPSIS</span></span>
<span data-ttu-id="744b3-103">두 가상 네트워크 간에 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="744b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="744b3-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="744b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="744b3-105">DESCRIPTION</span></span>
<span data-ttu-id="744b3-106">**Add-AzureRmVirtualNetworkPeering** cmdlet은 두 가상 네트워크 간에 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="744b3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="744b3-107">EXAMPLES</span></span>

### <span data-ttu-id="744b3-108">예제 1: 같은 지역에 있는 두 가상 네트워크 간에 피어 링 만들기</span><span class="sxs-lookup"><span data-stu-id="744b3-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="744b3-109">피어 링 연결이 작동 하려면 vnet1에서 vnet2로, 그리고 그 반대의 경우에는 피어 링 링크를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="744b3-110">예제 2: 서로 다른 지역의 두 가상 네트워크 간에 피어 링 만들기</span><span class="sxs-lookup"><span data-stu-id="744b3-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="744b3-111">미국 서쪽 중부의 ' myVnet1 '은 캐나다 중부의 ' myVnet2 ' peered.</span><span class="sxs-lookup"><span data-stu-id="744b3-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="744b3-112">변수</span><span class="sxs-lookup"><span data-stu-id="744b3-112">PARAMETERS</span></span>

### <span data-ttu-id="744b3-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="744b3-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="744b3-114">이 cmdlet이 원격 가상 네트워크의 가상 머신에서 전달 된 트래픽을 허용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-115">-Allow게이트웨이 전송</span><span class="sxs-lookup"><span data-stu-id="744b3-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="744b3-116">원격 가상 네트워크의이 가상 네트워크에 대 한 링크에서 네트워크 연결을 사용할 수 있도록 허용 하는 플래그</span><span class="sxs-lookup"><span data-stu-id="744b3-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="744b3-117">-AsJob</span></span>
<span data-ttu-id="744b3-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="744b3-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="744b3-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="744b3-120">이 cmdlet이 연결 된 가상 네트워크 공간의 가상 컴퓨터를 차단 하 여 로컬 가상 네트워크 공간의 모든 가상 컴퓨터에 액세스할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744b3-121">-DefaultProfile</span></span>
<span data-ttu-id="744b3-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-123">-이름</span><span class="sxs-lookup"><span data-stu-id="744b3-123">-Name</span></span>
<span data-ttu-id="744b3-124">가상 네트워크 피어 링의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="744b3-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="744b3-126">원격 가상 네트워크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="744b3-127">-UseRemoteGateways</span></span>
<span data-ttu-id="744b3-128">이 cmdlet이이 가상 네트워크에서 원격 게이트웨이를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="744b3-129">-VirtualNetwork</span></span>
<span data-ttu-id="744b3-130">부모 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-130">Specifies the parent virtual network.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="744b3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744b3-131">CommonParameters</span></span>
<span data-ttu-id="744b3-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744b3-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744b3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744b3-134">입력</span><span class="sxs-lookup"><span data-stu-id="744b3-134">INPUTS</span></span>

### <span data-ttu-id="744b3-135">이름</span><span class="sxs-lookup"><span data-stu-id="744b3-135">String</span></span>
<span data-ttu-id="744b3-136">' RemoteVirtualNetworkId ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="744b3-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="744b3-137">PSVirtualNetwork</span></span>
<span data-ttu-id="744b3-138">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="744b3-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="744b3-139">출력</span><span class="sxs-lookup"><span data-stu-id="744b3-139">OUTPUTS</span></span>

### <span data-ttu-id="744b3-140">PSVirtualNetworkPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="744b3-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="744b3-141">상속자</span><span class="sxs-lookup"><span data-stu-id="744b3-141">NOTES</span></span>

## <span data-ttu-id="744b3-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="744b3-142">RELATED LINKS</span></span>

[<span data-ttu-id="744b3-143">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="744b3-143">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="744b3-144">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744b3-144">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="744b3-145">제거-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744b3-145">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="744b3-146">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="744b3-146">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


