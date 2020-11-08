---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 541115347cfca85e0259e425912e83c4649e0952
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204526"
---
# <span data-ttu-id="00f21-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00f21-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="00f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f21-102">SYNOPSIS</span></span>
<span data-ttu-id="00f21-103">VirtualHub 아래에 있는 기존 P2SVpnGateway를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00f21-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="00f21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00f21-104">SYNTAX</span></span>

### <span data-ttu-id="00f21-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="00f21-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00f21-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f21-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00f21-107">설명은</span><span class="sxs-lookup"><span data-stu-id="00f21-107">DESCRIPTION</span></span>
<span data-ttu-id="00f21-108">**AzP2sVpnGateway** cmdlet을 사용 하면 virtualhub 아래에 기존 P2SVpnGateway를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00f21-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="00f21-109">예제의</span><span class="sxs-lookup"><span data-stu-id="00f21-109">EXAMPLES</span></span>

### <span data-ttu-id="00f21-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="00f21-110">Example 1</span></span>
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

<span data-ttu-id="00f21-111">**AzP2sVpnGateway** cmdlet을 사용 하면 사이트 연결을 가리키는 데 사용 되는 virtualhub 아래에 있는 기존 P2SVpnGateway를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00f21-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="00f21-112">변수</span><span class="sxs-lookup"><span data-stu-id="00f21-112">PARAMETERS</span></span>

### <span data-ttu-id="00f21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f21-113">-DefaultProfile</span></span>
<span data-ttu-id="00f21-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00f21-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f21-115">-이름</span><span class="sxs-lookup"><span data-stu-id="00f21-115">-Name</span></span>
<span data-ttu-id="00f21-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00f21-116">The resource name.</span></span>

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

### <span data-ttu-id="00f21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f21-117">-ResourceGroupName</span></span>
<span data-ttu-id="00f21-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00f21-118">The resource group name.</span></span>

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

### <span data-ttu-id="00f21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f21-119">CommonParameters</span></span>
<span data-ttu-id="00f21-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f21-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f21-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f21-122">입력</span><span class="sxs-lookup"><span data-stu-id="00f21-122">INPUTS</span></span>

### <span data-ttu-id="00f21-123">않아야</span><span class="sxs-lookup"><span data-stu-id="00f21-123">None</span></span>

## <span data-ttu-id="00f21-124">출력</span><span class="sxs-lookup"><span data-stu-id="00f21-124">OUTPUTS</span></span>

### <span data-ttu-id="00f21-125">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="00f21-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="00f21-126">상속자</span><span class="sxs-lookup"><span data-stu-id="00f21-126">NOTES</span></span>

## <span data-ttu-id="00f21-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00f21-127">RELATED LINKS</span></span>
