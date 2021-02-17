---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: d177c0dfa5ff59fde0adfe8ac4e3598ae70127f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202536"
---
# <span data-ttu-id="445ac-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="445ac-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="445ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="445ac-102">SYNOPSIS</span></span>
<span data-ttu-id="445ac-103">Azure RouteServer에서 피어를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="445ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="445ac-104">SYNTAX</span></span>

### <span data-ttu-id="445ac-105">RouteServerNPeerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="445ac-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="445ac-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="445ac-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="445ac-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="445ac-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="445ac-108">설명</span><span class="sxs-lookup"><span data-stu-id="445ac-108">DESCRIPTION</span></span>
<span data-ttu-id="445ac-109">**Remove-AzRouteServerPeer** cmdlet은 Azure RouteServer에서 RouteServer 피어를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="445ac-110">예제</span><span class="sxs-lookup"><span data-stu-id="445ac-110">EXAMPLES</span></span>

### <span data-ttu-id="445ac-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="445ac-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="445ac-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="445ac-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="445ac-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="445ac-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="445ac-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="445ac-114">PARAMETERS</span></span>

### <span data-ttu-id="445ac-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="445ac-115">-AsJob</span></span>
<span data-ttu-id="445ac-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="445ac-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445ac-117">-DefaultProfile</span></span>
<span data-ttu-id="445ac-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="445ac-119">-Force</span><span class="sxs-lookup"><span data-stu-id="445ac-119">-Force</span></span>
<span data-ttu-id="445ac-120">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445ac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="445ac-121">-InputObject</span></span>
<span data-ttu-id="445ac-122">경로 서버 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-122">The route server peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer
Parameter Sets: RouteServerNPeerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445ac-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="445ac-123">-PeerName</span></span>
<span data-ttu-id="445ac-124">경로 서버 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-124">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="445ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="445ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="445ac-126">경로 서버/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-126">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="445ac-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="445ac-127">-ResourceId</span></span>
<span data-ttu-id="445ac-128">경로 서버 피어 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-128">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="445ac-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="445ac-129">-RouteServerName</span></span>
<span data-ttu-id="445ac-130">피어가 있는 경로 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-130">The route server where peer exists.</span></span>

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

### <span data-ttu-id="445ac-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="445ac-131">-Confirm</span></span>
<span data-ttu-id="445ac-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445ac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445ac-133">-WhatIf</span></span>
<span data-ttu-id="445ac-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="445ac-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445ac-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445ac-136">CommonParameters</span></span>
<span data-ttu-id="445ac-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="445ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445ac-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="445ac-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445ac-139">입력</span><span class="sxs-lookup"><span data-stu-id="445ac-139">INPUTS</span></span>

### <span data-ttu-id="445ac-140">System.String</span><span class="sxs-lookup"><span data-stu-id="445ac-140">System.String</span></span>

### <span data-ttu-id="445ac-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="445ac-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="445ac-142">출력</span><span class="sxs-lookup"><span data-stu-id="445ac-142">OUTPUTS</span></span>

### <span data-ttu-id="445ac-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="445ac-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="445ac-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="445ac-144">NOTES</span></span>

## <span data-ttu-id="445ac-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="445ac-145">RELATED LINKS</span></span>
