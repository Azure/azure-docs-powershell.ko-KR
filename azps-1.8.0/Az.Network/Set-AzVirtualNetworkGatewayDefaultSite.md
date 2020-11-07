---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 10cc9686b89dd690234b819c86352141ed1d93e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699956"
---
# <span data-ttu-id="b9fa6-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b9fa6-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="b9fa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fa6-103">가상 네트워크 게이트웨이의 기본 사이트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="b9fa6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9fa6-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9fa6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b9fa6-105">DESCRIPTION</span></span>
<span data-ttu-id="b9fa6-106">**AzVirtualNetworkGatewayDefaultSite** cmdlet은 강제 터널링 기본 사이트를 가상 네트워크 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="b9fa6-107">강제 터널링은 Azure 가상 컴퓨터에서 온-프레미스 네트워크로 인터넷에 바인딩된 트래픽을 리디렉션할 수 있는 방법을 제공 합니다. 이렇게 하면 트래픽을 해제 하기 전에 검사 하 고 감사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="b9fa6-108">강제 터널링은 VPN (가상 사설망) 터널을 사용 하 여 수행 됩니다. 이 터널에는 모든 Azure 인터넷 바인딩 트래픽이 리디렉션되는 기본 사이트 (로컬 게이트웨이)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="b9fa6-109">**Set-AzVirtualNetworkGatewayDefaultSite** 는 게이트웨이에 할당 된 기본 사이트를 변경 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="b9fa6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b9fa6-110">EXAMPLES</span></span>

### <span data-ttu-id="b9fa6-111">예제 1: 가상 네트워크 게이트웨이에 기본 사이트 할당</span><span class="sxs-lookup"><span data-stu-id="b9fa6-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="b9fa6-112">이 예제에서는 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이에 기본 사이트를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="b9fa6-113">첫 번째 명령은 ContosoLocalGateway 라는 로컬 게이트웨이에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="b9fa6-114">$LocalGateway 라는 변수에 저장 된이 개체 참조는 기본 사이트로 구성 될 게이트웨이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="b9fa6-115">그런 다음 두 번째 명령은 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들고 결과를 $VirtualGateway 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="b9fa6-116">세 번째 명령은 **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet을 사용 하 여 기본 사이트를 ContosoVirtualGateway에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="b9fa6-117">변수</span><span class="sxs-lookup"><span data-stu-id="b9fa6-117">PARAMETERS</span></span>

### <span data-ttu-id="b9fa6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fa6-118">-DefaultProfile</span></span>
<span data-ttu-id="b9fa6-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9fa6-120">-게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="b9fa6-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="b9fa6-121">지정 된 가상 네트워크의 기본 사이트로 할당할 로컬 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="b9fa6-122">Get-AzLocalNetworkGateway cmdlet을 사용 하 여 로컬 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9fa6-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9fa6-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b9fa6-124">기본 사이트가 할당 될 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="b9fa6-125">**AzVirtualNetworkGateway** 를 사용 하 고 게이트웨이 이름을 지정 하 여 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="b9fa6-126">변수 $VirtualGateway는 *VirtualNetworkGateway* 매개 변수에 대 한 매개 변수 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="b9fa6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fa6-127">CommonParameters</span></span>
<span data-ttu-id="b9fa6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fa6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9fa6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fa6-130">입력</span><span class="sxs-lookup"><span data-stu-id="b9fa6-130">INPUTS</span></span>

### <span data-ttu-id="b9fa6-131">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b9fa6-132">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9fa6-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="b9fa6-133">출력</span><span class="sxs-lookup"><span data-stu-id="b9fa6-133">OUTPUTS</span></span>

### <span data-ttu-id="b9fa6-134">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b9fa6-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b9fa6-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b9fa6-135">NOTES</span></span>

## <span data-ttu-id="b9fa6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9fa6-136">RELATED LINKS</span></span>

[<span data-ttu-id="b9fa6-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9fa6-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="b9fa6-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b9fa6-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b9fa6-139">제거-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b9fa6-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


