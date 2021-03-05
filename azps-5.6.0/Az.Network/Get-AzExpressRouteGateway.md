---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 0d7bec7a40ced6ddcd5ffc61f48f233cea115459
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009467"
---
# <span data-ttu-id="5b006-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="5b006-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="5b006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b006-102">SYNOPSIS</span></span>
<span data-ttu-id="5b006-103">ResourceGroupName 및 GatewayName을 사용하여 ExpressRouteGateway 리소스를 얻거나 ResourceGroupName 또는 SubscriptionId에 의해 모든 게이트웨이를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="5b006-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b006-104">SYNTAX</span></span>

### <span data-ttu-id="5b006-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b006-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b006-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b006-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b006-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="5b006-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b006-108">설명</span><span class="sxs-lookup"><span data-stu-id="5b006-108">DESCRIPTION</span></span>
<span data-ttu-id="5b006-109">ResourceGroupName 및 GatewayName을 사용하여 ExpressRouteGateway 리소스를 얻거나 ResourceGroupName 또는 SubscriptionId에 의해 모든 게이트웨이를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="5b006-110">예제</span><span class="sxs-lookup"><span data-stu-id="5b006-110">EXAMPLES</span></span>

### <span data-ttu-id="5b006-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b006-111">Example 1</span></span>

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

<span data-ttu-id="5b006-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 "testRG" 리소스 그룹에 미국 중서부에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5b006-113">2개 확장 단위가 있는 Virtual Hub에서 ExpressRoute 게이트웨이가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5b006-114">그런 다음 해당 resourceGroupName 및 게이트웨이 이름을 사용하여 ExpressRouteGateway를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="5b006-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="5b006-115">Example 2</span></span>

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

<span data-ttu-id="5b006-116">이 명령은 "test"로 시작하는 모든 ExpressRouteGateways를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="5b006-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b006-117">PARAMETERS</span></span>

### <span data-ttu-id="5b006-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b006-118">-DefaultProfile</span></span>
<span data-ttu-id="5b006-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b006-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b006-120">-Name</span></span>
<span data-ttu-id="5b006-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-121">The resource name.</span></span>

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

### <span data-ttu-id="5b006-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b006-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b006-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-123">The resource group name.</span></span>

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

### <span data-ttu-id="5b006-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b006-124">-ResourceId</span></span>
<span data-ttu-id="5b006-125">삭제할 expressRouteGateway에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="5b006-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b006-126">CommonParameters</span></span>
<span data-ttu-id="5b006-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b006-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b006-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b006-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b006-129">입력</span><span class="sxs-lookup"><span data-stu-id="5b006-129">INPUTS</span></span>

### <span data-ttu-id="5b006-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5b006-130">System.String</span></span>

## <span data-ttu-id="5b006-131">출력</span><span class="sxs-lookup"><span data-stu-id="5b006-131">OUTPUTS</span></span>

### <span data-ttu-id="5b006-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="5b006-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="5b006-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b006-133">NOTES</span></span>

## <span data-ttu-id="5b006-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b006-134">RELATED LINKS</span></span>
