---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 4ab32ab5830356740cdb1709799b7dcb8f811c90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529254"
---
# <span data-ttu-id="3e646-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="3e646-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="3e646-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e646-102">SYNOPSIS</span></span>
<span data-ttu-id="3e646-103">가상 네트워크 게이트웨이의 기본 사이트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e646-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e646-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e646-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3e646-105">DESCRIPTION</span></span>
<span data-ttu-id="3e646-106">**AzureRmVirtualNetworkGatewayDefaultSite** cmdlet은 강제 터널링 기본 사이트를 가상 네트워크 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="3e646-107">강제 터널링은 Azure 가상 컴퓨터에서 온-프레미스 네트워크로 인터넷에 바인딩된 트래픽을 리디렉션할 수 있는 방법을 제공 합니다. 이렇게 하면 트래픽을 해제 하기 전에 검사 하 고 감사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="3e646-108">강제 터널링은 VPN (가상 사설망) 터널을 사용 하 여 수행 됩니다. 이 터널에는 모든 Azure 인터넷 바인딩 트래픽이 리디렉션되는 기본 사이트 (로컬 게이트웨이)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="3e646-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** 는 게이트웨이에 할당 된 기본 사이트를 변경 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="3e646-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3e646-110">EXAMPLES</span></span>

### <span data-ttu-id="3e646-111">예제 1: 가상 네트워크 게이트웨이에 기본 사이트 할당</span><span class="sxs-lookup"><span data-stu-id="3e646-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="3e646-112">이 예제에서는 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이에 기본 사이트를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="3e646-113">첫 번째 명령은 ContosoLocalGateway 라는 로컬 게이트웨이에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="3e646-114">$LocalGateway 라는 변수에 저장 된이 개체 참조는 기본 사이트로 구성 될 게이트웨이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="3e646-115">.</span><span class="sxs-lookup"><span data-stu-id="3e646-115">.</span></span>
<span data-ttu-id="3e646-116">그런 다음 두 번째 명령은 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들고 결과를 $VirtualGateway 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="3e646-117">세 번째 명령은 **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet을 사용 하 여 기본 사이트를 ContosoVirtualGateway에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-117">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="3e646-118">변수</span><span class="sxs-lookup"><span data-stu-id="3e646-118">PARAMETERS</span></span>

### <span data-ttu-id="3e646-119">-게이트웨이 Defaultsite</span><span class="sxs-lookup"><span data-stu-id="3e646-119">-GatewayDefaultSite</span></span>
<span data-ttu-id="3e646-120">지정 된 가상 네트워크의 기본 사이트로 할당할 로컬 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-120">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="3e646-121">Get-AzureRmLocalNetworkGateway cmdlet을 사용 하 여 로컬 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-121">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="3e646-122">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3e646-122">-VirtualNetworkGateway</span></span>
<span data-ttu-id="3e646-123">기본 사이트가 할당 될 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-123">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="3e646-124">**AzureRmVirtualNetworkGateway** 를 사용 하 고 게이트웨이 이름을 지정 하 여 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-124">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="3e646-125">변수 $VirtualGateway는 *VirtualNetworkGateway* 매개 변수에 대 한 매개 변수 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-125">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="3e646-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e646-126">-DefaultProfile</span></span>
<span data-ttu-id="3e646-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e646-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e646-128">CommonParameters</span></span>
<span data-ttu-id="3e646-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e646-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e646-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e646-131">입력</span><span class="sxs-lookup"><span data-stu-id="3e646-131">INPUTS</span></span>

###  
<span data-ttu-id="3e646-132">이 cmdlet은 **PSVirtualNetworkGateway** 개체의 파이프라인 인스턴스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="3e646-133">출력</span><span class="sxs-lookup"><span data-stu-id="3e646-133">OUTPUTS</span></span>

###  
<span data-ttu-id="3e646-134">이 cmdlet은 **PSVirtualNetworkGateway** 개체의 기존 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e646-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="3e646-135">상속자</span><span class="sxs-lookup"><span data-stu-id="3e646-135">NOTES</span></span>

## <span data-ttu-id="3e646-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e646-136">RELATED LINKS</span></span>

[<span data-ttu-id="3e646-137">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3e646-137">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="3e646-138">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3e646-138">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3e646-139">제거-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="3e646-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


