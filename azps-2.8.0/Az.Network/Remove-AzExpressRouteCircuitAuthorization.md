---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 62cfc4fc3555b9eb798a1d64c53b0b25e9abc14c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871257"
---
# <span data-ttu-id="b56d8-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b56d8-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="b56d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b56d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b56d8-103">기존 Express 경로 구성 권한 부여를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="b56d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b56d8-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b56d8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b56d8-105">DESCRIPTION</span></span>
<span data-ttu-id="b56d8-106">**AzExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 할당 된 인증을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="b56d8-107">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="b56d8-108">Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="b56d8-109">가상 네트워크 당 하나의 권한 부여만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="b56d8-110">그러나 언제 든 지 회로 소유자는 **제거-AzExpressRouteCircuitAuthorization** 를 사용 하 여 가상 네트워크에 할당 된 권한을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="b56d8-111">이 경우 해당 가상 네트워크는 더 이상 대상 경로를 사용 하 여 Azure에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="b56d8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b56d8-112">EXAMPLES</span></span>

### <span data-ttu-id="b56d8-113">예제 1: Express 회로에서 회로 승인 제거</span><span class="sxs-lookup"><span data-stu-id="b56d8-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="b56d8-114">이 예제에서는 Express 경로 회로에서 회로 인증을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="b56d8-115">첫 번째 명령은 **AzExpressRouteCircuit** cmdlet을 사용 하 여 ContosoCircuit 이라는 express 경로에 대 한 개체 참조를 만들고 결과를 $Circuit 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="b56d8-116">두 번째 명령은 회로 권한 부여 ContosoCircuitAuthorization 제거를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="b56d8-117">세 번째 명령은 Set-AzExpressRouteCircuit cmdlet을 사용 하 여 $Circuit 변수에 저장 된 Express 대상 회로가 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="b56d8-118">변수</span><span class="sxs-lookup"><span data-stu-id="b56d8-118">PARAMETERS</span></span>

### <span data-ttu-id="b56d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56d8-119">-DefaultProfile</span></span>
<span data-ttu-id="b56d8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b56d8-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b56d8-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b56d8-122">이 cmdlet이 제거 하는 ExpressRouteCircuit 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b56d8-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b56d8-123">-Name</span></span>
<span data-ttu-id="b56d8-124">이 cmdlet이 제거 하는 회로 권한 부여의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b56d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56d8-125">CommonParameters</span></span>
<span data-ttu-id="b56d8-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b56d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56d8-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56d8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56d8-128">입력</span><span class="sxs-lookup"><span data-stu-id="b56d8-128">INPUTS</span></span>

### <span data-ttu-id="b56d8-129">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b56d8-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b56d8-130">출력</span><span class="sxs-lookup"><span data-stu-id="b56d8-130">OUTPUTS</span></span>

### <span data-ttu-id="b56d8-131">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b56d8-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b56d8-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b56d8-132">NOTES</span></span>

## <span data-ttu-id="b56d8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b56d8-133">RELATED LINKS</span></span>

[<span data-ttu-id="b56d8-134">추가-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b56d8-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b56d8-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b56d8-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b56d8-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b56d8-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b56d8-137">새로운 AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b56d8-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b56d8-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b56d8-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
