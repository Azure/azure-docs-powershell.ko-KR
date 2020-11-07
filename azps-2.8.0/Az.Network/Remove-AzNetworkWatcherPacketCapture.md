---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d99b085f5137c9f18d4dda50fce0654954266f37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871201"
---
# <span data-ttu-id="34c26-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c26-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="34c26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34c26-102">SYNOPSIS</span></span>
<span data-ttu-id="34c26-103">패킷 캡처 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="34c26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34c26-104">SYNTAX</span></span>

### <span data-ttu-id="34c26-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="34c26-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c26-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="34c26-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c26-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="34c26-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34c26-108">설명은</span><span class="sxs-lookup"><span data-stu-id="34c26-108">DESCRIPTION</span></span>
<span data-ttu-id="34c26-109">Remove-AzNetworkWatcherPacketCapture는 패킷 캡처 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="34c26-110">Remove-AzNetworkWatcherPacketCapture를 호출 하기 전에 Stop-AzNetworkWatcherPacketCapture를 호출 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="34c26-111">Remove-AzNetworkWatcherPacketCapture를 호출할 때 패킷 캡처 세션을 실행 중인 경우 패킷 캡처는 저장 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="34c26-112">제거 하기 전에 세션이 중지 된 경우 캡처 데이터를 포함 하는 cap 파일은 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="34c26-113">예제의</span><span class="sxs-lookup"><span data-stu-id="34c26-113">EXAMPLES</span></span>

### <span data-ttu-id="34c26-114">예제 1: 패킷 캡처 세션 제거</span><span class="sxs-lookup"><span data-stu-id="34c26-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="34c26-115">이 예제에서는 "PacketCaptureTest" 이라는 기존 패킷 캡처 세션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="34c26-116">변수</span><span class="sxs-lookup"><span data-stu-id="34c26-116">PARAMETERS</span></span>

### <span data-ttu-id="34c26-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34c26-117">-AsJob</span></span>
<span data-ttu-id="34c26-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="34c26-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34c26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c26-119">-DefaultProfile</span></span>
<span data-ttu-id="34c26-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34c26-121">-위치</span><span class="sxs-lookup"><span data-stu-id="34c26-121">-Location</span></span>
<span data-ttu-id="34c26-122">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="34c26-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c26-123">-NetworkWatcher</span></span>
<span data-ttu-id="34c26-124">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="34c26-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="34c26-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="34c26-125">-NetworkWatcherName</span></span>
<span data-ttu-id="34c26-126">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="34c26-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="34c26-127">-PacketCaptureName</span></span>
<span data-ttu-id="34c26-128">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-128">The packet capture name.</span></span>

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

### <span data-ttu-id="34c26-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34c26-129">-PassThru</span></span>
<span data-ttu-id="34c26-130">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="34c26-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34c26-131">-ResourceGroupName</span></span>
<span data-ttu-id="34c26-132">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="34c26-133">-확인</span><span class="sxs-lookup"><span data-stu-id="34c26-133">-Confirm</span></span>
<span data-ttu-id="34c26-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34c26-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c26-135">-WhatIf</span></span>
<span data-ttu-id="34c26-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34c26-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34c26-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c26-138">CommonParameters</span></span>
<span data-ttu-id="34c26-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34c26-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c26-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c26-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c26-141">입력</span><span class="sxs-lookup"><span data-stu-id="34c26-141">INPUTS</span></span>

### <span data-ttu-id="34c26-142">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c26-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="34c26-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34c26-143">System.String</span></span>

## <span data-ttu-id="34c26-144">출력</span><span class="sxs-lookup"><span data-stu-id="34c26-144">OUTPUTS</span></span>

### <span data-ttu-id="34c26-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="34c26-145">System.Boolean</span></span>

## <span data-ttu-id="34c26-146">상속자</span><span class="sxs-lookup"><span data-stu-id="34c26-146">NOTES</span></span>
<span data-ttu-id="34c26-147">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽, 제거</span><span class="sxs-lookup"><span data-stu-id="34c26-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="34c26-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34c26-148">RELATED LINKS</span></span>

[<span data-ttu-id="34c26-149">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c26-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="34c26-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c26-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="34c26-151">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="34c26-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="34c26-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="34c26-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="34c26-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="34c26-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="34c26-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="34c26-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="34c26-155">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="34c26-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="34c26-156">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c26-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34c26-157">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="34c26-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="34c26-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c26-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34c26-159">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c26-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34c26-160">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="34c26-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="34c26-161">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="34c26-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="34c26-162">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="34c26-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="34c26-163">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="34c26-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="34c26-164">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34c26-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34c26-165">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34c26-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34c26-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34c26-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34c26-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="34c26-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="34c26-168">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34c26-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34c26-169">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34c26-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="34c26-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="34c26-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="34c26-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="34c26-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="34c26-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="34c26-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="34c26-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="34c26-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="34c26-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="34c26-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="34c26-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="34c26-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
