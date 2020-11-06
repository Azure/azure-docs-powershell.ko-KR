---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: fc78481ceeec796fe4a498bf76092955adb1639a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531375"
---
# <span data-ttu-id="3d42f-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d42f-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="3d42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d42f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d42f-103">실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d42f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d42f-104">SYNTAX</span></span>

### <span data-ttu-id="3d42f-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d42f-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d42f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3d42f-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d42f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3d42f-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d42f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3d42f-108">DESCRIPTION</span></span>
<span data-ttu-id="3d42f-109">Stop-AzureRmNetworkWatcherPacketCapture 실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-109">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="3d42f-110">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="3d42f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3d42f-111">EXAMPLES</span></span>

### <span data-ttu-id="3d42f-112">예제 1: 패킷 캡처 세션 중지</span><span class="sxs-lookup"><span data-stu-id="3d42f-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="3d42f-113">이 예제에서는 "PacketCaptureTest" 라는 실행 되는 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="3d42f-114">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="3d42f-115">변수</span><span class="sxs-lookup"><span data-stu-id="3d42f-115">PARAMETERS</span></span>

### <span data-ttu-id="3d42f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d42f-116">-AsJob</span></span>
<span data-ttu-id="3d42f-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3d42f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d42f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d42f-118">-DefaultProfile</span></span>
<span data-ttu-id="3d42f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d42f-120">-위치</span><span class="sxs-lookup"><span data-stu-id="3d42f-120">-Location</span></span>
<span data-ttu-id="3d42f-121">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3d42f-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d42f-122">-NetworkWatcher</span></span>
<span data-ttu-id="3d42f-123">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="3d42f-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="3d42f-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3d42f-124">-NetworkWatcherName</span></span>
<span data-ttu-id="3d42f-125">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="3d42f-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="3d42f-126">-PacketCaptureName</span></span>
<span data-ttu-id="3d42f-127">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-127">The packet capture name.</span></span>

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

### <span data-ttu-id="3d42f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d42f-128">-PassThru</span></span>
<span data-ttu-id="3d42f-129">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="3d42f-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3d42f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d42f-130">-ResourceGroupName</span></span>
<span data-ttu-id="3d42f-131">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3d42f-132">-확인</span><span class="sxs-lookup"><span data-stu-id="3d42f-132">-Confirm</span></span>
<span data-ttu-id="3d42f-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d42f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d42f-134">-WhatIf</span></span>
<span data-ttu-id="3d42f-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d42f-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d42f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d42f-137">CommonParameters</span></span>
<span data-ttu-id="3d42f-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d42f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d42f-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d42f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d42f-140">입력</span><span class="sxs-lookup"><span data-stu-id="3d42f-140">INPUTS</span></span>

### <span data-ttu-id="3d42f-141">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d42f-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3d42f-142">매개 변수: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3d42f-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="3d42f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d42f-143">System.String</span></span>
<span data-ttu-id="3d42f-144">매개 변수: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3d42f-144">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="3d42f-145">출력</span><span class="sxs-lookup"><span data-stu-id="3d42f-145">OUTPUTS</span></span>

### <span data-ttu-id="3d42f-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3d42f-146">System.Boolean</span></span>

## <span data-ttu-id="3d42f-147">상속자</span><span class="sxs-lookup"><span data-stu-id="3d42f-147">NOTES</span></span>
<span data-ttu-id="3d42f-148">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="3d42f-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="3d42f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d42f-149">RELATED LINKS</span></span>

[<span data-ttu-id="3d42f-150">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d42f-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d42f-151">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3d42f-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="3d42f-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d42f-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d42f-153">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d42f-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d42f-154">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d42f-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3d42f-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d42f-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3d42f-156">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d42f-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3d42f-157">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3d42f-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="3d42f-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3d42f-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="3d42f-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3d42f-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3d42f-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3d42f-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="3d42f-161">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3d42f-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3d42f-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3d42f-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3d42f-163">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d42f-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d42f-164">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d42f-164">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3d42f-165">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3d42f-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="3d42f-166">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d42f-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d42f-167">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d42f-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d42f-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d42f-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d42f-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3d42f-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3d42f-170">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d42f-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d42f-171">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d42f-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d42f-172">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3d42f-172">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3d42f-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3d42f-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3d42f-174">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3d42f-174">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3d42f-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3d42f-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="3d42f-176">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d42f-176">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
