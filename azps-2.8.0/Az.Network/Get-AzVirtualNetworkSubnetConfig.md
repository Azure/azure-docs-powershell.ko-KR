---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 350b084ee9a7de03e447520dae0cc584bcfacde9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870069"
---
# <span data-ttu-id="5f21a-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f21a-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5f21a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f21a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f21a-103">가상 네트워크의 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="5f21a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f21a-104">SYNTAX</span></span>

### <span data-ttu-id="5f21a-105">GetByVirtualNetwork (기본값)</span><span class="sxs-lookup"><span data-stu-id="5f21a-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f21a-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f21a-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f21a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5f21a-107">DESCRIPTION</span></span>
<span data-ttu-id="5f21a-108">**AzVirtualNetworkSubnetConfig** Cmdlet은 Azure 가상 네트워크에서 하나 이상의 서브넷 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="5f21a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5f21a-109">EXAMPLES</span></span>

### <span data-ttu-id="5f21a-110">1: 가상 네트워크에서 서브넷 가져오기</span><span class="sxs-lookup"><span data-stu-id="5f21a-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="5f21a-111">이 예제에서는 리소스 그룹과 해당 리소스 그룹에 단일 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="5f21a-112">그런 다음 해당 서브넷에 대 한 데이터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="5f21a-113">변수</span><span class="sxs-lookup"><span data-stu-id="5f21a-113">PARAMETERS</span></span>

### <span data-ttu-id="5f21a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f21a-114">-DefaultProfile</span></span>
<span data-ttu-id="5f21a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f21a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="5f21a-116">-Name</span></span>
<span data-ttu-id="5f21a-117">이 cmdlet이 가져오는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f21a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f21a-118">-ResourceId</span></span>
<span data-ttu-id="5f21a-119">이 cmdlet이 가져오는 서브넷의 리소스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f21a-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5f21a-120">-VirtualNetwork</span></span>
<span data-ttu-id="5f21a-121">이 cmdlet이 가져오는 서브넷 구성을 포함 하는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f21a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f21a-122">CommonParameters</span></span>
<span data-ttu-id="5f21a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f21a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f21a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f21a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f21a-125">입력</span><span class="sxs-lookup"><span data-stu-id="5f21a-125">INPUTS</span></span>

### <span data-ttu-id="5f21a-126">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5f21a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="5f21a-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5f21a-127">System.String</span></span>

## <span data-ttu-id="5f21a-128">출력</span><span class="sxs-lookup"><span data-stu-id="5f21a-128">OUTPUTS</span></span>

### <span data-ttu-id="5f21a-129">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5f21a-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5f21a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5f21a-130">NOTES</span></span>

## <span data-ttu-id="5f21a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f21a-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f21a-132">추가-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f21a-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5f21a-133">새로운 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f21a-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5f21a-134">제거-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f21a-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5f21a-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5f21a-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
