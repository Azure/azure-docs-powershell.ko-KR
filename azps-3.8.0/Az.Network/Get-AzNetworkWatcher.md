---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: ea4eb4b7c6a8b88d78db809ee85ab0f484a9eba6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412608"
---
# <span data-ttu-id="68190-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68190-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="68190-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68190-102">SYNOPSIS</span></span>
<span data-ttu-id="68190-103">Network Watcher의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68190-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="68190-104">구문</span><span class="sxs-lookup"><span data-stu-id="68190-104">SYNTAX</span></span>

### <span data-ttu-id="68190-105">목록</span><span class="sxs-lookup"><span data-stu-id="68190-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68190-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="68190-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68190-107">설명</span><span class="sxs-lookup"><span data-stu-id="68190-107">DESCRIPTION</span></span>
<span data-ttu-id="68190-108">Get-AzNetworkWatcher cmdlet은 하나 이상의 Azure Network Watcher 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68190-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="68190-109">예제</span><span class="sxs-lookup"><span data-stu-id="68190-109">EXAMPLES</span></span>

### <span data-ttu-id="68190-110">예제 1: Network Watcher를 얻게</span><span class="sxs-lookup"><span data-stu-id="68190-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="68190-111">NetworkWatcherRG 리소스 NetworkWatcher_westcentralus 이름의 Network Watcher를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68190-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="68190-112">예제 2: 필터링을 사용하여 Network Watchers 나열</span><span class="sxs-lookup"><span data-stu-id="68190-112">Example 2: List Network Watchers using filtering</span></span>
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

<span data-ttu-id="68190-113">"NetworkWatcher"로 시작하는 Network Watcher를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68190-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="68190-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68190-114">PARAMETERS</span></span>

### <span data-ttu-id="68190-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68190-115">-DefaultProfile</span></span>
<span data-ttu-id="68190-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68190-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68190-117">-Location</span><span class="sxs-lookup"><span data-stu-id="68190-117">-Location</span></span>
<span data-ttu-id="68190-118">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="68190-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="68190-119">-Name</span><span class="sxs-lookup"><span data-stu-id="68190-119">-Name</span></span>
<span data-ttu-id="68190-120">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68190-120">The network watcher name.</span></span>

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

### <span data-ttu-id="68190-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68190-121">-ResourceGroupName</span></span>
<span data-ttu-id="68190-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68190-122">The resource group name.</span></span>

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

### <span data-ttu-id="68190-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68190-123">CommonParameters</span></span>
<span data-ttu-id="68190-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68190-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68190-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68190-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68190-126">입력</span><span class="sxs-lookup"><span data-stu-id="68190-126">INPUTS</span></span>

### <span data-ttu-id="68190-127">없음</span><span class="sxs-lookup"><span data-stu-id="68190-127">None</span></span>

## <span data-ttu-id="68190-128">출력</span><span class="sxs-lookup"><span data-stu-id="68190-128">OUTPUTS</span></span>

### <span data-ttu-id="68190-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68190-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="68190-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68190-130">NOTES</span></span>
<span data-ttu-id="68190-131">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="68190-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="68190-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68190-132">RELATED LINKS</span></span>

[<span data-ttu-id="68190-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68190-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="68190-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68190-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="68190-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68190-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="68190-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="68190-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="68190-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="68190-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="68190-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="68190-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="68190-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="68190-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="68190-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68190-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68190-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="68190-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="68190-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68190-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68190-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68190-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68190-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68190-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68190-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="68190-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="68190-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="68190-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="68190-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="68190-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="68190-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68190-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68190-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68190-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68190-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68190-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68190-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="68190-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="68190-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68190-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68190-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68190-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68190-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="68190-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="68190-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="68190-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="68190-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="68190-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="68190-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="68190-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="68190-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="68190-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="68190-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68190-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
