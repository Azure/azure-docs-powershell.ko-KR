---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 5a2490e25d42e6285183d1f78182ce0d7c92f02f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532214"
---
# <span data-ttu-id="926cf-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="926cf-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="926cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="926cf-102">SYNOPSIS</span></span>
<span data-ttu-id="926cf-103">가상 네트워크 게이트웨이에서 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="926cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="926cf-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="926cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="926cf-105">DESCRIPTION</span></span>
<span data-ttu-id="926cf-106">**AzureRmVirtualNetworkGatewayDefaultSite** cmdlet은 가상 네트워크 게이트웨이에서 강제 터널링 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="926cf-107">강제 터널링은 Azure 가상 컴퓨터에서 온-프레미스 네트워크로 인터넷에 바인딩된 트래픽을 리디렉션할 수 있는 방법을 제공 합니다. 이렇게 하면 트래픽을 해제 하기 전에 검사 하 고 감사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="926cf-108">강제 터널링은 VPN (가상 사설망) 터널을 사용 하 여 수행 됩니다. 이 터널에는 모든 Azure 인터넷 바인딩 트래픽이 리디렉션되는 기본 사이트 (로컬 게이트웨이)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>

<span data-ttu-id="926cf-109">**제거-AzureRmVirtualNetworkGatewayDefaultSite** 는 게이트웨이에 할당 된 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="926cf-110">이렇게 하는 경우 게이트웨이를 강제 터널링에 사용할 수 있으려면 먼저 Set-AzureRmVirtualNetworkGatewayDefaultSite를 사용 하 여 새 기본 사이트를 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="926cf-111">예제의</span><span class="sxs-lookup"><span data-stu-id="926cf-111">EXAMPLES</span></span>

### <span data-ttu-id="926cf-112">예제 1: 가상 네트워크 게이트웨이에 할당 된 기본 사이트 제거</span><span class="sxs-lookup"><span data-stu-id="926cf-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

<span data-ttu-id="926cf-113">이 예제에서는 ContosoVirtualGateway 라는 가상 네트워크 게이트웨이에 현재 할당 된 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="926cf-114">첫 번째 명령은 **Get-AzureRmVirtualNetworkGateway** 를 사용 하 여 게이트웨이에 대 한 개체 참조를 만듭니다. 이 개체 참조는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="926cf-115">그런 다음 두 번째 명령은 **remove-AzureRmVirtualNetworkGatewayDefaultSite** 를 사용 하 여 해당 게이트웨이에 할당 된 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="926cf-116">변수</span><span class="sxs-lookup"><span data-stu-id="926cf-116">PARAMETERS</span></span>

### <span data-ttu-id="926cf-117">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="926cf-117">-VirtualNetworkGateway</span></span>
<span data-ttu-id="926cf-118">제거할 기본 사이트를 포함 하는 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-118">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="926cf-119">Get-AzureRmVirtualNetworkGateway를 사용 하 고 게이트웨이의 이름을 지정 하 여 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-119">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="926cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926cf-120">-DefaultProfile</span></span>
<span data-ttu-id="926cf-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="926cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926cf-122">CommonParameters</span></span>
<span data-ttu-id="926cf-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926cf-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926cf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926cf-125">입력</span><span class="sxs-lookup"><span data-stu-id="926cf-125">INPUTS</span></span>

###  
<span data-ttu-id="926cf-126">이 cmdlet은 **PSVirtualNetworkGateway** 개체의 파이프라인 인스턴스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-126">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="926cf-127">출력</span><span class="sxs-lookup"><span data-stu-id="926cf-127">OUTPUTS</span></span>

###  
<span data-ttu-id="926cf-128">이 cmdlet은 **PSVirtualNetworkGateway** 개체의 기존 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="926cf-128">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="926cf-129">상속자</span><span class="sxs-lookup"><span data-stu-id="926cf-129">NOTES</span></span>

## <span data-ttu-id="926cf-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="926cf-130">RELATED LINKS</span></span>

[<span data-ttu-id="926cf-131">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="926cf-131">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="926cf-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="926cf-132">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


