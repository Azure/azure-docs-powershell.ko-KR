---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492768"
---
# <span data-ttu-id="8dc19-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="8dc19-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="8dc19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc19-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc19-103">ResourceGroupName 및 GatewayName을 사용하여 ExpressRouteGateway 리소스를 얻거나 ResourceGroupName 또는 SubscriptionId에 의해 모든 게이트웨이를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="8dc19-104">구문</span><span class="sxs-lookup"><span data-stu-id="8dc19-104">SYNTAX</span></span>

### <span data-ttu-id="8dc19-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="8dc19-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dc19-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc19-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dc19-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc19-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dc19-108">설명</span><span class="sxs-lookup"><span data-stu-id="8dc19-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc19-109">ResourceGroupName 및 GatewayName을 사용하여 ExpressRouteGateway 리소스를 얻거나 ResourceGroupName 또는 SubscriptionId에 의해 모든 게이트웨이를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="8dc19-110">예제</span><span class="sxs-lookup"><span data-stu-id="8dc19-110">EXAMPLES</span></span>

### <span data-ttu-id="8dc19-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8dc19-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="8dc19-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 중서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8dc19-113">ExpressRoute 게이트웨이는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="8dc19-114">그런 다음 resourceGroupName 및 게이트웨이 이름을 사용하여 ExpressRouteGateway를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="8dc19-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="8dc19-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="8dc19-116">이 명령은 "test"로 시작하는 모든 ExpressRouteGateways를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="8dc19-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc19-117">PARAMETERS</span></span>

### <span data-ttu-id="8dc19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc19-118">-DefaultProfile</span></span>
<span data-ttu-id="8dc19-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc19-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8dc19-120">-Name</span></span>
<span data-ttu-id="8dc19-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8dc19-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc19-122">-ResourceGroupName</span></span>
<span data-ttu-id="8dc19-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8dc19-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc19-124">-ResourceId</span></span>
<span data-ttu-id="8dc19-125">삭제할 expressRouteGateway에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc19-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc19-126">CommonParameters</span></span>
<span data-ttu-id="8dc19-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc19-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc19-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8dc19-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc19-129">입력</span><span class="sxs-lookup"><span data-stu-id="8dc19-129">INPUTS</span></span>

### <span data-ttu-id="8dc19-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8dc19-130">System.String</span></span>

## <span data-ttu-id="8dc19-131">출력</span><span class="sxs-lookup"><span data-stu-id="8dc19-131">OUTPUTS</span></span>

### <span data-ttu-id="8dc19-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="8dc19-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="8dc19-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8dc19-133">NOTES</span></span>

## <span data-ttu-id="8dc19-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dc19-134">RELATED LINKS</span></span>
