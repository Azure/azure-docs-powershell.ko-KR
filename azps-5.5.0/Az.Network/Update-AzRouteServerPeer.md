---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 79d907a5ac1b75bdc65d6ea79ffc6c9dea911479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193300"
---
# <span data-ttu-id="3fa3e-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="3fa3e-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="3fa3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fa3e-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa3e-103">Azure RouteServer에서 피어 업데이트</span><span class="sxs-lookup"><span data-stu-id="3fa3e-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="3fa3e-104">구문</span><span class="sxs-lookup"><span data-stu-id="3fa3e-104">SYNTAX</span></span>

### <span data-ttu-id="3fa3e-105">RouteServerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3fa3e-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa3e-106">RouteServerNPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fa3e-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fa3e-107">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fa3e-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa3e-108">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fa3e-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa3e-109">설명</span><span class="sxs-lookup"><span data-stu-id="3fa3e-109">DESCRIPTION</span></span>
<span data-ttu-id="3fa3e-110">**Update-AzRouteServerPeer** cmdlet은 RouteServer 피어를 Azure RouteServer로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="3fa3e-111">예제</span><span class="sxs-lookup"><span data-stu-id="3fa3e-111">EXAMPLES</span></span>

### <span data-ttu-id="3fa3e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3fa3e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="3fa3e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3fa3e-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="3fa3e-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="3fa3e-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="3fa3e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fa3e-115">PARAMETERS</span></span>

### <span data-ttu-id="3fa3e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fa3e-116">-AsJob</span></span>
<span data-ttu-id="3fa3e-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3fa3e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fa3e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa3e-118">-DefaultProfile</span></span>
<span data-ttu-id="3fa3e-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa3e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3fa3e-120">-Force</span></span>
<span data-ttu-id="3fa3e-121">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3fa3e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fa3e-122">-InputObject</span></span>
<span data-ttu-id="3fa3e-123">경로 서버 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="3fa3e-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="3fa3e-124">-PeerAsn</span></span>
<span data-ttu-id="3fa3e-125">원격 경로 서버 피어의 ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-125">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3e-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="3fa3e-126">-PeerIp</span></span>
<span data-ttu-id="3fa3e-127">원격 경로 서버 피어의 IP입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="3fa3e-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="3fa3e-128">-PeerName</span></span>
<span data-ttu-id="3fa3e-129">경로 서버 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="3fa3e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa3e-130">-ResourceGroupName</span></span>
<span data-ttu-id="3fa3e-131">경로 서버/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-131">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa3e-132">-ResourceId</span></span>
<span data-ttu-id="3fa3e-133">경로 서버 피어 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="3fa3e-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="3fa3e-134">-RouteServerName</span></span>
<span data-ttu-id="3fa3e-135">피어가 있는 경로 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-135">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fa3e-136">-Confirm</span></span>
<span data-ttu-id="3fa3e-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa3e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa3e-138">-WhatIf</span></span>
<span data-ttu-id="3fa3e-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3fa3e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa3e-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa3e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa3e-141">CommonParameters</span></span>
<span data-ttu-id="3fa3e-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa3e-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3fa3e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa3e-144">입력</span><span class="sxs-lookup"><span data-stu-id="3fa3e-144">INPUTS</span></span>

### <span data-ttu-id="3fa3e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3fa3e-145">System.String</span></span>

### <span data-ttu-id="3fa3e-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="3fa3e-146">System.UInt32</span></span>

### <span data-ttu-id="3fa3e-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="3fa3e-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="3fa3e-148">출력</span><span class="sxs-lookup"><span data-stu-id="3fa3e-148">OUTPUTS</span></span>

### <span data-ttu-id="3fa3e-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="3fa3e-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="3fa3e-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3fa3e-150">NOTES</span></span>

## <span data-ttu-id="3fa3e-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fa3e-151">RELATED LINKS</span></span>
