---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: bee7857751b9553314085ab3fee4f5edbadce1b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978272"
---
# <span data-ttu-id="b04b1-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b04b1-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b04b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b04b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b04b1-103">가상 네트워크에서 서브넷을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="b04b1-104">구문</span><span class="sxs-lookup"><span data-stu-id="b04b1-104">SYNTAX</span></span>

### <span data-ttu-id="b04b1-105">GetByVirtualNetwork(기본값)</span><span class="sxs-lookup"><span data-stu-id="b04b1-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b04b1-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b04b1-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b04b1-107">설명</span><span class="sxs-lookup"><span data-stu-id="b04b1-107">DESCRIPTION</span></span>
<span data-ttu-id="b04b1-108">**Get-AzVirtualNetworkSubnetConfig** cmdlet은 Azure 가상 네트워크에서 하나 이상의 서브넷 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="b04b1-109">예제</span><span class="sxs-lookup"><span data-stu-id="b04b1-109">EXAMPLES</span></span>

### <span data-ttu-id="b04b1-110">1: 가상 네트워크에서 서브넷을 얻다</span><span class="sxs-lookup"><span data-stu-id="b04b1-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="b04b1-111">이 예제에서는 해당 리소스 그룹에 단일 서브넷이 있는 리소스 그룹과 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="b04b1-112">그런 다음 해당 서브넷에 대한 데이터를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="b04b1-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b04b1-113">PARAMETERS</span></span>

### <span data-ttu-id="b04b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04b1-114">-DefaultProfile</span></span>
<span data-ttu-id="b04b1-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b04b1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b04b1-116">-Name</span></span>
<span data-ttu-id="b04b1-117">이 cmdlet이 얻을 서브넷 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b04b1-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b04b1-118">-ResourceId</span></span>
<span data-ttu-id="b04b1-119">이 cmdlet이 얻을 서브넷의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b04b1-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b04b1-120">-VirtualNetwork</span></span>
<span data-ttu-id="b04b1-121">이 cmdlet에서 얻을 서브넷 구성을 포함하는 **VirtualNetwork** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b04b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04b1-122">CommonParameters</span></span>
<span data-ttu-id="b04b1-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b04b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04b1-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b04b1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04b1-125">입력</span><span class="sxs-lookup"><span data-stu-id="b04b1-125">INPUTS</span></span>

### <span data-ttu-id="b04b1-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b04b1-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="b04b1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b04b1-127">System.String</span></span>

## <span data-ttu-id="b04b1-128">출력</span><span class="sxs-lookup"><span data-stu-id="b04b1-128">OUTPUTS</span></span>

### <span data-ttu-id="b04b1-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b04b1-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b04b1-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b04b1-130">NOTES</span></span>

## <span data-ttu-id="b04b1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b04b1-131">RELATED LINKS</span></span>

[<span data-ttu-id="b04b1-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b04b1-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b04b1-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b04b1-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b04b1-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b04b1-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b04b1-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b04b1-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
