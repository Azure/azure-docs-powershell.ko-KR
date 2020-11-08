---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217579"
---
# <span data-ttu-id="4adf1-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4adf1-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="4adf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4adf1-102">SYNOPSIS</span></span>
<span data-ttu-id="4adf1-103">가상 네트워크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-103">Updates a virtual network.</span></span>

## <span data-ttu-id="4adf1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4adf1-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4adf1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4adf1-105">DESCRIPTION</span></span>
<span data-ttu-id="4adf1-106">**AzVirtualNetwork** cmdlet은 가상 네트워크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="4adf1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4adf1-107">EXAMPLES</span></span>

### <span data-ttu-id="4adf1-108">1: 가상 네트워크를 만들고 해당 서브넷 중 하나를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="4adf1-109">이 예제에서는 두 개의 서브넷 (frontendSubnet 및 backendSubnet)을 사용 하 여 TestResourceGroup 이라는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="4adf1-110">그런 다음 가상 네트워크의 메모리 내 표현에서 backendSubnet subnet을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4adf1-111">그런 다음 서비스 쪽에서 수정 된 가상 네트워크 상태를 쓰는 데 Set-AzVirtualNetwork cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="4adf1-112">Set-AzVirtualNetwork cmdlet이 실행 되 면 backendSubnet가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="4adf1-113">변수</span><span class="sxs-lookup"><span data-stu-id="4adf1-113">PARAMETERS</span></span>

### <span data-ttu-id="4adf1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4adf1-114">-AsJob</span></span>
<span data-ttu-id="4adf1-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4adf1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4adf1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4adf1-116">-DefaultProfile</span></span>
<span data-ttu-id="4adf1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4adf1-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4adf1-118">-VirtualNetwork</span></span>
<span data-ttu-id="4adf1-119">가상 네트워크를 설정 해야 하는 상태를 나타내는 가상 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="4adf1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4adf1-120">CommonParameters</span></span>
<span data-ttu-id="4adf1-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4adf1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4adf1-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4adf1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4adf1-123">입력</span><span class="sxs-lookup"><span data-stu-id="4adf1-123">INPUTS</span></span>

### <span data-ttu-id="4adf1-124">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4adf1-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4adf1-125">출력</span><span class="sxs-lookup"><span data-stu-id="4adf1-125">OUTPUTS</span></span>

### <span data-ttu-id="4adf1-126">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4adf1-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4adf1-127">상속자</span><span class="sxs-lookup"><span data-stu-id="4adf1-127">NOTES</span></span>

## <span data-ttu-id="4adf1-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4adf1-128">RELATED LINKS</span></span>

[<span data-ttu-id="4adf1-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4adf1-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4adf1-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4adf1-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="4adf1-131">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4adf1-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="4adf1-132">제거-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4adf1-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


