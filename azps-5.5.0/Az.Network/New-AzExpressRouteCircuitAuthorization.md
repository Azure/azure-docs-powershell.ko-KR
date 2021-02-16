---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189692"
---
# <span data-ttu-id="c9d81-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c9d81-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="c9d81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9d81-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d81-103">ExpressRoute 회로 권한 부여를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="c9d81-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9d81-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9d81-105">설명</span><span class="sxs-lookup"><span data-stu-id="c9d81-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d81-106">**New-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 추가할 수 있는 회로 권한 부여를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="c9d81-107">ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="c9d81-108">ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="c9d81-109">가상 네트워크당 하나의 권한 부여만 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="c9d81-110">ExpressRoute 회로를 만든 후 **Add-AzExpressRouteCircuitAuthorization을** 사용하여 해당 회로에 권한 부여를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="c9d81-111">또는 **New-AzExpressRouteCircuitAuthorization을** 사용하여 회로를 만드는 동시에 새 회로에 추가할 수 있는 권한 부여를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="c9d81-112">예제</span><span class="sxs-lookup"><span data-stu-id="c9d81-112">EXAMPLES</span></span>

### <span data-ttu-id="c9d81-113">예제 1: 새 회로 권한 부여 만들기</span><span class="sxs-lookup"><span data-stu-id="c9d81-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="c9d81-114">이 명령은 ContosoCircuitAuthorization이라는 새 회로 권한 부여를 만든 다음, 해당 개체를 $Authorization.</span><span class="sxs-lookup"><span data-stu-id="c9d81-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="c9d81-115">개체를 변수에 저장하는 것이 중요합니다. **New-AzExpressRouteCircuitAuthorization이** 회로 권한 부여를 만들 수 있는 경우 회로 경로에 해당 권한 부여를 추가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="c9d81-116">대신 새 ExpressRoute 회로를 $Authorization New-AzExpressRouteCircuit 변수가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="c9d81-117">자세한 내용은 New-AzExpressRouteCircuit cmdlet에 대한 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9d81-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="c9d81-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9d81-118">PARAMETERS</span></span>

### <span data-ttu-id="c9d81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d81-119">-DefaultProfile</span></span>
<span data-ttu-id="c9d81-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d81-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c9d81-121">-Name</span></span>
<span data-ttu-id="c9d81-122">새 ExpressRoute 회로 권한 부여에 대한 고유한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="c9d81-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d81-123">CommonParameters</span></span>
<span data-ttu-id="c9d81-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d81-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d81-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9d81-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d81-126">입력</span><span class="sxs-lookup"><span data-stu-id="c9d81-126">INPUTS</span></span>

### <span data-ttu-id="c9d81-127">없음</span><span class="sxs-lookup"><span data-stu-id="c9d81-127">None</span></span>

## <span data-ttu-id="c9d81-128">출력</span><span class="sxs-lookup"><span data-stu-id="c9d81-128">OUTPUTS</span></span>

### <span data-ttu-id="c9d81-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c9d81-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="c9d81-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9d81-130">NOTES</span></span>

## <span data-ttu-id="c9d81-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9d81-131">RELATED LINKS</span></span>

[<span data-ttu-id="c9d81-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c9d81-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c9d81-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c9d81-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c9d81-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c9d81-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

