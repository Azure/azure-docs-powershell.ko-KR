---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: d36a919adfbf1a7a2e2b7a10313433e820cc478a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184668"
---
# <span data-ttu-id="448ba-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="448ba-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="448ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="448ba-102">SYNOPSIS</span></span>
<span data-ttu-id="448ba-103">Azure RouteServer에서 RouteServer 피어를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="448ba-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="448ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="448ba-104">SYNTAX</span></span>

### <span data-ttu-id="448ba-105">RouteServerNPeerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="448ba-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="448ba-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="448ba-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="448ba-107">설명</span><span class="sxs-lookup"><span data-stu-id="448ba-107">DESCRIPTION</span></span>
<span data-ttu-id="448ba-108">**Get-AzRouteServerPeer** cmdlet은 Azure RouteServer에서 피어를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="448ba-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="448ba-109">예제</span><span class="sxs-lookup"><span data-stu-id="448ba-109">EXAMPLES</span></span>

### <span data-ttu-id="448ba-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="448ba-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="448ba-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="448ba-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="448ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="448ba-112">PARAMETERS</span></span>

### <span data-ttu-id="448ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448ba-113">-DefaultProfile</span></span>
<span data-ttu-id="448ba-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="448ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="448ba-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="448ba-115">-PeerName</span></span>
<span data-ttu-id="448ba-116">경로 서버 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="448ba-116">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="448ba-118">경로 서버의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="448ba-118">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448ba-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="448ba-119">-ResourceId</span></span>
<span data-ttu-id="448ba-120">경로 서버 피어의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="448ba-120">ResourceId of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448ba-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="448ba-121">-RouteServerName</span></span>
<span data-ttu-id="448ba-122">경로 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="448ba-122">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448ba-123">CommonParameters</span></span>
<span data-ttu-id="448ba-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="448ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448ba-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="448ba-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448ba-126">입력</span><span class="sxs-lookup"><span data-stu-id="448ba-126">INPUTS</span></span>

### <span data-ttu-id="448ba-127">System.String</span><span class="sxs-lookup"><span data-stu-id="448ba-127">System.String</span></span>

## <span data-ttu-id="448ba-128">출력</span><span class="sxs-lookup"><span data-stu-id="448ba-128">OUTPUTS</span></span>

### <span data-ttu-id="448ba-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="448ba-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="448ba-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="448ba-130">NOTES</span></span>

## <span data-ttu-id="448ba-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="448ba-131">RELATED LINKS</span></span>
