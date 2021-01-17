---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489959"
---
# <span data-ttu-id="1a206-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1a206-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="1a206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a206-102">SYNOPSIS</span></span>
<span data-ttu-id="1a206-103">ExpressRoute 회로 권한 부여에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="1a206-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a206-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a206-105">설명</span><span class="sxs-lookup"><span data-stu-id="1a206-105">DESCRIPTION</span></span>
<span data-ttu-id="1a206-106">**Get-AzExpressRouteCircuitAuthorization** cmdlet은 ExpressRoute 회로에 할당된 권한 부여에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="1a206-107">ExpressRoute 회로는 공용 인터넷 대신 연결 공급자를 사용하여 Microsoft 클라우드에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="1a206-108">ExpressRoute 회로의 소유자는 각 회로에 대해 10개까지 권한 부여를 만들 수 있습니다. 이러한 권한 부여는 가상 네트워크 소유자가 자신의 네트워크를 회로에 연결하는 데 사용할 수 있는 권한 부여 키를 생성합니다(가상 네트워크당 하나의 권한 부여).</span><span class="sxs-lookup"><span data-stu-id="1a206-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="1a206-109">권한 부여 키 및 권한 부여에 대한 기타 정보는 **Get-AzExpressRouteCircuitAuthorization을** 실행하여 수시로 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="1a206-110">예제</span><span class="sxs-lookup"><span data-stu-id="1a206-110">EXAMPLES</span></span>

### <span data-ttu-id="1a206-111">예제 1: 모든 ExpressRoute 권한 부여를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="1a206-112">이러한 명령은 ExpressRoute 회로와 연결된 모든 ExpressRoute 권한 부여에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="1a206-113">첫 번째 명령은 **Get-AzExpressRouteCircuit** cmdlet을 사용하여 ContosoCircuit이라는 회로를 참조하는 개체를 만듭니다. 해당 개체 참조는 변수에 저장됩니다$Circuit.</span><span class="sxs-lookup"><span data-stu-id="1a206-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="1a206-114">그런 다음, 두 번째 명령은 해당 개체 참조 및 **Get-AzExpressRouteCircuitAuthorization** cmdlet을 사용하여 ContosoCircuit과 연결된 권한 부여에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="1a206-115">예제 2: Where-Object cmdlet을 사용하여 모든 ExpressRoute 권한 부여를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="1a206-116">이러한 명령은 예제 1에 사용된 명령의 변형을 나타났습니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="1a206-117">그러나 이 경우 사용할 수 있는 권한 부여(즉, 가상 네트워크에 할당되지 않은 권한 부여의 경우)에 대한 정보만 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="1a206-118">이를 위해 회로 권한 부여 정보는 명령 2에서 반환되어 **Where-Object** cmdlet으로 파이프됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="1a206-119">**Where-Object는** *AuthorizationUseStatus* 속성이 사용 가능으로 설정된 권한 부여만 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="1a206-120">사용할 수 없는 권한 부여만 나열하기 위해 Where 절에 대해 다음 구문을 사용하세요. `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="1a206-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="1a206-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a206-121">PARAMETERS</span></span>

### <span data-ttu-id="1a206-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a206-122">-DefaultProfile</span></span>
<span data-ttu-id="1a206-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a206-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a206-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1a206-125">ExpressRoute 회로 권한 부여를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="1a206-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1a206-126">-Name</span></span>
<span data-ttu-id="1a206-127">이 cmdlet에서 얻을 ExpressRoute 회로 권한 부여의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="1a206-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="1a206-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="1a206-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a206-129">CommonParameters</span></span>
<span data-ttu-id="1a206-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a206-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a206-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a206-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a206-132">입력</span><span class="sxs-lookup"><span data-stu-id="1a206-132">INPUTS</span></span>

### <span data-ttu-id="1a206-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a206-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1a206-134">출력</span><span class="sxs-lookup"><span data-stu-id="1a206-134">OUTPUTS</span></span>

### <span data-ttu-id="1a206-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1a206-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="1a206-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a206-136">NOTES</span></span>

## <span data-ttu-id="1a206-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a206-137">RELATED LINKS</span></span>

[<span data-ttu-id="1a206-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1a206-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="1a206-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a206-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="1a206-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1a206-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="1a206-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="1a206-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
