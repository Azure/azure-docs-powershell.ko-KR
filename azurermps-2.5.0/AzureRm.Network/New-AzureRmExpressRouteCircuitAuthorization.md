---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881373"
---
# <span data-ttu-id="bb1fb-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fb-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="bb1fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1fb-103">Express 경로 회로 인증을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb1fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb1fb-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb1fb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb1fb-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1fb-106">**AzureRmExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 추가할 수 있는 회로 인증을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="bb1fb-107">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="bb1fb-108">Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="bb1fb-109">각 가상 네트워크에는 하나의 권한 부여만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="bb1fb-110">Express 경로를 만든 후에 **추가-AzureRmExpressRouteCircuitAuthorization** 를 사용 하 여 해당 회로에 대 한 인증을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="bb1fb-111">또는 **새 AzureRmExpressRouteCircuitAuthorization** 를 사용 하 여 회로가 생성 될 때 새 회로에 추가할 수 있는 인증을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="bb1fb-112">예제의</span><span class="sxs-lookup"><span data-stu-id="bb1fb-112">EXAMPLES</span></span>

### <span data-ttu-id="bb1fb-113">예제 1: 새 회로 승인 만들기</span><span class="sxs-lookup"><span data-stu-id="bb1fb-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="bb1fb-114">이 명령은 ContosoCircuitAuthorization 이라는 새 회로 인증을 만든 다음 해당 개체를 $Authorization 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="bb1fb-115">개체를 변수에 저장 하는 것이 중요 합니다. 하지만 **새 AzureRmExpressRouteCircuitAuthorization** 는 회로 인증을 만들 수 있지만, 회로 경로에는 해당 권한을 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="bb1fb-116">대신 새 Express 경로를 만들 때 변수 $Authorization를 사용 New-AzureRmExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="bb1fb-117">자세한 내용은 New-AzureRmExpressRouteCircuit cmdlet에 대 한 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="bb1fb-118">변수</span><span class="sxs-lookup"><span data-stu-id="bb1fb-118">PARAMETERS</span></span>

### <span data-ttu-id="bb1fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1fb-119">-DefaultProfile</span></span>
<span data-ttu-id="bb1fb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb1fb-121">-이름</span><span class="sxs-lookup"><span data-stu-id="bb1fb-121">-Name</span></span>
<span data-ttu-id="bb1fb-122">새 Express 경로 회로 권한 부여에 대 한 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1fb-123">CommonParameters</span></span>
<span data-ttu-id="bb1fb-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1fb-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1fb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1fb-126">입력</span><span class="sxs-lookup"><span data-stu-id="bb1fb-126">INPUTS</span></span>

### <span data-ttu-id="bb1fb-127">않아야</span><span class="sxs-lookup"><span data-stu-id="bb1fb-127">None</span></span>
<span data-ttu-id="bb1fb-128">이 cmdlet은 파이프라인 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="bb1fb-129">출력</span><span class="sxs-lookup"><span data-stu-id="bb1fb-129">OUTPUTS</span></span>

### <span data-ttu-id="bb1fb-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fb-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="bb1fb-131">이 cmdlet은 **PSExpressRouteCircuitAuthorization** 개체의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bb1fb-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="bb1fb-132">상속자</span><span class="sxs-lookup"><span data-stu-id="bb1fb-132">NOTES</span></span>

## <span data-ttu-id="bb1fb-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb1fb-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb1fb-134">추가-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fb-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bb1fb-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fb-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="bb1fb-136">제거-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="bb1fb-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

