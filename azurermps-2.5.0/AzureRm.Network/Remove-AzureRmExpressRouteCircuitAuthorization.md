---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880962"
---
# <span data-ttu-id="33364-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33364-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="33364-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33364-102">SYNOPSIS</span></span>
<span data-ttu-id="33364-103">기존 Express 경로 구성 권한 부여를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33364-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33364-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33364-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33364-105">DESCRIPTION</span></span>
<span data-ttu-id="33364-106">**AzureRmExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 할당 된 인증을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="33364-107">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Azure에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="33364-108">Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="33364-109">가상 네트워크 당 하나의 권한 부여만 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33364-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="33364-110">그러나 언제 든 지 회로 소유자는 **제거-AzureRmExpressRouteCircuitAuthorization** 를 사용 하 여 가상 네트워크에 할당 된 권한을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33364-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="33364-111">이 경우 해당 가상 네트워크는 더 이상 대상 경로를 사용 하 여 Azure에 연결할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="33364-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="33364-112">예제의</span><span class="sxs-lookup"><span data-stu-id="33364-112">EXAMPLES</span></span>

### <span data-ttu-id="33364-113">예제 1: Express 회로에서 회로 승인 제거</span><span class="sxs-lookup"><span data-stu-id="33364-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="33364-114">이 예제에서는 Express 경로 회로에서 회로 인증을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="33364-115">첫 번째 명령은 **AzureRmExpressRouteCircuit** cmdlet을 사용 하 여 ContosoCircuit 이라는 express 경로에 대 한 개체 참조를 만들고 결과를 $Circuit 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="33364-116">두 번째 명령은 회로 권한 부여 ContosoCircuitAuthorization 제거를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="33364-117">세 번째 명령은 Set-AzureRmExpressRouteCircuit cmdlet을 사용 하 여 $Circuit 변수에 저장 된 Express 대상 회로가 제거 되었는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="33364-118">변수</span><span class="sxs-lookup"><span data-stu-id="33364-118">PARAMETERS</span></span>

### <span data-ttu-id="33364-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33364-119">-DefaultProfile</span></span>
<span data-ttu-id="33364-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33364-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33364-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="33364-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="33364-122">이 cmdlet이 제거 하는 ExpressRouteCircuit 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33364-123">-이름</span><span class="sxs-lookup"><span data-stu-id="33364-123">-Name</span></span>
<span data-ttu-id="33364-124">이 cmdlet이 제거 하는 회로 권한 부여의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33364-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33364-125">CommonParameters</span></span>
<span data-ttu-id="33364-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33364-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33364-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33364-128">입력</span><span class="sxs-lookup"><span data-stu-id="33364-128">INPUTS</span></span>

### <span data-ttu-id="33364-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="33364-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="33364-130">이 cmdlet은 **PSExpressRouteCircuit** 개체의 파이프라인 인스턴스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="33364-131">출력</span><span class="sxs-lookup"><span data-stu-id="33364-131">OUTPUTS</span></span>

### <span data-ttu-id="33364-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="33364-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="33364-133">이 cmdlet은 **PSExpressRouteCircuit** 개체의 기존 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33364-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="33364-134">상속자</span><span class="sxs-lookup"><span data-stu-id="33364-134">NOTES</span></span>

## <span data-ttu-id="33364-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33364-135">RELATED LINKS</span></span>

[<span data-ttu-id="33364-136">추가-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33364-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="33364-137">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="33364-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="33364-138">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33364-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="33364-139">새로운 AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="33364-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="33364-140">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="33364-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
