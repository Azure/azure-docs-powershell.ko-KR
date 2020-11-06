---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537055"
---
# <span data-ttu-id="086db-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="086db-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="086db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="086db-102">SYNOPSIS</span></span>
<span data-ttu-id="086db-103">가상 네트워크의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086db-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="086db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="086db-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="086db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="086db-105">DESCRIPTION</span></span>
<span data-ttu-id="086db-106">**AzureRmVirtualNetwork** Cmdlet은 Azure 가상 네트워크에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086db-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="086db-107">예제의</span><span class="sxs-lookup"><span data-stu-id="086db-107">EXAMPLES</span></span>

### <span data-ttu-id="086db-108">1: 가상 네트워크를 만들고 해당 서브넷 중 하나를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="086db-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="086db-109">이 예제에서는 두 개의 서브넷이 있는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="086db-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="086db-110">그런 다음 가상 네트워크의 메모리 내 표현에서 하나의 서브넷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="086db-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="086db-111">그런 다음 서비스 쪽에서 수정 된 가상 네트워크 상태를 쓰는 데 Set-AzureRmVirtualNetwork cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="086db-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="086db-112">변수</span><span class="sxs-lookup"><span data-stu-id="086db-112">PARAMETERS</span></span>

### <span data-ttu-id="086db-113">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="086db-113">-VirtualNetwork</span></span>
<span data-ttu-id="086db-114">목표 상태를 나타내는 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="086db-114">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="086db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086db-115">-DefaultProfile</span></span>
<span data-ttu-id="086db-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="086db-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="086db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086db-117">CommonParameters</span></span>
<span data-ttu-id="086db-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="086db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086db-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="086db-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086db-120">입력</span><span class="sxs-lookup"><span data-stu-id="086db-120">INPUTS</span></span>

### <span data-ttu-id="086db-121">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="086db-121">PSVirtualNetwork</span></span>
<span data-ttu-id="086db-122">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="086db-122">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="086db-123">출력</span><span class="sxs-lookup"><span data-stu-id="086db-123">OUTPUTS</span></span>

### <span data-ttu-id="086db-124">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="086db-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="086db-125">상속자</span><span class="sxs-lookup"><span data-stu-id="086db-125">NOTES</span></span>

## <span data-ttu-id="086db-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="086db-126">RELATED LINKS</span></span>

[<span data-ttu-id="086db-127">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="086db-127">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="086db-128">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="086db-128">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="086db-129">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="086db-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="086db-130">제거-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="086db-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


