---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1a28b061b10dc28fd5ecc0fe20cd817d7d1699b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872082"
---
# <span data-ttu-id="6633f-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6633f-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="6633f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6633f-102">SYNOPSIS</span></span>
<span data-ttu-id="6633f-103">실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="6633f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6633f-104">SYNTAX</span></span>

### <span data-ttu-id="6633f-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="6633f-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6633f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6633f-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6633f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6633f-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6633f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6633f-108">DESCRIPTION</span></span>
<span data-ttu-id="6633f-109">Stop-AzNetworkWatcherPacketCapture 실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="6633f-110">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="6633f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6633f-111">EXAMPLES</span></span>

### <span data-ttu-id="6633f-112">예제 1: 패킷 캡처 세션 중지</span><span class="sxs-lookup"><span data-stu-id="6633f-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="6633f-113">이 예제에서는 "PacketCaptureTest" 라는 실행 되는 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="6633f-114">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="6633f-115">변수</span><span class="sxs-lookup"><span data-stu-id="6633f-115">PARAMETERS</span></span>

### <span data-ttu-id="6633f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6633f-116">-AsJob</span></span>
<span data-ttu-id="6633f-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6633f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6633f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6633f-118">-DefaultProfile</span></span>
<span data-ttu-id="6633f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6633f-120">-위치</span><span class="sxs-lookup"><span data-stu-id="6633f-120">-Location</span></span>
<span data-ttu-id="6633f-121">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6633f-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6633f-122">-NetworkWatcher</span></span>
<span data-ttu-id="6633f-123">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="6633f-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="6633f-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6633f-124">-NetworkWatcherName</span></span>
<span data-ttu-id="6633f-125">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="6633f-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="6633f-126">-PacketCaptureName</span></span>
<span data-ttu-id="6633f-127">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-127">The packet capture name.</span></span>

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

### <span data-ttu-id="6633f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6633f-128">-PassThru</span></span>
<span data-ttu-id="6633f-129">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="6633f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6633f-130">-ResourceGroupName</span></span>
<span data-ttu-id="6633f-131">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6633f-132">-확인</span><span class="sxs-lookup"><span data-stu-id="6633f-132">-Confirm</span></span>
<span data-ttu-id="6633f-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6633f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6633f-134">-WhatIf</span></span>
<span data-ttu-id="6633f-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6633f-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6633f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6633f-137">CommonParameters</span></span>
<span data-ttu-id="6633f-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6633f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6633f-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6633f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6633f-140">입력</span><span class="sxs-lookup"><span data-stu-id="6633f-140">INPUTS</span></span>

### <span data-ttu-id="6633f-141">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6633f-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6633f-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6633f-142">System.String</span></span>

## <span data-ttu-id="6633f-143">출력</span><span class="sxs-lookup"><span data-stu-id="6633f-143">OUTPUTS</span></span>

### <span data-ttu-id="6633f-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6633f-144">System.Boolean</span></span>

## <span data-ttu-id="6633f-145">상속자</span><span class="sxs-lookup"><span data-stu-id="6633f-145">NOTES</span></span>
<span data-ttu-id="6633f-146">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="6633f-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="6633f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6633f-147">RELATED LINKS</span></span>

[<span data-ttu-id="6633f-148">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6633f-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6633f-149">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6633f-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6633f-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6633f-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6633f-151">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6633f-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6633f-152">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6633f-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6633f-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6633f-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6633f-154">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6633f-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6633f-155">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6633f-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6633f-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6633f-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6633f-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6633f-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6633f-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6633f-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6633f-159">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6633f-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6633f-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6633f-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6633f-161">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6633f-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6633f-162">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6633f-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6633f-163">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6633f-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6633f-164">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6633f-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6633f-165">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6633f-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6633f-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6633f-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6633f-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6633f-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6633f-168">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6633f-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6633f-169">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6633f-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6633f-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6633f-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6633f-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6633f-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6633f-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6633f-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6633f-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6633f-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="6633f-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6633f-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
