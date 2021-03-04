---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: da74734284d3e103b887215f5c25c26214b38f49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954395"
---
# <span data-ttu-id="bcbbb-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcbbb-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="bcbbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbbb-103">패킷 캡처 리소스의 정보 및 속성 및 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="bcbbb-104">구문</span><span class="sxs-lookup"><span data-stu-id="bcbbb-104">SYNTAX</span></span>

### <span data-ttu-id="bcbbb-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="bcbbb-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbbb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bcbbb-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcbbb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bcbbb-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcbbb-108">설명</span><span class="sxs-lookup"><span data-stu-id="bcbbb-108">DESCRIPTION</span></span>
<span data-ttu-id="bcbbb-109">Get-AzNetworkWatcherPacketCapture 캡처 리소스의 속성 및 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="bcbbb-110">예제</span><span class="sxs-lookup"><span data-stu-id="bcbbb-110">EXAMPLES</span></span>

### <span data-ttu-id="bcbbb-111">예제 1: 여러 필터를 사용하여 패킷 캡처 만들기 및 해당 상태를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="bcbbb-112">이 예제에서는 여러 필터와 시간 제한이 있는 "PacketCaptureTest"라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="bcbbb-113">세션이 완료되면 지정된 저장소 계정에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="bcbbb-114">그런 다음 Get-AzNetworkWatcherPacketCapture 세션의 상태를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="bcbbb-115">참고: 패킷 캡처를 만들기 위해 Azure Network Watcher 확장을 대상 가상 머신에 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="bcbbb-116">New-AzNetworkWatcherPacketCapture 명령에서 직접 패킷 캡처에 대한 참조를 만드는 경우 모든 속성이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="bcbbb-117">Get-AzNetworkWatcherPacketCapture 호출하여 패킷 캡처의 모든 속성을 얻을 Get-AzNetworkWatcherPacketCapture 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="bcbbb-118">예제 2: 여러 필터를 사용하여 패킷 캡처 만들기 및 해당 상태를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="bcbbb-119">이 cmdlet은 nw1 Network Watcher에서 "PacketCapture"로 시작하는 모든 패킷 캡처를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="bcbbb-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bcbbb-120">PARAMETERS</span></span>

### <span data-ttu-id="bcbbb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcbbb-121">-AsJob</span></span>
<span data-ttu-id="bcbbb-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bcbbb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcbbb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbbb-123">-DefaultProfile</span></span>
<span data-ttu-id="bcbbb-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcbbb-125">-Location</span><span class="sxs-lookup"><span data-stu-id="bcbbb-125">-Location</span></span>
<span data-ttu-id="bcbbb-126">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bcbbb-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcbbb-127">-NetworkWatcher</span></span>
<span data-ttu-id="bcbbb-128">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="bcbbb-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bcbbb-129">-NetworkWatcherName</span></span>
<span data-ttu-id="bcbbb-130">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="bcbbb-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="bcbbb-131">-PacketCaptureName</span></span>
<span data-ttu-id="bcbbb-132">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="bcbbb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbbb-133">-ResourceGroupName</span></span>
<span data-ttu-id="bcbbb-134">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bcbbb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbbb-135">CommonParameters</span></span>
<span data-ttu-id="bcbbb-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbbb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbbb-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcbbb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbbb-138">입력</span><span class="sxs-lookup"><span data-stu-id="bcbbb-138">INPUTS</span></span>

### <span data-ttu-id="bcbbb-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcbbb-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="bcbbb-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bcbbb-140">System.String</span></span>

## <span data-ttu-id="bcbbb-141">출력</span><span class="sxs-lookup"><span data-stu-id="bcbbb-141">OUTPUTS</span></span>

### <span data-ttu-id="bcbbb-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="bcbbb-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="bcbbb-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bcbbb-143">NOTES</span></span>
<span data-ttu-id="bcbbb-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="bcbbb-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="bcbbb-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcbbb-145">RELATED LINKS</span></span>

[<span data-ttu-id="bcbbb-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcbbb-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bcbbb-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcbbb-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bcbbb-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcbbb-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bcbbb-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bcbbb-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bcbbb-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bcbbb-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bcbbb-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bcbbb-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bcbbb-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bcbbb-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bcbbb-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcbbb-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bcbbb-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bcbbb-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bcbbb-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcbbb-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bcbbb-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcbbb-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bcbbb-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcbbb-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bcbbb-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bcbbb-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="bcbbb-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bcbbb-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bcbbb-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bcbbb-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="bcbbb-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcbbb-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bcbbb-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcbbb-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bcbbb-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcbbb-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bcbbb-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bcbbb-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="bcbbb-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcbbb-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bcbbb-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcbbb-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bcbbb-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bcbbb-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="bcbbb-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bcbbb-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="bcbbb-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bcbbb-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="bcbbb-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bcbbb-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bcbbb-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bcbbb-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="bcbbb-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcbbb-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

