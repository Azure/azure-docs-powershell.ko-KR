---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529455"
---
# <span data-ttu-id="fb29e-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb29e-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="fb29e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb29e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb29e-103">가상 네트워크의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb29e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb29e-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb29e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb29e-105">DESCRIPTION</span></span>
<span data-ttu-id="fb29e-106">**AzureRmVirtualNetwork** Cmdlet은 Azure 가상 네트워크에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="fb29e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fb29e-107">EXAMPLES</span></span>

### <span data-ttu-id="fb29e-108">1: 가상 네트워크를 만들고 해당 서브넷 중 하나를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="fb29e-109">이 예제에서는 두 개의 서브넷 (frontendSubnet 및 backendSubnet)을 사용 하 여 TestResourceGroup 이라는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="fb29e-110">그런 다음 가상 네트워크의 메모리 내 표현에서 backendSubnet subnet을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="fb29e-111">그런 다음 서비스 쪽에서 수정 된 가상 네트워크 상태를 쓰는 데 Set-AzureRmVirtualNetwork cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="fb29e-112">Set-AzureRmVirtualNetwork cmdlet이 실행 되 면 backendSubnet가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="fb29e-113">변수</span><span class="sxs-lookup"><span data-stu-id="fb29e-113">PARAMETERS</span></span>

### <span data-ttu-id="fb29e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb29e-114">-AsJob</span></span>
<span data-ttu-id="fb29e-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fb29e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb29e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb29e-116">-DefaultProfile</span></span>
<span data-ttu-id="fb29e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb29e-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb29e-118">-VirtualNetwork</span></span>
<span data-ttu-id="fb29e-119">목표 상태를 나타내는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="fb29e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb29e-120">CommonParameters</span></span>
<span data-ttu-id="fb29e-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb29e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb29e-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb29e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb29e-123">입력</span><span class="sxs-lookup"><span data-stu-id="fb29e-123">INPUTS</span></span>

### <span data-ttu-id="fb29e-124">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fb29e-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="fb29e-125">매개 변수: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fb29e-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="fb29e-126">출력</span><span class="sxs-lookup"><span data-stu-id="fb29e-126">OUTPUTS</span></span>

### <span data-ttu-id="fb29e-127">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fb29e-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="fb29e-128">상속자</span><span class="sxs-lookup"><span data-stu-id="fb29e-128">NOTES</span></span>

## <span data-ttu-id="fb29e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb29e-129">RELATED LINKS</span></span>

[<span data-ttu-id="fb29e-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb29e-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fb29e-131">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb29e-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fb29e-132">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb29e-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="fb29e-133">제거-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb29e-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


