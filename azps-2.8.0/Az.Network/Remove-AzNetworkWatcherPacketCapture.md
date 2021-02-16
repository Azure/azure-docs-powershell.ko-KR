---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 35bd138a682eaca3b58ba82190961d3b7d7e3e26
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412183"
---
# <span data-ttu-id="1277f-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1277f-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="1277f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1277f-102">SYNOPSIS</span></span>
<span data-ttu-id="1277f-103">패킷 캡처 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="1277f-104">구문</span><span class="sxs-lookup"><span data-stu-id="1277f-104">SYNTAX</span></span>

### <span data-ttu-id="1277f-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="1277f-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1277f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1277f-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1277f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1277f-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1277f-108">설명</span><span class="sxs-lookup"><span data-stu-id="1277f-108">DESCRIPTION</span></span>
<span data-ttu-id="1277f-109">이 Remove-AzNetworkWatcherPacketCapture 캡처 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="1277f-110">Remove-AzNetworkWatcherPacketCapture를 Stop-AzNetworkWatcherPacketCapture 호출하기 전에 호출을 호출하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="1277f-111">패킷 캡처 세션이 실행 중일 때 Remove-AzNetworkWatcherPacketCapture 캡처가 저장되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="1277f-112">제거하기 전에 세션이 중지된 경우 캡처 데이터가 포함된 .cap 파일은 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="1277f-113">예제</span><span class="sxs-lookup"><span data-stu-id="1277f-113">EXAMPLES</span></span>

### <span data-ttu-id="1277f-114">예제 1: 패킷 캡처 세션 제거</span><span class="sxs-lookup"><span data-stu-id="1277f-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="1277f-115">이 예제에서는 "PacketCaptureTest"라는 기존 패킷 캡처 세션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="1277f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1277f-116">PARAMETERS</span></span>

### <span data-ttu-id="1277f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1277f-117">-AsJob</span></span>
<span data-ttu-id="1277f-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1277f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1277f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1277f-119">-DefaultProfile</span></span>
<span data-ttu-id="1277f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1277f-121">-Location</span><span class="sxs-lookup"><span data-stu-id="1277f-121">-Location</span></span>
<span data-ttu-id="1277f-122">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1277f-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1277f-123">-NetworkWatcher</span></span>
<span data-ttu-id="1277f-124">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-124">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1277f-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1277f-125">-NetworkWatcherName</span></span>
<span data-ttu-id="1277f-126">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-126">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1277f-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="1277f-127">-PacketCaptureName</span></span>
<span data-ttu-id="1277f-128">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-128">The packet capture name.</span></span>

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

### <span data-ttu-id="1277f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1277f-129">-PassThru</span></span>
<span data-ttu-id="1277f-130">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-130">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1277f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1277f-131">-ResourceGroupName</span></span>
<span data-ttu-id="1277f-132">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-132">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1277f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1277f-133">-Confirm</span></span>
<span data-ttu-id="1277f-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1277f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1277f-135">-WhatIf</span></span>
<span data-ttu-id="1277f-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1277f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1277f-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1277f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1277f-138">CommonParameters</span></span>
<span data-ttu-id="1277f-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1277f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1277f-140">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1277f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1277f-141">입력</span><span class="sxs-lookup"><span data-stu-id="1277f-141">INPUTS</span></span>

### <span data-ttu-id="1277f-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1277f-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1277f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1277f-143">System.String</span></span>

## <span data-ttu-id="1277f-144">출력</span><span class="sxs-lookup"><span data-stu-id="1277f-144">OUTPUTS</span></span>

### <span data-ttu-id="1277f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1277f-145">System.Boolean</span></span>

## <span data-ttu-id="1277f-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1277f-146">NOTES</span></span>
<span data-ttu-id="1277f-147">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽, 제거</span><span class="sxs-lookup"><span data-stu-id="1277f-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="1277f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1277f-148">RELATED LINKS</span></span>

[<span data-ttu-id="1277f-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1277f-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1277f-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1277f-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1277f-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1277f-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1277f-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1277f-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1277f-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1277f-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1277f-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1277f-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1277f-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1277f-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1277f-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1277f-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1277f-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1277f-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1277f-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1277f-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1277f-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1277f-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1277f-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1277f-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1277f-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1277f-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1277f-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1277f-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1277f-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1277f-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1277f-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1277f-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1277f-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1277f-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1277f-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1277f-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1277f-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1277f-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1277f-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1277f-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1277f-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1277f-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1277f-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1277f-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1277f-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1277f-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1277f-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1277f-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1277f-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1277f-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1277f-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1277f-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1277f-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1277f-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
