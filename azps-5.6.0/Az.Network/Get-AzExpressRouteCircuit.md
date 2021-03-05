---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 8961948970843873f337fd1625aabfdf878ba15d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967904"
---
# <span data-ttu-id="1a7ce-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a7ce-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="1a7ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="1a7ce-103">Azure에서 Azure ExpressRoute 회로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="1a7ce-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a7ce-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a7ce-105">설명</span><span class="sxs-lookup"><span data-stu-id="1a7ce-105">DESCRIPTION</span></span>
<span data-ttu-id="1a7ce-106">**Get-AzExpressRouteCircuit** cmdlet은 구독에서 ExpressRoute 회로 개체를 검색하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="1a7ce-107">반환된 회로 개체는 ExpressRoute 회로에서 작동하는 다른 cmdlet에 대한 입력으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="1a7ce-108">예제</span><span class="sxs-lookup"><span data-stu-id="1a7ce-108">EXAMPLES</span></span>

### <span data-ttu-id="1a7ce-109">예제 1: ExpressRoute 회로 사용</span><span class="sxs-lookup"><span data-stu-id="1a7ce-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="1a7ce-110">이름 "testrg" 및 ResourceGroupName "test"를 사용하여 특정 ExpressRoute 회로를 구합니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="1a7ce-111">예제 2: 필터링을 사용하여 ExpressRoute 회로 나열</span><span class="sxs-lookup"><span data-stu-id="1a7ce-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="1a7ce-112">이름이 "test"로 시작하는 모든 ExpressRoute 회로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="1a7ce-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a7ce-113">PARAMETERS</span></span>

### <span data-ttu-id="1a7ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a7ce-114">-DefaultProfile</span></span>
<span data-ttu-id="1a7ce-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a7ce-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1a7ce-116">-Name</span></span>
<span data-ttu-id="1a7ce-117">ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="1a7ce-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a7ce-118">-ResourceGroupName</span></span>
<span data-ttu-id="1a7ce-119">ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="1a7ce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a7ce-120">CommonParameters</span></span>
<span data-ttu-id="1a7ce-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a7ce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a7ce-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a7ce-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a7ce-123">입력</span><span class="sxs-lookup"><span data-stu-id="1a7ce-123">INPUTS</span></span>

### <span data-ttu-id="1a7ce-124">System.String</span><span class="sxs-lookup"><span data-stu-id="1a7ce-124">System.String</span></span>

## <span data-ttu-id="1a7ce-125">출력</span><span class="sxs-lookup"><span data-stu-id="1a7ce-125">OUTPUTS</span></span>

### <span data-ttu-id="1a7ce-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a7ce-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1a7ce-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a7ce-127">NOTES</span></span>

## <span data-ttu-id="1a7ce-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a7ce-128">RELATED LINKS</span></span>

[<span data-ttu-id="1a7ce-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a7ce-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="1a7ce-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a7ce-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="1a7ce-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a7ce-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="1a7ce-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1a7ce-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
