---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360753"
---
# <span data-ttu-id="fe15e-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fe15e-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="fe15e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe15e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe15e-103">기존 ExpressRoute 구성 권한 부여를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="fe15e-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe15e-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe15e-105">설명</span><span class="sxs-lookup"><span data-stu-id="fe15e-105">DESCRIPTION</span></span>
<span data-ttu-id="fe15e-106">**Remove-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 할당된 권한 부여를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="fe15e-107">ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Azure에 Azure에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="fe15e-108">ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 자신의 네트워크를 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="fe15e-109">가상 네트워크당 하나의 권한 부여만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="fe15e-110">그러나 회로 소유자는 **제거-AzExpressRouteCircuitAuthorization을** 사용하여 가상 네트워크에 할당된 권한 부여를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="fe15e-111">이 경우 해당 가상 네트워크는 더 이상 ExpressRoute 회로를 사용하여 Azure에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="fe15e-112">예제</span><span class="sxs-lookup"><span data-stu-id="fe15e-112">EXAMPLES</span></span>

### <span data-ttu-id="fe15e-113">예제 1: ExpressRoute 회로에서 회로 권한 부여 제거</span><span class="sxs-lookup"><span data-stu-id="fe15e-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="fe15e-114">이 예제에서는 ExpressRoute 회로에서 회로 권한 부여를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="fe15e-115">첫 번째 명령은 **Get-AzExpressRouteCircuit** cmdlet을 사용하여 ContosoCircuit이라는 ExpressRoute 회로에 대한 개체 참조를 만들고 결과를 이름 지정 변수에 $Circuit.</span><span class="sxs-lookup"><span data-stu-id="fe15e-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="fe15e-116">두 번째 명령은 제거를 위해 회로 권한 부여 ContosoCircuitAuthorization을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="fe15e-117">세 번째 명령은 Set-AzExpressRouteCircuit cmdlet을 사용하여 $Circuit 변수에 저장된 ExpressRoute 회로의 제거를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="fe15e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe15e-118">PARAMETERS</span></span>

### <span data-ttu-id="fe15e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe15e-119">-DefaultProfile</span></span>
<span data-ttu-id="fe15e-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe15e-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe15e-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="fe15e-122">이 cmdlet에서 제거하는 ExpressRouteCircuit 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe15e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fe15e-123">-Name</span></span>
<span data-ttu-id="fe15e-124">이 cmdlet이 제거하는 회로 권한 부여의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe15e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe15e-125">CommonParameters</span></span>
<span data-ttu-id="fe15e-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe15e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe15e-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fe15e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe15e-128">입력</span><span class="sxs-lookup"><span data-stu-id="fe15e-128">INPUTS</span></span>

### <span data-ttu-id="fe15e-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe15e-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fe15e-130">출력</span><span class="sxs-lookup"><span data-stu-id="fe15e-130">OUTPUTS</span></span>

### <span data-ttu-id="fe15e-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe15e-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fe15e-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe15e-132">NOTES</span></span>

## <span data-ttu-id="fe15e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe15e-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe15e-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fe15e-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="fe15e-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe15e-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="fe15e-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fe15e-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="fe15e-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="fe15e-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="fe15e-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe15e-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
