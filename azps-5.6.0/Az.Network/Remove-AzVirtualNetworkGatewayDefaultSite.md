---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: ddf0f6687550e544aa22efbce772c0751a7b810e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006000"
---
# <span data-ttu-id="27072-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="27072-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="27072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27072-102">SYNOPSIS</span></span>
<span data-ttu-id="27072-103">가상 네트워크 게이트웨이에서 기본 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="27072-104">구문</span><span class="sxs-lookup"><span data-stu-id="27072-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27072-105">설명</span><span class="sxs-lookup"><span data-stu-id="27072-105">DESCRIPTION</span></span>
<span data-ttu-id="27072-106">**Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet은 가상 네트워크 게이트웨이에서 강제 터널링 기본 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="27072-107">강제 터널링은 Azure 가상 머신에서 인터넷 바인딩 트래픽을 프레미스 네트워크로 리디렉션하는 방법을 제공합니다. 이렇게 하면 트래픽을 발매하기 전에 트래픽을 검사하고 감사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27072-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="27072-108">강제 터널링은 VPN(가상 사설망) 터널을 사용하여 수행됩니다. 이 터널에는 모든 Azure 인터넷 바인딩 트래픽이 리디렉션되는 로컬 게이트웨이인 기본 사이트가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="27072-109">**Remove-AzVirtualNetworkGatewayDefaultSite는** 게이트웨이에 할당된 기본 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="27072-110">이렇게 하면 게이트웨이를 강제 터널링에 Set-AzVirtualNetworkGatewayDefaultSite 전에 새 기본 사이트를 할당하기 위해 새 사이트를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="27072-111">예제</span><span class="sxs-lookup"><span data-stu-id="27072-111">EXAMPLES</span></span>

### <span data-ttu-id="27072-112">예제 1: 가상 네트워크 게이트웨이에 할당된 기본 사이트 제거</span><span class="sxs-lookup"><span data-stu-id="27072-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="27072-113">이 예제에서는 ContosoVirtualGateway라는 가상 네트워크 게이트웨이에 현재 할당된 기본 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="27072-114">첫 번째 명령은 **Get-AzVirtualNetworkGateway를 사용하여** 게이트웨이에 대한 개체 참조를 만듭니다. 이 개체 참조는 이라는 변수에 $Gateway.</span><span class="sxs-lookup"><span data-stu-id="27072-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="27072-115">그런 다음 두 번째 명령은 **Remove-AzVirtualNetworkGatewayDefaultSite를 사용하여** 해당 게이트웨이에 할당된 기본 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="27072-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27072-116">PARAMETERS</span></span>

### <span data-ttu-id="27072-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27072-117">-DefaultProfile</span></span>
<span data-ttu-id="27072-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27072-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27072-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27072-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="27072-120">제거할 기본 사이트를 포함하는 가상 네트워크 게이트웨이에 대한 개체 참조를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="27072-121">가상 네트워크 게이트웨이에 대한 개체 참조를 Get-AzVirtualNetworkGateway 게이트웨이 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="27072-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27072-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27072-122">CommonParameters</span></span>
<span data-ttu-id="27072-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27072-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27072-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27072-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27072-125">입력</span><span class="sxs-lookup"><span data-stu-id="27072-125">INPUTS</span></span>

### <span data-ttu-id="27072-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27072-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="27072-127">출력</span><span class="sxs-lookup"><span data-stu-id="27072-127">OUTPUTS</span></span>

### <span data-ttu-id="27072-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27072-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="27072-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27072-129">NOTES</span></span>

## <span data-ttu-id="27072-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27072-130">RELATED LINKS</span></span>

[<span data-ttu-id="27072-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="27072-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="27072-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="27072-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


