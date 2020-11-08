---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214904"
---
# <span data-ttu-id="9849c-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9849c-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="9849c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9849c-102">SYNOPSIS</span></span>
<span data-ttu-id="9849c-103">Express 경로 회로 인증을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="9849c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9849c-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9849c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9849c-105">DESCRIPTION</span></span>
<span data-ttu-id="9849c-106">**AzExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 인증을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="9849c-107">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="9849c-108">Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다 (가상 네트워크 당 하나의 권한 부여).</span><span class="sxs-lookup"><span data-stu-id="9849c-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="9849c-109">**추가-AzExpressRouteCircuitAuthorization** 는 회로에 새 권한 부여를 추가 하 고 동시에 해당 하는 인증 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="9849c-110">이러한 키는 언제 든 지 Get-AzExpressRouteCircuitAuthorization cmdlet을 실행 하 여 볼 수 있으며 필요한 경우 복사 하 여 적절 한 네트워크 소유자에 게 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="9849c-111">**Add-AzExpressRouteCircuitAuthorization** 을 실행 한 후에는 Set-AzExpressRouteCircuit cmdlet을 호출 하 여 키를 활성화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="9849c-112">**Set-AzExpressRouteCircuit** 를 호출 하지 않으면 권한 부여가 회로에 추가 되지만 사용할 수 있도록 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="9849c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="9849c-113">EXAMPLES</span></span>

### <span data-ttu-id="9849c-114">예제 1: 지정 된 Express 경로 회로에 대 한 권한 부여 추가</span><span class="sxs-lookup"><span data-stu-id="9849c-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="9849c-115">이 예제의 명령은 기존 Express 경로에 새 인증을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="9849c-116">첫 번째 명령은 **AzExpressRouteCircuit** 를 사용 하 여 ContosoCircuit 라는 회로에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="9849c-117">해당 개체 참조는 $Circuit 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="9849c-118">두 번째 명령에서는 **추가-AzExpressRouteCircuitAuthorization** cmdlet을 사용 하 여 새 권한 부여 (ContosoCircuitAuthorization)를 express 회로에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="9849c-119">이 명령은 권한 부여를 추가 하지만 해당 인증을 활성화 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="9849c-120">인증을 활성화 하려면 예제의 마지막 명령에 표시 된 **Set-AzExpressRouteCircuit** 가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="9849c-121">변수</span><span class="sxs-lookup"><span data-stu-id="9849c-121">PARAMETERS</span></span>

### <span data-ttu-id="9849c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9849c-122">-DefaultProfile</span></span>
<span data-ttu-id="9849c-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9849c-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9849c-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="9849c-125">이 cmdlet이 권한 부여를 추가 하는 대상 지정 회로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="9849c-126">-이름</span><span class="sxs-lookup"><span data-stu-id="9849c-126">-Name</span></span>
<span data-ttu-id="9849c-127">추가할 회로 승인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="9849c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9849c-128">CommonParameters</span></span>
<span data-ttu-id="9849c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9849c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9849c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9849c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9849c-131">입력</span><span class="sxs-lookup"><span data-stu-id="9849c-131">INPUTS</span></span>

### <span data-ttu-id="9849c-132">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9849c-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9849c-133">출력</span><span class="sxs-lookup"><span data-stu-id="9849c-133">OUTPUTS</span></span>

### <span data-ttu-id="9849c-134">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9849c-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9849c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="9849c-135">NOTES</span></span>

## <span data-ttu-id="9849c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9849c-136">RELATED LINKS</span></span>

[<span data-ttu-id="9849c-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9849c-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9849c-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9849c-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="9849c-139">새로운 AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9849c-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="9849c-140">제거-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9849c-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="9849c-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9849c-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
