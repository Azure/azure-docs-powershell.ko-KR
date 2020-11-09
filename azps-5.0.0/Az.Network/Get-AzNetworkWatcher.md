---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: dc8d3a3db0eaa76974e02a62111b022ed81524b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311474"
---
# <span data-ttu-id="58471-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58471-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="58471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58471-102">SYNOPSIS</span></span>
<span data-ttu-id="58471-103">네트워크 감시자의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58471-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="58471-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58471-104">SYNTAX</span></span>

### <span data-ttu-id="58471-105">목록</span><span class="sxs-lookup"><span data-stu-id="58471-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58471-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="58471-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58471-107">설명은</span><span class="sxs-lookup"><span data-stu-id="58471-107">DESCRIPTION</span></span>
<span data-ttu-id="58471-108">Get-AzNetworkWatcher cmdlet은 하나 이상의 Azure 네트워크 감시자 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58471-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="58471-109">예제의</span><span class="sxs-lookup"><span data-stu-id="58471-109">EXAMPLES</span></span>

### <span data-ttu-id="58471-110">예제 1: 네트워크 감시자 가져오기</span><span class="sxs-lookup"><span data-stu-id="58471-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="58471-111">리소스 그룹 NetworkWatcherRG의 NetworkWatcher_westcentralus 라는 네트워크 감시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58471-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="58471-112">예제 2: 필터링을 사용 하 여 네트워크 감시자 나열</span><span class="sxs-lookup"><span data-stu-id="58471-112">Example 2: List Network Watchers using filtering</span></span>
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

<span data-ttu-id="58471-113">"NetworkWatcher"로 시작 하는 네트워크 감시자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58471-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="58471-114">변수</span><span class="sxs-lookup"><span data-stu-id="58471-114">PARAMETERS</span></span>

### <span data-ttu-id="58471-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58471-115">-DefaultProfile</span></span>
<span data-ttu-id="58471-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58471-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58471-117">-위치</span><span class="sxs-lookup"><span data-stu-id="58471-117">-Location</span></span>
<span data-ttu-id="58471-118">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="58471-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="58471-119">-이름</span><span class="sxs-lookup"><span data-stu-id="58471-119">-Name</span></span>
<span data-ttu-id="58471-120">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58471-120">The network watcher name.</span></span>

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

### <span data-ttu-id="58471-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58471-121">-ResourceGroupName</span></span>
<span data-ttu-id="58471-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58471-122">The resource group name.</span></span>

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

### <span data-ttu-id="58471-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58471-123">CommonParameters</span></span>
<span data-ttu-id="58471-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58471-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58471-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58471-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58471-126">입력</span><span class="sxs-lookup"><span data-stu-id="58471-126">INPUTS</span></span>

### <span data-ttu-id="58471-127">않아야</span><span class="sxs-lookup"><span data-stu-id="58471-127">None</span></span>

## <span data-ttu-id="58471-128">출력</span><span class="sxs-lookup"><span data-stu-id="58471-128">OUTPUTS</span></span>

### <span data-ttu-id="58471-129">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58471-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="58471-130">상속자</span><span class="sxs-lookup"><span data-stu-id="58471-130">NOTES</span></span>
<span data-ttu-id="58471-131">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="58471-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="58471-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58471-132">RELATED LINKS</span></span>

[<span data-ttu-id="58471-133">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58471-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="58471-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58471-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="58471-135">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="58471-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="58471-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="58471-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="58471-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="58471-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="58471-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="58471-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="58471-139">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="58471-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="58471-140">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58471-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58471-141">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="58471-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="58471-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58471-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58471-143">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58471-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58471-144">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58471-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="58471-145">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="58471-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="58471-146">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="58471-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="58471-147">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="58471-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="58471-148">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58471-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58471-149">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58471-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58471-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58471-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58471-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="58471-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="58471-152">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58471-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58471-153">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58471-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="58471-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="58471-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="58471-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="58471-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="58471-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="58471-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="58471-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="58471-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="58471-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="58471-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="58471-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="58471-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
