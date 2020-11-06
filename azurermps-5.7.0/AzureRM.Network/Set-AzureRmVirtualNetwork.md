---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 22ea0a6a28a24503413fa9b8958002616c03b884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528011"
---
# <span data-ttu-id="b10ed-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b10ed-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="b10ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b10ed-102">SYNOPSIS</span></span>
<span data-ttu-id="b10ed-103">가상 네트워크의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b10ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b10ed-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b10ed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b10ed-105">DESCRIPTION</span></span>
<span data-ttu-id="b10ed-106">**AzureRmVirtualNetwork** Cmdlet은 Azure 가상 네트워크에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="b10ed-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b10ed-107">EXAMPLES</span></span>

### <span data-ttu-id="b10ed-108">1: 가상 네트워크를 만들고 해당 서브넷 중 하나를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="b10ed-109">이 예제에서는 두 개의 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="b10ed-110">그런 다음 가상 네트워크의 메모리 내 표현에서 하나의 서브넷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="b10ed-111">그런 다음 서비스 쪽에서 수정 된 가상 네트워크 상태를 쓰는 데 Set-AzureRmVirtualNetwork cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="b10ed-112">변수</span><span class="sxs-lookup"><span data-stu-id="b10ed-112">PARAMETERS</span></span>

### <span data-ttu-id="b10ed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b10ed-113">-AsJob</span></span>
<span data-ttu-id="b10ed-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b10ed-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b10ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b10ed-115">-DefaultProfile</span></span>
<span data-ttu-id="b10ed-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b10ed-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b10ed-117">-VirtualNetwork</span></span>
<span data-ttu-id="b10ed-118">목표 상태를 나타내는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="b10ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b10ed-119">CommonParameters</span></span>
<span data-ttu-id="b10ed-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b10ed-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b10ed-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b10ed-122">입력</span><span class="sxs-lookup"><span data-stu-id="b10ed-122">INPUTS</span></span>

### <span data-ttu-id="b10ed-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b10ed-123">PSVirtualNetwork</span></span>
<span data-ttu-id="b10ed-124">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10ed-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="b10ed-125">출력</span><span class="sxs-lookup"><span data-stu-id="b10ed-125">OUTPUTS</span></span>

### <span data-ttu-id="b10ed-126">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b10ed-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b10ed-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b10ed-127">NOTES</span></span>

## <span data-ttu-id="b10ed-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b10ed-128">RELATED LINKS</span></span>

[<span data-ttu-id="b10ed-129">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b10ed-129">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b10ed-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b10ed-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b10ed-131">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b10ed-131">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b10ed-132">제거-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b10ed-132">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


