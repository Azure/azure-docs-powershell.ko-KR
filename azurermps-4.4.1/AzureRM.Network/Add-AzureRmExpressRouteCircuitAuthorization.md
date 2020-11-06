---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 03b9e64970be7f3d3876a3d04f26b11ac24dd8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534908"
---
# <span data-ttu-id="dbe3a-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="dbe3a-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="dbe3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbe3a-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe3a-103">Express 경로 회로 인증을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbe3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbe3a-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbe3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbe3a-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe3a-106">**AzureRmExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 인증을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="dbe3a-107">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="dbe3a-108">Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다 (가상 네트워크 당 하나의 권한 부여).</span><span class="sxs-lookup"><span data-stu-id="dbe3a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="dbe3a-109">**추가-AzureRmExpressRouteCircuitAuthorization** 는 회로에 새 권한 부여를 추가 하 고 동시에 해당 하는 인증 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="dbe3a-110">이러한 키는 언제 든 지 Get-AzureRmExpressRouteCircuitAuthorization cmdlet을 실행 하 여 볼 수 있으며 필요한 경우 복사 하 여 적절 한 네트워크 소유자에 게 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="dbe3a-111">**Add-AzureRmExpressRouteCircuitAuthorization** 을 실행 한 후에는 Set-AzureRmExpressRouteCircuit cmdlet을 호출 하 여 키를 활성화 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="dbe3a-112">**Set-AzureRmExpressRouteCircuit** 를 호출 하지 않으면 권한 부여가 회로에 추가 되지만 사용할 수 있도록 설정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="dbe3a-113">예제의</span><span class="sxs-lookup"><span data-stu-id="dbe3a-113">EXAMPLES</span></span>

### <span data-ttu-id="dbe3a-114">예제 1: 지정 된 Express 경로 회로에 대 한 권한 부여 추가</span><span class="sxs-lookup"><span data-stu-id="dbe3a-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="dbe3a-115">이 예제의 명령은 기존 Express 경로에 새 인증을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="dbe3a-116">첫 번째 명령은 **AzureRmExpressRouteCircuit** 를 사용 하 여 ContosoCircuit 라는 회로에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="dbe3a-117">해당 개체 참조는 $Circuit 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="dbe3a-118">두 번째 명령에서는 **추가-AzureRmExpressRouteCircuitAuthorization** cmdlet을 사용 하 여 새 권한 부여 (ContosoCircuitAuthorization)를 express 회로에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="dbe3a-119">이 명령은 권한 부여를 추가 하지만 해당 인증을 활성화 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="dbe3a-120">인증을 활성화 하려면 예제의 마지막 명령에 표시 된 **Set-AzureRmExpressRouteCircuit** 가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="dbe3a-121">변수</span><span class="sxs-lookup"><span data-stu-id="dbe3a-121">PARAMETERS</span></span>

### <span data-ttu-id="dbe3a-122">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dbe3a-122">-ExpressRouteCircuit</span></span>
<span data-ttu-id="dbe3a-123">이 cmdlet이 권한 부여를 추가 하는 대상 지정 회로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-123">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="dbe3a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="dbe3a-124">-Name</span></span>
<span data-ttu-id="dbe3a-125">추가할 회로 승인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-125">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="dbe3a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe3a-126">-DefaultProfile</span></span>
<span data-ttu-id="dbe3a-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbe3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe3a-128">CommonParameters</span></span>
<span data-ttu-id="dbe3a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe3a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe3a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe3a-131">입력</span><span class="sxs-lookup"><span data-stu-id="dbe3a-131">INPUTS</span></span>

### <span data-ttu-id="dbe3a-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dbe3a-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="dbe3a-133">**Add-AzureRmExpressRouteCircuitAuthorization** 는 **PSExpressRouteCircuit** 개체의 파이프라인 인스턴스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="dbe3a-134">출력</span><span class="sxs-lookup"><span data-stu-id="dbe3a-134">OUTPUTS</span></span>

### <span data-ttu-id="dbe3a-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dbe3a-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="dbe3a-136">**Add-AzureRmExpressRouteCircuitAuthorization** 는 **PSExpressRouteCircuit** 개체의 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbe3a-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="dbe3a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="dbe3a-137">NOTES</span></span>

## <span data-ttu-id="dbe3a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbe3a-138">RELATED LINKS</span></span>

[<span data-ttu-id="dbe3a-139">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dbe3a-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="dbe3a-140">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="dbe3a-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="dbe3a-141">새로운 AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="dbe3a-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="dbe3a-142">제거-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="dbe3a-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="dbe3a-143">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dbe3a-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
