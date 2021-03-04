---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: 0d798c5eb70c8c472862e9af0f992d01827a750e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954075"
---
# <span data-ttu-id="13549-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="13549-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="13549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13549-102">SYNOPSIS</span></span>
<span data-ttu-id="13549-103">Azure RouteServer에서 RouteServer 피어를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13549-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="13549-104">구문</span><span class="sxs-lookup"><span data-stu-id="13549-104">SYNTAX</span></span>

### <span data-ttu-id="13549-105">RouteServerNPeerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="13549-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13549-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13549-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13549-107">설명</span><span class="sxs-lookup"><span data-stu-id="13549-107">DESCRIPTION</span></span>
<span data-ttu-id="13549-108">**Get-AzRouteServerPeer** cmdlet은 Azure RouteServer에서 피어를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13549-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="13549-109">예제</span><span class="sxs-lookup"><span data-stu-id="13549-109">EXAMPLES</span></span>

### <span data-ttu-id="13549-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="13549-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="13549-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="13549-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="13549-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="13549-112">PARAMETERS</span></span>

### <span data-ttu-id="13549-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13549-113">-DefaultProfile</span></span>
<span data-ttu-id="13549-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13549-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13549-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="13549-115">-PeerName</span></span>
<span data-ttu-id="13549-116">경로 서버 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13549-116">The name of the route server peer.</span></span>

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

### <span data-ttu-id="13549-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13549-117">-ResourceGroupName</span></span>
<span data-ttu-id="13549-118">경로 서버의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13549-118">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="13549-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13549-119">-ResourceId</span></span>
<span data-ttu-id="13549-120">경로 서버 피어의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="13549-120">ResourceId of the route server peer.</span></span>

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

### <span data-ttu-id="13549-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="13549-121">-RouteServerName</span></span>
<span data-ttu-id="13549-122">경로 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13549-122">The name of the route server.</span></span>

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

### <span data-ttu-id="13549-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13549-123">CommonParameters</span></span>
<span data-ttu-id="13549-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13549-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13549-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13549-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13549-126">입력</span><span class="sxs-lookup"><span data-stu-id="13549-126">INPUTS</span></span>

### <span data-ttu-id="13549-127">System.String</span><span class="sxs-lookup"><span data-stu-id="13549-127">System.String</span></span>

## <span data-ttu-id="13549-128">출력</span><span class="sxs-lookup"><span data-stu-id="13549-128">OUTPUTS</span></span>

### <span data-ttu-id="13549-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="13549-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="13549-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13549-130">NOTES</span></span>

## <span data-ttu-id="13549-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13549-131">RELATED LINKS</span></span>
