---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529520"
---
# <span data-ttu-id="41b48-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="41b48-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="41b48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41b48-102">SYNOPSIS</span></span>
<span data-ttu-id="41b48-103">ResourceGroupName 및 VpnGateway Name을 사용 하 여 리소스를 가져오거나 ResourceGroupName 또는 SubscriptionId에의 한 모든 게이트웨이를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41b48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41b48-104">SYNTAX</span></span>

### <span data-ttu-id="41b48-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="41b48-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41b48-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b48-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41b48-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41b48-107">DESCRIPTION</span></span>
<span data-ttu-id="41b48-108">ResourceGroupName 및 VpnGateway Name을 사용 하 여 리소스를 가져오거나 ResourceGroupName 또는 SubscriptionId에의 한 모든 게이트웨이를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="41b48-109">예제의</span><span class="sxs-lookup"><span data-stu-id="41b48-109">EXAMPLES</span></span>

### <span data-ttu-id="41b48-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="41b48-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

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

<span data-ttu-id="41b48-111">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="41b48-112">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="41b48-113">그런 다음 해당 resourceGroupName 및 게이트웨이 이름을 사용 하 여 VpnGateway를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="41b48-114">변수</span><span class="sxs-lookup"><span data-stu-id="41b48-114">PARAMETERS</span></span>

### <span data-ttu-id="41b48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b48-115">-DefaultProfile</span></span>
<span data-ttu-id="41b48-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41b48-117">-이름</span><span class="sxs-lookup"><span data-stu-id="41b48-117">-Name</span></span>
<span data-ttu-id="41b48-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b48-119">-ResourceGroupName</span></span>
<span data-ttu-id="41b48-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b48-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b48-121">CommonParameters</span></span>
<span data-ttu-id="41b48-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41b48-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b48-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b48-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b48-124">입력</span><span class="sxs-lookup"><span data-stu-id="41b48-124">INPUTS</span></span>

### <span data-ttu-id="41b48-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41b48-125">System.String</span></span>

## <span data-ttu-id="41b48-126">출력</span><span class="sxs-lookup"><span data-stu-id="41b48-126">OUTPUTS</span></span>

### <span data-ttu-id="41b48-127">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="41b48-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="41b48-128">상속자</span><span class="sxs-lookup"><span data-stu-id="41b48-128">NOTES</span></span>

## <span data-ttu-id="41b48-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41b48-129">RELATED LINKS</span></span>
