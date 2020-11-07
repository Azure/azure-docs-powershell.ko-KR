---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876545"
---
# <span data-ttu-id="5cb74-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cb74-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="5cb74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cb74-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb74-103">가상 네트워크의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="5cb74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5cb74-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cb74-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5cb74-105">DESCRIPTION</span></span>
<span data-ttu-id="5cb74-106">**AzVirtualNetwork** Cmdlet은 Azure 가상 네트워크에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="5cb74-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5cb74-107">EXAMPLES</span></span>

### <span data-ttu-id="5cb74-108">1: 가상 네트워크를 만들고 해당 서브넷 중 하나를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="5cb74-109">이 예제에서는 두 개의 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="5cb74-110">그런 다음 가상 네트워크의 메모리 내 표현에서 하나의 서브넷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5cb74-111">그런 다음 서비스 쪽에서 수정 된 가상 네트워크 상태를 쓰는 데 Set-AzVirtualNetwork cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="5cb74-112">변수</span><span class="sxs-lookup"><span data-stu-id="5cb74-112">PARAMETERS</span></span>

### <span data-ttu-id="5cb74-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cb74-113">-AsJob</span></span>
<span data-ttu-id="5cb74-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5cb74-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cb74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb74-115">-DefaultProfile</span></span>
<span data-ttu-id="5cb74-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cb74-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cb74-117">-VirtualNetwork</span></span>
<span data-ttu-id="5cb74-118">목표 상태를 나타내는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="5cb74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb74-119">CommonParameters</span></span>
<span data-ttu-id="5cb74-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb74-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb74-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb74-122">입력</span><span class="sxs-lookup"><span data-stu-id="5cb74-122">INPUTS</span></span>

### <span data-ttu-id="5cb74-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cb74-123">PSVirtualNetwork</span></span>
<span data-ttu-id="5cb74-124">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cb74-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="5cb74-125">출력</span><span class="sxs-lookup"><span data-stu-id="5cb74-125">OUTPUTS</span></span>

### <span data-ttu-id="5cb74-126">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5cb74-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5cb74-127">상속자</span><span class="sxs-lookup"><span data-stu-id="5cb74-127">NOTES</span></span>

## <span data-ttu-id="5cb74-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5cb74-128">RELATED LINKS</span></span>

[<span data-ttu-id="5cb74-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cb74-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="5cb74-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cb74-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="5cb74-131">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cb74-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="5cb74-132">제거-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5cb74-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


