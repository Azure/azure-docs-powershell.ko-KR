---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043360"
---
# <span data-ttu-id="14996-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="14996-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="14996-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14996-102">SYNOPSIS</span></span>
<span data-ttu-id="14996-103">ResourceGroupName 및 ExpressRouteGateway Name을 사용 하 여 리소스를 가져오거나 ResourceGroupName 또는 SubscriptionId에의 한 모든 게이트웨이를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="14996-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="14996-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14996-104">SYNTAX</span></span>

### <span data-ttu-id="14996-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="14996-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14996-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14996-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14996-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="14996-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14996-108">설명은</span><span class="sxs-lookup"><span data-stu-id="14996-108">DESCRIPTION</span></span>
<span data-ttu-id="14996-109">ResourceGroupName 및 ExpressRouteGateway Name을 사용 하 여 리소스를 가져오거나 ResourceGroupName 또는 SubscriptionId에의 한 모든 게이트웨이를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="14996-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="14996-110">예제의</span><span class="sxs-lookup"><span data-stu-id="14996-110">EXAMPLES</span></span>

### <span data-ttu-id="14996-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="14996-111">Example 1</span></span>

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

<span data-ttu-id="14996-112">위의 방법으로 Azure의 "testRG" 리소스 그룹에 서 중앙 미국에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14996-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="14996-113">1 개의 배율 단위를 사용 하 여 가상 허브에 Express 경로 게이트웨이가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14996-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="14996-114">그런 다음 해당 resourceGroupName 및 게이트웨이 이름을 사용 하 여 ExpressRouteGateway를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14996-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="14996-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="14996-115">Example 2</span></span>

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

<span data-ttu-id="14996-116">이 명령은 "test"로 시작 하는 모든 ExpressRouteGateways를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14996-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="14996-117">변수</span><span class="sxs-lookup"><span data-stu-id="14996-117">PARAMETERS</span></span>

### <span data-ttu-id="14996-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14996-118">-DefaultProfile</span></span>
<span data-ttu-id="14996-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14996-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14996-120">-이름</span><span class="sxs-lookup"><span data-stu-id="14996-120">-Name</span></span>
<span data-ttu-id="14996-121">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14996-121">The resource name.</span></span>

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

### <span data-ttu-id="14996-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14996-122">-ResourceGroupName</span></span>
<span data-ttu-id="14996-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14996-123">The resource group name.</span></span>

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

### <span data-ttu-id="14996-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14996-124">-ResourceId</span></span>
<span data-ttu-id="14996-125">삭제할 expressRouteGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14996-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="14996-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14996-126">CommonParameters</span></span>
<span data-ttu-id="14996-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14996-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14996-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14996-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14996-129">입력</span><span class="sxs-lookup"><span data-stu-id="14996-129">INPUTS</span></span>

### <span data-ttu-id="14996-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14996-130">System.String</span></span>

## <span data-ttu-id="14996-131">출력</span><span class="sxs-lookup"><span data-stu-id="14996-131">OUTPUTS</span></span>

### <span data-ttu-id="14996-132">PSExpressRouteGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="14996-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="14996-133">상속자</span><span class="sxs-lookup"><span data-stu-id="14996-133">NOTES</span></span>

## <span data-ttu-id="14996-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14996-134">RELATED LINKS</span></span>
