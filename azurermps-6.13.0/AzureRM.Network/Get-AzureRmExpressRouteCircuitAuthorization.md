---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 5b277ca35071c3639a3c7b341451cea78c024901
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536600"
---
# <span data-ttu-id="c35a5-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c35a5-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="c35a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c35a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c35a5-103">Express 경로 권한 부여에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c35a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c35a5-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c35a5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c35a5-105">DESCRIPTION</span></span>
<span data-ttu-id="c35a5-106">**AzureRmExpressRouteCircuitAuthorization** Cmdlet은 express 경로 회로에 할당 된 권한 부여에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="c35a5-107">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="c35a5-108">Express 경로 회로의 소유자는 각 회로에 대해 최대 10 개의 권한을 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 네트워크를 회로에 연결 하는 데 사용할 수 있는 인증 키를 생성 합니다 (가상 네트워크 당 하나의 권한 부여).</span><span class="sxs-lookup"><span data-stu-id="c35a5-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="c35a5-109">인증 키 및 권한 부여에 대 한 기타 정보는 **AzureRmExpressRouteCircuitAuthorization** 를 실행 하 여 언제 든 지 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="c35a5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c35a5-110">EXAMPLES</span></span>

### <span data-ttu-id="c35a5-111">예제 1: 모든 Express 위치 권한 부여 가져오기</span><span class="sxs-lookup"><span data-stu-id="c35a5-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="c35a5-112">이러한 명령은 Express 경로 회로와 연결 된 모든 Express 권한 부여에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="c35a5-113">첫 번째 명령은 **AzureRmExpressRouteCircuit** cmdlet을 사용 하 여 개체 참조 (ContosoCircuit 라는 회로)를 만듭니다. 해당 개체 참조는 변수 $Circuit에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="c35a5-114">그런 다음 두 번째 명령은 해당 개체 참조 및 **AzureRmExpressRouteCircuitAuthorization** cmdlet을 사용 하 여 ContosoCircuit와 연결 된 권한 부여에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="c35a5-115">예제 2: Where-Object cmdlet을 사용 하 여 모든 Express 경로 권한 부여 가져오기</span><span class="sxs-lookup"><span data-stu-id="c35a5-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="c35a5-116">이러한 명령은 예제 1에 사용 된 명령의 변형을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="c35a5-117">그러나이 경우에는 사용할 수 있는 권한 부여 (즉, 가상 네트워크에 할당 되지 않은 권한 부여)에 대해서만 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="c35a5-118">이렇게 하려면 회로 인증 정보가 명령 2에 반환 되 고, **Where-Object** cmdlet에 대 한 것으로 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="c35a5-119">**여기서-Object** 는 *AuthorizationUseStatus* 속성이 사용 가능으로 설정 된 권한 부여만 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="c35a5-120">사용할 수 없는 권한 부여만 나열 하려면 Where 절에 다음 구문을 사용 합니다. `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="c35a5-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="c35a5-121">변수</span><span class="sxs-lookup"><span data-stu-id="c35a5-121">PARAMETERS</span></span>

### <span data-ttu-id="c35a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c35a5-122">-DefaultProfile</span></span>
<span data-ttu-id="c35a5-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c35a5-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c35a5-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c35a5-125">Express 경로 회로 인증을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="c35a5-126">-이름</span><span class="sxs-lookup"><span data-stu-id="c35a5-126">-Name</span></span>
<span data-ttu-id="c35a5-127">이 cmdlet이 가져오는 Express 경로에 대 한 회로 권한 부여의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="c35a5-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="c35a5-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="c35a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35a5-129">CommonParameters</span></span>
<span data-ttu-id="c35a5-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c35a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35a5-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c35a5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35a5-132">입력</span><span class="sxs-lookup"><span data-stu-id="c35a5-132">INPUTS</span></span>

### <span data-ttu-id="c35a5-133">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c35a5-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="c35a5-134">매개 변수: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c35a5-134">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="c35a5-135">출력</span><span class="sxs-lookup"><span data-stu-id="c35a5-135">OUTPUTS</span></span>

### <span data-ttu-id="c35a5-136">PSExpressRouteCircuitAuthorization에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c35a5-136">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="c35a5-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c35a5-137">NOTES</span></span>

## <span data-ttu-id="c35a5-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c35a5-138">RELATED LINKS</span></span>

[<span data-ttu-id="c35a5-139">추가-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c35a5-139">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c35a5-140">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c35a5-140">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c35a5-141">새로운 AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c35a5-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="c35a5-142">제거-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="c35a5-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
