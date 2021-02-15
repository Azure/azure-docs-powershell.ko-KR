---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: b6537b9b8501aa2ec0aa76c9ede080893bf136ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187097"
---
# <span data-ttu-id="b14b7-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b14b7-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="b14b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b14b7-102">SYNOPSIS</span></span>
<span data-ttu-id="b14b7-103">ResourceGroupName 및 GatewayName을 사용하여 VpnGateway 리소스를 얻거나 ResourceGroupName 또는 SubscriptionId에 의해 모든 게이트웨이를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="b14b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="b14b7-104">SYNTAX</span></span>

### <span data-ttu-id="b14b7-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="b14b7-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b14b7-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b14b7-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b14b7-107">설명</span><span class="sxs-lookup"><span data-stu-id="b14b7-107">DESCRIPTION</span></span>
<span data-ttu-id="b14b7-108">ResourceGroupName 및 GatewayName을 사용하여 VpnGateway 리소스를 얻거나 ResourceGroupName 또는 SubscriptionId에 의해 모든 게이트웨이를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="b14b7-109">예제</span><span class="sxs-lookup"><span data-stu-id="b14b7-109">EXAMPLES</span></span>

### <span data-ttu-id="b14b7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b14b7-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="b14b7-111">위의 리소스 그룹인 Virtual WAN, Virtual Network, Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b14b7-112">VPN Gateway는 2개 배율 단위가 있는 가상 허브에서 이후에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="b14b7-113">그런 다음 resourceGroupName 및 게이트웨이 이름을 사용하여 VpnGateway를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="b14b7-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="b14b7-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
IpConfigurations    : {Instance0, Instance1}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="b14b7-115">이 cmdlet은 "test"로 시작하는 모든 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="b14b7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b14b7-116">PARAMETERS</span></span>

### <span data-ttu-id="b14b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14b7-117">-DefaultProfile</span></span>
<span data-ttu-id="b14b7-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b14b7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b14b7-119">-Name</span></span>
<span data-ttu-id="b14b7-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="b14b7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b14b7-121">-ResourceGroupName</span></span>
<span data-ttu-id="b14b7-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-122">The resource group name.</span></span>

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

### <span data-ttu-id="b14b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14b7-123">CommonParameters</span></span>
<span data-ttu-id="b14b7-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b14b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14b7-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b14b7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14b7-126">입력</span><span class="sxs-lookup"><span data-stu-id="b14b7-126">INPUTS</span></span>

### <span data-ttu-id="b14b7-127">없음</span><span class="sxs-lookup"><span data-stu-id="b14b7-127">None</span></span>

## <span data-ttu-id="b14b7-128">출력</span><span class="sxs-lookup"><span data-stu-id="b14b7-128">OUTPUTS</span></span>

### <span data-ttu-id="b14b7-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b14b7-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="b14b7-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b14b7-130">NOTES</span></span>

## <span data-ttu-id="b14b7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b14b7-131">RELATED LINKS</span></span>

[<span data-ttu-id="b14b7-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b14b7-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="b14b7-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b14b7-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="b14b7-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b14b7-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
