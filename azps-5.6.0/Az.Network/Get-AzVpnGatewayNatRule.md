---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
ms.openlocfilehash: 1670e8549f561f0b1fae12711303bb3e1ac83280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965696"
---
# <span data-ttu-id="6f50f-101">Get-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="6f50f-101">Get-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="6f50f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f50f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f50f-103">VpnGateway와 연결된 NAT 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-103">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="6f50f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f50f-104">SYNTAX</span></span>

### <span data-ttu-id="6f50f-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6f50f-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f50f-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6f50f-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f50f-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6f50f-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnGatewayNatRule -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f50f-108">설명</span><span class="sxs-lookup"><span data-stu-id="6f50f-108">DESCRIPTION</span></span>
<span data-ttu-id="6f50f-109">VpnGateway와 연결된 NAT 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-109">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="6f50f-110">예제</span><span class="sxs-lookup"><span data-stu-id="6f50f-110">EXAMPLES</span></span>

### <span data-ttu-id="6f50f-111">예제</span><span class="sxs-lookup"><span data-stu-id="6f50f-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Get-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule

```

<span data-ttu-id="6f50f-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub 및 VpnGateway는 vpngateway와 & NAT 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and VpnGateway & a NAT rule associated with Vpngateway.</span></span>
<span data-ttu-id="6f50f-113">그런 다음 NAT 규칙 이름을 사용하여 NAT 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-113">Then it gets the NAT rule using the NAT rule name.</span></span>

## <span data-ttu-id="6f50f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6f50f-114">PARAMETERS</span></span>

### <span data-ttu-id="6f50f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f50f-115">-DefaultProfile</span></span>
<span data-ttu-id="6f50f-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f50f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6f50f-117">-Name</span></span>
<span data-ttu-id="6f50f-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f50f-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6f50f-119">-ParentObject</span></span>
<span data-ttu-id="6f50f-120">이 VpnGatewayNatRule의 부모 VpnGateway입니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-120">The parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f50f-121">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6f50f-121">-ParentResourceId</span></span>
<span data-ttu-id="6f50f-122">이 VpnGatewayNatRule에 대한 부모 VpnGateway의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-122">The resource id of the parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f50f-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="6f50f-123">-ParentResourceName</span></span>
<span data-ttu-id="6f50f-124">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f50f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f50f-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f50f-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f50f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f50f-127">CommonParameters</span></span>
<span data-ttu-id="6f50f-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f50f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f50f-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f50f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f50f-130">입력</span><span class="sxs-lookup"><span data-stu-id="6f50f-130">INPUTS</span></span>

### <span data-ttu-id="6f50f-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6f50f-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="6f50f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6f50f-132">System.String</span></span>

## <span data-ttu-id="6f50f-133">출력</span><span class="sxs-lookup"><span data-stu-id="6f50f-133">OUTPUTS</span></span>

### <span data-ttu-id="6f50f-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="6f50f-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="6f50f-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f50f-135">NOTES</span></span>

## <span data-ttu-id="6f50f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f50f-136">RELATED LINKS</span></span>
