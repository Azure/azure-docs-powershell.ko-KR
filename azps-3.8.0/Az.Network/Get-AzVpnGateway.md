---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: 646d060dabd002ac5e817d8719c48a2f37a4113b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044860"
---
# <span data-ttu-id="15a6b-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="15a6b-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="15a6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="15a6b-103">ResourceGroupName 및 VpnGateway Name을 사용 하 여 리소스를 가져오거나 ResourceGroupName 또는 SubscriptionId에의 한 모든 게이트웨이를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="15a6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15a6b-104">SYNTAX</span></span>

### <span data-ttu-id="15a6b-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="15a6b-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a6b-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a6b-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15a6b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="15a6b-107">DESCRIPTION</span></span>
<span data-ttu-id="15a6b-108">ResourceGroupName 및 VpnGateway Name을 사용 하 여 리소스를 가져오거나 ResourceGroupName 또는 SubscriptionId에의 한 모든 게이트웨이를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="15a6b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="15a6b-109">EXAMPLES</span></span>

### <span data-ttu-id="15a6b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="15a6b-110">Example 1</span></span>

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
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="15a6b-111">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="15a6b-112">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="15a6b-113">그런 다음 해당 resourceGroupName 및 게이트웨이 이름을 사용 하 여 VpnGateway를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="15a6b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="15a6b-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="15a6b-115">이 cmdlet은 "test"로 시작 하는 모든 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="15a6b-116">변수</span><span class="sxs-lookup"><span data-stu-id="15a6b-116">PARAMETERS</span></span>

### <span data-ttu-id="15a6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a6b-117">-DefaultProfile</span></span>
<span data-ttu-id="15a6b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a6b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="15a6b-119">-Name</span></span>
<span data-ttu-id="15a6b-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-120">The resource name.</span></span>

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

### <span data-ttu-id="15a6b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a6b-121">-ResourceGroupName</span></span>
<span data-ttu-id="15a6b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-122">The resource group name.</span></span>

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

### <span data-ttu-id="15a6b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a6b-123">CommonParameters</span></span>
<span data-ttu-id="15a6b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15a6b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a6b-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15a6b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a6b-126">입력</span><span class="sxs-lookup"><span data-stu-id="15a6b-126">INPUTS</span></span>

### <span data-ttu-id="15a6b-127">않아야</span><span class="sxs-lookup"><span data-stu-id="15a6b-127">None</span></span>

## <span data-ttu-id="15a6b-128">출력</span><span class="sxs-lookup"><span data-stu-id="15a6b-128">OUTPUTS</span></span>

### <span data-ttu-id="15a6b-129">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="15a6b-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="15a6b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="15a6b-130">NOTES</span></span>

## <span data-ttu-id="15a6b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15a6b-131">RELATED LINKS</span></span>

[<span data-ttu-id="15a6b-132">새로운 AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="15a6b-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="15a6b-133">제거-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="15a6b-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="15a6b-134">업데이트-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="15a6b-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
