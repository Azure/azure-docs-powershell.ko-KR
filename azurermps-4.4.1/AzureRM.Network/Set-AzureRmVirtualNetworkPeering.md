---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527380"
---
# <span data-ttu-id="91713-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91713-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="91713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91713-102">SYNOPSIS</span></span>
<span data-ttu-id="91713-103">가상 네트워크 피어 링을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="91713-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91713-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91713-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91713-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91713-105">DESCRIPTION</span></span>
<span data-ttu-id="91713-106">**AzureRmVirtualNetworkPeering** cmdlet은 가상 네트워크 피어 링을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="91713-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="91713-107">예제의</span><span class="sxs-lookup"><span data-stu-id="91713-107">EXAMPLES</span></span>

### <span data-ttu-id="91713-108">예제 1: 가상 네트워크 피어 링의 전달 된 트래픽 구성 변경</span><span class="sxs-lookup"><span data-stu-id="91713-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="91713-109">예제 2: 가상 네트워크 피어 링의 가상 네트워크 액세스 변경</span><span class="sxs-lookup"><span data-stu-id="91713-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="91713-110">예제 3: 가상 네트워크 피어 링의 게이트웨이 전송 속성 구성 변경</span><span class="sxs-lookup"><span data-stu-id="91713-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="91713-111">예제 4: 가상 네트워크 피어 링에서 원격 게이트웨이 사용</span><span class="sxs-lookup"><span data-stu-id="91713-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="91713-112">이 속성을 $True로 변경 하면 피어의 VNet 게이트웨이를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91713-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="91713-113">그러나 피어 VNet에는 게이트웨이가 구성 되어 있어야 하 고 **Allow게이트웨이 전송** 에는 $True 값이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91713-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="91713-114">게이트웨이가 이미 구성 된 경우에는이 속성을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="91713-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="91713-115">변수</span><span class="sxs-lookup"><span data-stu-id="91713-115">PARAMETERS</span></span>

### <span data-ttu-id="91713-116">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91713-116">-VirtualNetworkPeering</span></span>
<span data-ttu-id="91713-117">가상 네트워크 피어 링을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91713-117">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91713-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91713-118">-DefaultProfile</span></span>
<span data-ttu-id="91713-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91713-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91713-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91713-120">CommonParameters</span></span>
<span data-ttu-id="91713-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91713-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91713-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91713-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91713-123">입력</span><span class="sxs-lookup"><span data-stu-id="91713-123">INPUTS</span></span>

### <span data-ttu-id="91713-124">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91713-124">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="91713-125">' VirtualNetworkPeering ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkPeering ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="91713-125">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="91713-126">출력</span><span class="sxs-lookup"><span data-stu-id="91713-126">OUTPUTS</span></span>

### <span data-ttu-id="91713-127">PSVirtualNetworkPeering에 대 한.</span><span class="sxs-lookup"><span data-stu-id="91713-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="91713-128">상속자</span><span class="sxs-lookup"><span data-stu-id="91713-128">NOTES</span></span>

## <span data-ttu-id="91713-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91713-129">RELATED LINKS</span></span>

[<span data-ttu-id="91713-130">추가-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91713-130">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="91713-131">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91713-131">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="91713-132">제거-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91713-132">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


