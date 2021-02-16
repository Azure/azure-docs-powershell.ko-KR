---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 048eeb08b820f5eccd76a74587d4949f1f9de110
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408409"
---
# <span data-ttu-id="d5073-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5073-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d5073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5073-102">SYNOPSIS</span></span>
<span data-ttu-id="d5073-103">실행 중인 패킷 캡처 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="d5073-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5073-104">SYNTAX</span></span>

### <span data-ttu-id="d5073-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="d5073-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5073-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d5073-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5073-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d5073-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5073-108">설명</span><span class="sxs-lookup"><span data-stu-id="d5073-108">DESCRIPTION</span></span>
<span data-ttu-id="d5073-109">이 Stop-AzNetworkWatcherPacketCapture 실행 중인 패킷 캡처 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="d5073-110">세션이 중지된 후 패킷 캡처 파일이 저장소에 업로드되고 구성에 따라 VM에 로컬로 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d5073-111">예제</span><span class="sxs-lookup"><span data-stu-id="d5073-111">EXAMPLES</span></span>

### <span data-ttu-id="d5073-112">예제 1: 패킷 캡처 세션 중지</span><span class="sxs-lookup"><span data-stu-id="d5073-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="d5073-113">이 예제에서는 "PacketCaptureTest"라는 실행 중인 패킷 캡처 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="d5073-114">세션이 중지된 후 패킷 캡처 파일이 저장소에 업로드되고 구성에 따라 VM에 로컬로 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="d5073-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5073-115">PARAMETERS</span></span>

### <span data-ttu-id="d5073-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5073-116">-AsJob</span></span>
<span data-ttu-id="d5073-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d5073-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5073-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5073-118">-DefaultProfile</span></span>
<span data-ttu-id="d5073-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5073-120">-Location</span><span class="sxs-lookup"><span data-stu-id="d5073-120">-Location</span></span>
<span data-ttu-id="d5073-121">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d5073-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5073-122">-NetworkWatcher</span></span>
<span data-ttu-id="d5073-123">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="d5073-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d5073-124">-NetworkWatcherName</span></span>
<span data-ttu-id="d5073-125">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="d5073-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d5073-126">-PacketCaptureName</span></span>
<span data-ttu-id="d5073-127">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-127">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5073-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5073-128">-PassThru</span></span>
<span data-ttu-id="d5073-129">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="d5073-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5073-130">-ResourceGroupName</span></span>
<span data-ttu-id="d5073-131">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d5073-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5073-132">-Confirm</span></span>
<span data-ttu-id="d5073-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5073-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5073-134">-WhatIf</span></span>
<span data-ttu-id="d5073-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d5073-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5073-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5073-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5073-137">CommonParameters</span></span>
<span data-ttu-id="d5073-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5073-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5073-139">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d5073-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5073-140">입력</span><span class="sxs-lookup"><span data-stu-id="d5073-140">INPUTS</span></span>

### <span data-ttu-id="d5073-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5073-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d5073-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d5073-142">System.String</span></span>

## <span data-ttu-id="d5073-143">출력</span><span class="sxs-lookup"><span data-stu-id="d5073-143">OUTPUTS</span></span>

### <span data-ttu-id="d5073-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5073-144">System.Boolean</span></span>

## <span data-ttu-id="d5073-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5073-145">NOTES</span></span>
<span data-ttu-id="d5073-146">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="d5073-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="d5073-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5073-147">RELATED LINKS</span></span>

[<span data-ttu-id="d5073-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5073-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5073-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d5073-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d5073-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5073-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5073-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5073-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5073-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5073-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d5073-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5073-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d5073-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d5073-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d5073-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d5073-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d5073-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d5073-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d5073-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d5073-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d5073-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d5073-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d5073-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d5073-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d5073-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d5073-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d5073-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d5073-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d5073-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5073-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d5073-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d5073-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d5073-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5073-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5073-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5073-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5073-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5073-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5073-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d5073-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d5073-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5073-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5073-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5073-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d5073-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d5073-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d5073-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d5073-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d5073-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d5073-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d5073-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d5073-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d5073-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d5073-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
