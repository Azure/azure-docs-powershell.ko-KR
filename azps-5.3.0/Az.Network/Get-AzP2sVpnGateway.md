---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 541115347cfca85e0259e425912e83c4649e0952
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495573"
---
# <span data-ttu-id="7d013-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7d013-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="7d013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d013-102">SYNOPSIS</span></span>
<span data-ttu-id="7d013-103">VirtualHub에서 기존 P2SVpnGateway를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d013-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="7d013-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d013-104">SYNTAX</span></span>

### <span data-ttu-id="7d013-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d013-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d013-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d013-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d013-107">설명</span><span class="sxs-lookup"><span data-stu-id="7d013-107">DESCRIPTION</span></span>
<span data-ttu-id="7d013-108">**Get-AzP2sVpnGateway** cmdlet을 사용하면 VirtualHub에서 기존 P2SVpnGateway를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d013-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="7d013-109">예제</span><span class="sxs-lookup"><span data-stu-id="7d013-109">EXAMPLES</span></span>

### <span data-ttu-id="7d013-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d013-110">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="7d013-111">**Get-AzP2sVpnGateway** cmdlet을 사용하면 지점 및 사이트 연결에 사용되는 VirtualHub에서 기존 P2SVpnGateway를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d013-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="7d013-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d013-112">PARAMETERS</span></span>

### <span data-ttu-id="7d013-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d013-113">-DefaultProfile</span></span>
<span data-ttu-id="7d013-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d013-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d013-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7d013-115">-Name</span></span>
<span data-ttu-id="7d013-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d013-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, P2SVpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d013-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d013-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d013-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d013-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d013-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d013-119">CommonParameters</span></span>
<span data-ttu-id="7d013-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d013-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d013-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d013-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d013-122">입력</span><span class="sxs-lookup"><span data-stu-id="7d013-122">INPUTS</span></span>

### <span data-ttu-id="7d013-123">없음</span><span class="sxs-lookup"><span data-stu-id="7d013-123">None</span></span>

## <span data-ttu-id="7d013-124">출력</span><span class="sxs-lookup"><span data-stu-id="7d013-124">OUTPUTS</span></span>

### <span data-ttu-id="7d013-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7d013-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7d013-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d013-126">NOTES</span></span>

## <span data-ttu-id="7d013-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d013-127">RELATED LINKS</span></span>
