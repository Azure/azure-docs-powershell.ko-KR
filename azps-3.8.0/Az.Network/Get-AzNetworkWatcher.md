---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: c1ea29572bb42bea0c7e64c3ec818fe2f2d0ed0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878173"
---
# <span data-ttu-id="4a77b-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a77b-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="4a77b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a77b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a77b-103">네트워크 감시자의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="4a77b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a77b-104">SYNTAX</span></span>

### <span data-ttu-id="4a77b-105">목록</span><span class="sxs-lookup"><span data-stu-id="4a77b-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a77b-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4a77b-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a77b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4a77b-107">DESCRIPTION</span></span>
<span data-ttu-id="4a77b-108">Get-AzNetworkWatcher cmdlet은 하나 이상의 Azure 네트워크 감시자 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="4a77b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4a77b-109">EXAMPLES</span></span>

### <span data-ttu-id="4a77b-110">예제 1: 네트워크 감시자 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a77b-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="4a77b-111">리소스 그룹 NetworkWatcherRG의 NetworkWatcher_westcentralus 라는 네트워크 감시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="4a77b-112">예제 2: 필터링을 사용 하 여 네트워크 감시자 나열</span><span class="sxs-lookup"><span data-stu-id="4a77b-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="4a77b-113">"NetworkWatcher"로 시작 하는 네트워크 감시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="4a77b-114">변수</span><span class="sxs-lookup"><span data-stu-id="4a77b-114">PARAMETERS</span></span>

### <span data-ttu-id="4a77b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a77b-115">-DefaultProfile</span></span>
<span data-ttu-id="4a77b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a77b-117">-위치</span><span class="sxs-lookup"><span data-stu-id="4a77b-117">-Location</span></span>
<span data-ttu-id="4a77b-118">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-118">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a77b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4a77b-119">-Name</span></span>
<span data-ttu-id="4a77b-120">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4a77b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a77b-121">-ResourceGroupName</span></span>
<span data-ttu-id="4a77b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4a77b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a77b-123">CommonParameters</span></span>
<span data-ttu-id="4a77b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a77b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a77b-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a77b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a77b-126">입력</span><span class="sxs-lookup"><span data-stu-id="4a77b-126">INPUTS</span></span>

### <span data-ttu-id="4a77b-127">않아야</span><span class="sxs-lookup"><span data-stu-id="4a77b-127">None</span></span>

## <span data-ttu-id="4a77b-128">출력</span><span class="sxs-lookup"><span data-stu-id="4a77b-128">OUTPUTS</span></span>

### <span data-ttu-id="4a77b-129">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a77b-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="4a77b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4a77b-130">NOTES</span></span>
<span data-ttu-id="4a77b-131">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="4a77b-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="4a77b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a77b-132">RELATED LINKS</span></span>

[<span data-ttu-id="4a77b-133">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a77b-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4a77b-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a77b-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4a77b-135">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4a77b-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4a77b-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4a77b-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4a77b-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4a77b-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4a77b-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4a77b-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4a77b-139">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4a77b-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4a77b-140">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a77b-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a77b-141">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4a77b-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4a77b-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a77b-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a77b-143">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a77b-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a77b-144">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4a77b-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4a77b-145">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a77b-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4a77b-146">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4a77b-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4a77b-147">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4a77b-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4a77b-148">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a77b-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a77b-149">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a77b-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a77b-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a77b-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a77b-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4a77b-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4a77b-152">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a77b-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a77b-153">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a77b-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4a77b-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4a77b-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4a77b-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4a77b-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4a77b-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4a77b-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4a77b-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4a77b-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4a77b-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4a77b-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4a77b-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4a77b-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
