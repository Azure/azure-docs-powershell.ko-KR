---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: ceb009dba1984f69e7da3e04a9ae57a9da14c067
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882913"
---
# <span data-ttu-id="009a3-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="009a3-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="009a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="009a3-102">SYNOPSIS</span></span>
<span data-ttu-id="009a3-103">가상 네트워크의 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="009a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="009a3-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="009a3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="009a3-105">DESCRIPTION</span></span>
<span data-ttu-id="009a3-106">**AzureRmVirtualNetworkSubnetConfig** Cmdlet은 Azure 가상 네트워크에서 하나 이상의 서브넷 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="009a3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="009a3-107">EXAMPLES</span></span>

### <span data-ttu-id="009a3-108">1: 가상 네트워크에서 서브넷 가져오기</span><span class="sxs-lookup"><span data-stu-id="009a3-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="009a3-109">이 예제에서는 리소스 그룹과 해당 리소스 그룹에 단일 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="009a3-110">그런 다음 해당 서브넷에 대 한 데이터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="009a3-111">변수</span><span class="sxs-lookup"><span data-stu-id="009a3-111">PARAMETERS</span></span>

### <span data-ttu-id="009a3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="009a3-112">-DefaultProfile</span></span>
<span data-ttu-id="009a3-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="009a3-114">-이름</span><span class="sxs-lookup"><span data-stu-id="009a3-114">-Name</span></span>
<span data-ttu-id="009a3-115">이 cmdlet이 가져오는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="009a3-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="009a3-116">-VirtualNetwork</span></span>
<span data-ttu-id="009a3-117">이 cmdlet이 가져오는 서브넷 구성을 포함 하는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="009a3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="009a3-118">CommonParameters</span></span>
<span data-ttu-id="009a3-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="009a3-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="009a3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="009a3-121">입력</span><span class="sxs-lookup"><span data-stu-id="009a3-121">INPUTS</span></span>

### <span data-ttu-id="009a3-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="009a3-122">PSVirtualNetwork</span></span>
<span data-ttu-id="009a3-123">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="009a3-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="009a3-124">출력</span><span class="sxs-lookup"><span data-stu-id="009a3-124">OUTPUTS</span></span>

### <span data-ttu-id="009a3-125">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="009a3-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="009a3-126">상속자</span><span class="sxs-lookup"><span data-stu-id="009a3-126">NOTES</span></span>

## <span data-ttu-id="009a3-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="009a3-127">RELATED LINKS</span></span>

[<span data-ttu-id="009a3-128">추가-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="009a3-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="009a3-129">새로운 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="009a3-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="009a3-130">제거-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="009a3-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="009a3-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="009a3-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


