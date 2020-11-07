---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875502"
---
# <span data-ttu-id="89a15-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89a15-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="89a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89a15-102">SYNOPSIS</span></span>
<span data-ttu-id="89a15-103">가상 네트워크의 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="89a15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89a15-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89a15-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89a15-105">DESCRIPTION</span></span>
<span data-ttu-id="89a15-106">**AzVirtualNetworkSubnetConfig** Cmdlet은 Azure 가상 네트워크에서 하나 이상의 서브넷 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="89a15-107">예제의</span><span class="sxs-lookup"><span data-stu-id="89a15-107">EXAMPLES</span></span>

### <span data-ttu-id="89a15-108">1: 가상 네트워크에서 서브넷 가져오기</span><span class="sxs-lookup"><span data-stu-id="89a15-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="89a15-109">이 예제에서는 리소스 그룹과 해당 리소스 그룹에 단일 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="89a15-110">그런 다음 해당 서브넷에 대 한 데이터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="89a15-111">변수</span><span class="sxs-lookup"><span data-stu-id="89a15-111">PARAMETERS</span></span>

### <span data-ttu-id="89a15-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a15-112">-DefaultProfile</span></span>
<span data-ttu-id="89a15-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89a15-114">-이름</span><span class="sxs-lookup"><span data-stu-id="89a15-114">-Name</span></span>
<span data-ttu-id="89a15-115">이 cmdlet이 가져오는 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89a15-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="89a15-116">-VirtualNetwork</span></span>
<span data-ttu-id="89a15-117">이 cmdlet이 가져오는 서브넷 구성을 포함 하는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89a15-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a15-118">CommonParameters</span></span>
<span data-ttu-id="89a15-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a15-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a15-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a15-121">입력</span><span class="sxs-lookup"><span data-stu-id="89a15-121">INPUTS</span></span>

### <span data-ttu-id="89a15-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="89a15-122">PSVirtualNetwork</span></span>
<span data-ttu-id="89a15-123">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="89a15-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="89a15-124">출력</span><span class="sxs-lookup"><span data-stu-id="89a15-124">OUTPUTS</span></span>

### <span data-ttu-id="89a15-125">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="89a15-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="89a15-126">상속자</span><span class="sxs-lookup"><span data-stu-id="89a15-126">NOTES</span></span>

## <span data-ttu-id="89a15-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89a15-127">RELATED LINKS</span></span>

[<span data-ttu-id="89a15-128">추가-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89a15-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="89a15-129">새로운 AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89a15-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="89a15-130">제거-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89a15-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="89a15-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="89a15-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


