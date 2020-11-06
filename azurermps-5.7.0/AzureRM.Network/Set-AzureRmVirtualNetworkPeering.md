---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a8af220313d0e6bbd03d35aa60d235651b19704c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528900"
---
# <span data-ttu-id="53698-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="53698-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="53698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53698-102">SYNOPSIS</span></span>
<span data-ttu-id="53698-103">가상 네트워크 피어 링을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53698-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53698-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53698-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53698-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53698-105">DESCRIPTION</span></span>
<span data-ttu-id="53698-106">**AzureRmVirtualNetworkPeering** cmdlet은 가상 네트워크 피어 링을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53698-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="53698-107">예제의</span><span class="sxs-lookup"><span data-stu-id="53698-107">EXAMPLES</span></span>

### <span data-ttu-id="53698-108">예제 1: 가상 네트워크 피어 링의 전달 된 트래픽 구성 변경</span><span class="sxs-lookup"><span data-stu-id="53698-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="53698-109">예제 2: 가상 네트워크 피어 링의 가상 네트워크 액세스 변경</span><span class="sxs-lookup"><span data-stu-id="53698-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="53698-110">예제 3: 가상 네트워크 피어 링의 게이트웨이 전송 속성 구성 변경</span><span class="sxs-lookup"><span data-stu-id="53698-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="53698-111">예제 4: 가상 네트워크 피어 링에서 원격 게이트웨이 사용</span><span class="sxs-lookup"><span data-stu-id="53698-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="53698-112">이 속성을 $True로 변경 하면 피어의 VNet 게이트웨이를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53698-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="53698-113">그러나 피어 VNet에는 게이트웨이가 구성 되어 있어야 하 고 **Allow게이트웨이 전송** 에는 $True 값이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53698-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="53698-114">게이트웨이가 이미 구성 된 경우에는이 속성을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="53698-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="53698-115">변수</span><span class="sxs-lookup"><span data-stu-id="53698-115">PARAMETERS</span></span>

### <span data-ttu-id="53698-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53698-116">-AsJob</span></span>
<span data-ttu-id="53698-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="53698-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53698-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53698-118">-DefaultProfile</span></span>
<span data-ttu-id="53698-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53698-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53698-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="53698-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="53698-121">가상 네트워크 피어 링을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53698-121">Specifies the virtual network peering.</span></span>

```yaml
Type: PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53698-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53698-122">CommonParameters</span></span>
<span data-ttu-id="53698-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53698-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53698-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53698-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53698-125">입력</span><span class="sxs-lookup"><span data-stu-id="53698-125">INPUTS</span></span>

### <span data-ttu-id="53698-126">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="53698-126">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="53698-127">' VirtualNetworkPeering ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkPeering ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53698-127">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="53698-128">출력</span><span class="sxs-lookup"><span data-stu-id="53698-128">OUTPUTS</span></span>

### <span data-ttu-id="53698-129">PSVirtualNetworkPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="53698-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="53698-130">상속자</span><span class="sxs-lookup"><span data-stu-id="53698-130">NOTES</span></span>

## <span data-ttu-id="53698-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53698-131">RELATED LINKS</span></span>

[<span data-ttu-id="53698-132">추가-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="53698-132">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="53698-133">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="53698-133">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="53698-134">제거-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="53698-134">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


