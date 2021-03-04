---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952304"
---
# <span data-ttu-id="313fd-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="313fd-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="313fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="313fd-102">SYNOPSIS</span></span>
<span data-ttu-id="313fd-103">ExpressRoute 회로 권한 부여를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="313fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="313fd-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="313fd-105">설명</span><span class="sxs-lookup"><span data-stu-id="313fd-105">DESCRIPTION</span></span>
<span data-ttu-id="313fd-106">**Add-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 권한 부여를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="313fd-107">ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 프레미스 네트워크를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="313fd-108">ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다(가상 네트워크당 하나의 권한 부여).</span><span class="sxs-lookup"><span data-stu-id="313fd-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="313fd-109">**Add-AzExpressRouteCircuitAuthorization은** 회로에 새 권한 부여를 추가하고 동시에 해당 권한 부여 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="313fd-110">이러한 키는 Get-AzExpressRouteCircuitAuthorization cmdlet을 실행하여 볼 수 있으며, 필요한 경우 해당 네트워크 소유자에게 복사하여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="313fd-111">**Add-AzExpressRouteCircuitAuthorization을** 실행한 후 키를 활성화하려면 Set-AzExpressRouteCircuit cmdlet을 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="313fd-112">**Set-AzExpressRouteCircuit를** 호출하지 않는 경우 권한 부여가 회로에 추가되지만 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="313fd-113">예제</span><span class="sxs-lookup"><span data-stu-id="313fd-113">EXAMPLES</span></span>

### <span data-ttu-id="313fd-114">예제 1: 지정된 ExpressRoute 회로에 권한 부여 추가</span><span class="sxs-lookup"><span data-stu-id="313fd-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="313fd-115">이 예제의 명령은 기존 ExpressRoute 회로에 새 권한 부여를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="313fd-116">첫 번째 명령은 **Get-AzExpressRouteCircuit를** 사용하여 ContosoCircuit라는 회로에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="313fd-117">해당 개체 참조는 이라는 변수에 $Circuit.</span><span class="sxs-lookup"><span data-stu-id="313fd-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="313fd-118">두 번째 명령에서는 **Add-AzExpressRouteCircuitAuthorization** cmdlet을 사용하여 ExpressRoute 회로에 새 권한 부여(ContosoCircuitAuthorization)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="313fd-119">이 명령은 권한 부여를 추가하지만 해당 권한 부여를 활성화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="313fd-120">권한 부여를 활성화하려면 예제의 최종 명령에 표시된 **Set-AzExpressRouteCircuit가** 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="313fd-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="313fd-121">PARAMETERS</span></span>

### <span data-ttu-id="313fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313fd-122">-DefaultProfile</span></span>
<span data-ttu-id="313fd-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="313fd-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="313fd-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="313fd-125">이 cmdlet이 권한 부여를 추가하는 ExpressRoute 회로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="313fd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="313fd-126">-Name</span></span>
<span data-ttu-id="313fd-127">추가할 회로 권한 부여의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="313fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313fd-128">CommonParameters</span></span>
<span data-ttu-id="313fd-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="313fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313fd-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="313fd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313fd-131">입력</span><span class="sxs-lookup"><span data-stu-id="313fd-131">INPUTS</span></span>

### <span data-ttu-id="313fd-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="313fd-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="313fd-133">출력</span><span class="sxs-lookup"><span data-stu-id="313fd-133">OUTPUTS</span></span>

### <span data-ttu-id="313fd-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="313fd-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="313fd-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="313fd-135">NOTES</span></span>

## <span data-ttu-id="313fd-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="313fd-136">RELATED LINKS</span></span>

[<span data-ttu-id="313fd-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="313fd-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="313fd-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="313fd-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="313fd-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="313fd-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="313fd-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="313fd-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="313fd-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="313fd-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
