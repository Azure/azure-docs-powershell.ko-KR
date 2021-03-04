---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: d20e2098a797d2e90363f54d79759dc682413803
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954256"
---
# <span data-ttu-id="9b679-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9b679-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="9b679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b679-102">SYNOPSIS</span></span>
<span data-ttu-id="9b679-103">VirtualHub에서 기존 P2SVpnGateway를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b679-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="9b679-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b679-104">SYNTAX</span></span>

### <span data-ttu-id="9b679-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="9b679-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b679-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b679-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b679-107">설명</span><span class="sxs-lookup"><span data-stu-id="9b679-107">DESCRIPTION</span></span>
<span data-ttu-id="9b679-108">**Get-AzP2sVpnGateway** cmdlet을 사용하면 VirtualHub에서 기존 P2SVpnGateway를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b679-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="9b679-109">예제</span><span class="sxs-lookup"><span data-stu-id="9b679-109">EXAMPLES</span></span>

### <span data-ttu-id="9b679-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b679-110">Example 1</span></span>
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

<span data-ttu-id="9b679-111">**Get-AzP2sVpnGateway** cmdlet을 사용하면 지점 및 사이트 연결에 사용되는 VirtualHub에서 기존 P2SVpnGateway를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b679-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="9b679-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9b679-112">PARAMETERS</span></span>

### <span data-ttu-id="9b679-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b679-113">-DefaultProfile</span></span>
<span data-ttu-id="9b679-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b679-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b679-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9b679-115">-Name</span></span>
<span data-ttu-id="9b679-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b679-116">The resource name.</span></span>

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

### <span data-ttu-id="9b679-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b679-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b679-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b679-118">The resource group name.</span></span>

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

### <span data-ttu-id="9b679-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b679-119">CommonParameters</span></span>
<span data-ttu-id="9b679-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b679-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b679-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9b679-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b679-122">입력</span><span class="sxs-lookup"><span data-stu-id="9b679-122">INPUTS</span></span>

### <span data-ttu-id="9b679-123">없음</span><span class="sxs-lookup"><span data-stu-id="9b679-123">None</span></span>

## <span data-ttu-id="9b679-124">출력</span><span class="sxs-lookup"><span data-stu-id="9b679-124">OUTPUTS</span></span>

### <span data-ttu-id="9b679-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9b679-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="9b679-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b679-126">NOTES</span></span>

## <span data-ttu-id="9b679-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b679-127">RELATED LINKS</span></span>
