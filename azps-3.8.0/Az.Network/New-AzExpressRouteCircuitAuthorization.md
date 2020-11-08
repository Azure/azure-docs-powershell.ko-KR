---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044748"
---
# <span data-ttu-id="0ab89-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ab89-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="0ab89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ab89-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab89-103">Express 경로 회로 인증을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="0ab89-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ab89-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ab89-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ab89-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab89-106">**AzExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 추가할 수 있는 회로 인증을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="0ab89-107">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="0ab89-108">Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="0ab89-109">각 가상 네트워크에는 하나의 권한 부여만 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="0ab89-110">Express 경로를 만든 후에 **추가-AzExpressRouteCircuitAuthorization** 를 사용 하 여 해당 회로에 대 한 인증을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="0ab89-111">또는 **새 AzExpressRouteCircuitAuthorization** 를 사용 하 여 회로가 생성 될 때 새 회로에 추가할 수 있는 인증을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="0ab89-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0ab89-112">EXAMPLES</span></span>

### <span data-ttu-id="0ab89-113">예제 1: 새 회로 승인 만들기</span><span class="sxs-lookup"><span data-stu-id="0ab89-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="0ab89-114">이 명령은 ContosoCircuitAuthorization 이라는 새 회로 인증을 만든 다음 해당 개체를 $Authorization 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="0ab89-115">개체를 변수에 저장 하는 것이 중요 합니다. 하지만 **새 AzExpressRouteCircuitAuthorization** 는 회로 인증을 만들 수 있지만, 회로 경로에는 해당 권한을 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="0ab89-116">대신 새 Express 경로를 만들 때 변수 $Authorization를 사용 New-AzExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="0ab89-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="0ab89-117">자세한 내용은 New-AzExpressRouteCircuit cmdlet에 대 한 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ab89-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="0ab89-118">변수</span><span class="sxs-lookup"><span data-stu-id="0ab89-118">PARAMETERS</span></span>

### <span data-ttu-id="0ab89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab89-119">-DefaultProfile</span></span>
<span data-ttu-id="0ab89-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ab89-121">-이름</span><span class="sxs-lookup"><span data-stu-id="0ab89-121">-Name</span></span>
<span data-ttu-id="0ab89-122">새 Express 경로 회로 권한 부여에 대 한 고유한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab89-123">CommonParameters</span></span>
<span data-ttu-id="0ab89-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab89-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab89-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab89-126">입력</span><span class="sxs-lookup"><span data-stu-id="0ab89-126">INPUTS</span></span>

### <span data-ttu-id="0ab89-127">않아야</span><span class="sxs-lookup"><span data-stu-id="0ab89-127">None</span></span>

## <span data-ttu-id="0ab89-128">출력</span><span class="sxs-lookup"><span data-stu-id="0ab89-128">OUTPUTS</span></span>

### <span data-ttu-id="0ab89-129">PSExpressRouteCircuitAuthorization에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0ab89-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="0ab89-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0ab89-130">NOTES</span></span>

## <span data-ttu-id="0ab89-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ab89-131">RELATED LINKS</span></span>

[<span data-ttu-id="0ab89-132">추가-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ab89-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0ab89-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ab89-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="0ab89-134">제거-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="0ab89-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

