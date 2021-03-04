---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 430292ba3a387a0b2a0285b26c147c375f114398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979776"
---
# <span data-ttu-id="0ca43-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="0ca43-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="0ca43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ca43-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca43-103">Azure RouteServer에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="0ca43-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="0ca43-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ca43-104">SYNTAX</span></span>

### <span data-ttu-id="0ca43-105">RouteServerNPeerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ca43-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca43-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca43-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ca43-107">설명</span><span class="sxs-lookup"><span data-stu-id="0ca43-107">DESCRIPTION</span></span>
<span data-ttu-id="0ca43-108">**Add-AzRouteServerPeer** cmdlet은 RouteServer 피어를 Azure RouteServer에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="0ca43-109">예제</span><span class="sxs-lookup"><span data-stu-id="0ca43-109">EXAMPLES</span></span>

### <span data-ttu-id="0ca43-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ca43-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="0ca43-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ca43-111">PARAMETERS</span></span>

### <span data-ttu-id="0ca43-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ca43-112">-AsJob</span></span>
<span data-ttu-id="0ca43-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0ca43-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ca43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca43-114">-DefaultProfile</span></span>
<span data-ttu-id="0ca43-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ca43-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0ca43-116">-Force</span></span>
<span data-ttu-id="0ca43-117">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0ca43-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="0ca43-118">-PeerAsn</span></span>
<span data-ttu-id="0ca43-119">원격 경로 서버 피어의 ASN입니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-119">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca43-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="0ca43-120">-PeerIp</span></span>
<span data-ttu-id="0ca43-121">원격 경로 서버 피어의 IP입니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="0ca43-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="0ca43-122">-PeerName</span></span>
<span data-ttu-id="0ca43-123">경로 서버 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-123">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca43-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ca43-125">경로 서버/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="0ca43-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="0ca43-126">-RouteServerName</span></span>
<span data-ttu-id="0ca43-127">피어가 있는 경로 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-127">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca43-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0ca43-128">-Confirm</span></span>
<span data-ttu-id="0ca43-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca43-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca43-130">-WhatIf</span></span>
<span data-ttu-id="0ca43-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ca43-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ca43-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca43-133">CommonParameters</span></span>
<span data-ttu-id="0ca43-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca43-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca43-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ca43-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca43-136">입력</span><span class="sxs-lookup"><span data-stu-id="0ca43-136">INPUTS</span></span>

### <span data-ttu-id="0ca43-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0ca43-137">System.String</span></span>

### <span data-ttu-id="0ca43-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="0ca43-138">System.UInt32</span></span>

## <span data-ttu-id="0ca43-139">출력</span><span class="sxs-lookup"><span data-stu-id="0ca43-139">OUTPUTS</span></span>

### <span data-ttu-id="0ca43-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="0ca43-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="0ca43-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ca43-141">NOTES</span></span>

## <span data-ttu-id="0ca43-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ca43-142">RELATED LINKS</span></span>
