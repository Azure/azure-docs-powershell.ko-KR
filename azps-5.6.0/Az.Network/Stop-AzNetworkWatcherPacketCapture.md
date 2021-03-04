---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b0446488668b0473e387563983bb264f6c4078b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951840"
---
# <span data-ttu-id="50f0a-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50f0a-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="50f0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="50f0a-103">실행 중인 패킷 캡처 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="50f0a-104">구문</span><span class="sxs-lookup"><span data-stu-id="50f0a-104">SYNTAX</span></span>

### <span data-ttu-id="50f0a-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="50f0a-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f0a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="50f0a-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f0a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="50f0a-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50f0a-108">설명</span><span class="sxs-lookup"><span data-stu-id="50f0a-108">DESCRIPTION</span></span>
<span data-ttu-id="50f0a-109">Stop-AzNetworkWatcherPacketCapture 패킷 캡처 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="50f0a-110">세션이 중지된 후 패킷 캡처 파일은 해당 구성에 따라 VM에 로컬로 저장 및/또는 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="50f0a-111">예제</span><span class="sxs-lookup"><span data-stu-id="50f0a-111">EXAMPLES</span></span>

### <span data-ttu-id="50f0a-112">예제 1: 패킷 캡처 세션 중지</span><span class="sxs-lookup"><span data-stu-id="50f0a-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="50f0a-113">이 예제에서는 "PacketCaptureTest"라는 실행 중인 패킷 캡처 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="50f0a-114">세션이 중지된 후 패킷 캡처 파일은 해당 구성에 따라 VM에 로컬로 저장 및/또는 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="50f0a-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="50f0a-115">PARAMETERS</span></span>

### <span data-ttu-id="50f0a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50f0a-116">-AsJob</span></span>
<span data-ttu-id="50f0a-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="50f0a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50f0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f0a-118">-DefaultProfile</span></span>
<span data-ttu-id="50f0a-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50f0a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="50f0a-120">-Location</span></span>
<span data-ttu-id="50f0a-121">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="50f0a-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50f0a-122">-NetworkWatcher</span></span>
<span data-ttu-id="50f0a-123">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="50f0a-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="50f0a-124">-NetworkWatcherName</span></span>
<span data-ttu-id="50f0a-125">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="50f0a-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="50f0a-126">-PacketCaptureName</span></span>
<span data-ttu-id="50f0a-127">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-127">The packet capture name.</span></span>

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

### <span data-ttu-id="50f0a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50f0a-128">-PassThru</span></span>
<span data-ttu-id="50f0a-129">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="50f0a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f0a-130">-ResourceGroupName</span></span>
<span data-ttu-id="50f0a-131">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="50f0a-132">-확인</span><span class="sxs-lookup"><span data-stu-id="50f0a-132">-Confirm</span></span>
<span data-ttu-id="50f0a-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50f0a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50f0a-134">-WhatIf</span></span>
<span data-ttu-id="50f0a-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50f0a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50f0a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f0a-137">CommonParameters</span></span>
<span data-ttu-id="50f0a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50f0a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f0a-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="50f0a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f0a-140">입력</span><span class="sxs-lookup"><span data-stu-id="50f0a-140">INPUTS</span></span>

### <span data-ttu-id="50f0a-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50f0a-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="50f0a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="50f0a-142">System.String</span></span>

## <span data-ttu-id="50f0a-143">출력</span><span class="sxs-lookup"><span data-stu-id="50f0a-143">OUTPUTS</span></span>

### <span data-ttu-id="50f0a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="50f0a-144">System.Boolean</span></span>

## <span data-ttu-id="50f0a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50f0a-145">NOTES</span></span>
<span data-ttu-id="50f0a-146">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="50f0a-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="50f0a-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50f0a-147">RELATED LINKS</span></span>

[<span data-ttu-id="50f0a-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50f0a-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="50f0a-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="50f0a-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="50f0a-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50f0a-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="50f0a-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50f0a-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="50f0a-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50f0a-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="50f0a-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50f0a-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="50f0a-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="50f0a-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="50f0a-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="50f0a-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="50f0a-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="50f0a-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="50f0a-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="50f0a-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="50f0a-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="50f0a-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="50f0a-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="50f0a-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="50f0a-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="50f0a-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="50f0a-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50f0a-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="50f0a-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="50f0a-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="50f0a-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="50f0a-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="50f0a-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="50f0a-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="50f0a-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="50f0a-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="50f0a-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="50f0a-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="50f0a-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="50f0a-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="50f0a-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="50f0a-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="50f0a-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="50f0a-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="50f0a-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="50f0a-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="50f0a-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="50f0a-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="50f0a-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="50f0a-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="50f0a-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="50f0a-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="50f0a-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="50f0a-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
