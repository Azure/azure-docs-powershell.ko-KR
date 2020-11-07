---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: e37c8fdded8fa5e141138903e502e2e1b0f1a0f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700604"
---
# <span data-ttu-id="98d4b-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="98d4b-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="98d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="98d4b-103">Azure에서 Azure Express 경로 회로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="98d4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98d4b-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="98d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="98d4b-106">**AzExpressRouteCircuit** cmdlet은 구독에서 express 경로 회로 개체를 검색 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="98d4b-107">반환 되는 회로 개체는 Express 경로 회로에서 작동 하는 다른 cmdlet에 대 한 입력으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="98d4b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="98d4b-108">EXAMPLES</span></span>

### <span data-ttu-id="98d4b-109">예제 1: Express 경로 가져오기</span><span class="sxs-lookup"><span data-stu-id="98d4b-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="98d4b-110">이름이 "testrg"이 고 ResourceGroupName "test" 인 특정 Express 경로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="98d4b-111">예제 2: 필터링을 사용 하 여가을 기준으로 Express 회로 나열</span><span class="sxs-lookup"><span data-stu-id="98d4b-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="98d4b-112">이름이 "test"로 시작 하는 모든 Express 회로를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="98d4b-113">변수</span><span class="sxs-lookup"><span data-stu-id="98d4b-113">PARAMETERS</span></span>

### <span data-ttu-id="98d4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d4b-114">-DefaultProfile</span></span>
<span data-ttu-id="98d4b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98d4b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="98d4b-116">-Name</span></span>
<span data-ttu-id="98d4b-117">Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="98d4b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d4b-118">-ResourceGroupName</span></span>
<span data-ttu-id="98d4b-119">Express 경로 회로가 포함 된 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="98d4b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d4b-120">CommonParameters</span></span>
<span data-ttu-id="98d4b-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98d4b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d4b-122">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="98d4b-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d4b-123">입력</span><span class="sxs-lookup"><span data-stu-id="98d4b-123">INPUTS</span></span>

### <span data-ttu-id="98d4b-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="98d4b-124">System.String</span></span>

## <span data-ttu-id="98d4b-125">출력</span><span class="sxs-lookup"><span data-stu-id="98d4b-125">OUTPUTS</span></span>

### <span data-ttu-id="98d4b-126">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="98d4b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="98d4b-127">상속자</span><span class="sxs-lookup"><span data-stu-id="98d4b-127">NOTES</span></span>

## <span data-ttu-id="98d4b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98d4b-128">RELATED LINKS</span></span>

[<span data-ttu-id="98d4b-129">이동-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="98d4b-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="98d4b-130">새로운 AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="98d4b-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="98d4b-131">제거-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="98d4b-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="98d4b-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="98d4b-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
