---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 05881e5248ecad95222d5e3e7148edbc8c1a1dea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033834"
---
# <span data-ttu-id="9db96-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9db96-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="9db96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9db96-102">SYNOPSIS</span></span>
<span data-ttu-id="9db96-103">VirtualHub 아래에 있는 기존 P2SVpnGateway를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9db96-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="9db96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9db96-104">SYNTAX</span></span>

### <span data-ttu-id="9db96-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="9db96-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9db96-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db96-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9db96-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9db96-107">DESCRIPTION</span></span>
<span data-ttu-id="9db96-108">**AzP2sVpnGateway** cmdlet을 사용 하면 virtualhub 아래에 기존 P2SVpnGateway를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9db96-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="9db96-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9db96-109">EXAMPLES</span></span>

### <span data-ttu-id="9db96-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9db96-110">Example 1</span></span>
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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="9db96-111">**AzP2sVpnGateway** cmdlet을 사용 하면 사이트 연결을 가리키는 데 사용 되는 virtualhub 아래에 있는 기존 P2SVpnGateway를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9db96-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="9db96-112">변수</span><span class="sxs-lookup"><span data-stu-id="9db96-112">PARAMETERS</span></span>

### <span data-ttu-id="9db96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db96-113">-DefaultProfile</span></span>
<span data-ttu-id="9db96-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9db96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9db96-115">-이름</span><span class="sxs-lookup"><span data-stu-id="9db96-115">-Name</span></span>
<span data-ttu-id="9db96-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9db96-116">The resource name.</span></span>

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

### <span data-ttu-id="9db96-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db96-117">-ResourceGroupName</span></span>
<span data-ttu-id="9db96-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9db96-118">The resource group name.</span></span>

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

### <span data-ttu-id="9db96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db96-119">CommonParameters</span></span>
<span data-ttu-id="9db96-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9db96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db96-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db96-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db96-122">입력</span><span class="sxs-lookup"><span data-stu-id="9db96-122">INPUTS</span></span>

### <span data-ttu-id="9db96-123">않아야</span><span class="sxs-lookup"><span data-stu-id="9db96-123">None</span></span>

## <span data-ttu-id="9db96-124">출력</span><span class="sxs-lookup"><span data-stu-id="9db96-124">OUTPUTS</span></span>

### <span data-ttu-id="9db96-125">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9db96-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="9db96-126">상속자</span><span class="sxs-lookup"><span data-stu-id="9db96-126">NOTES</span></span>

## <span data-ttu-id="9db96-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9db96-127">RELATED LINKS</span></span>
