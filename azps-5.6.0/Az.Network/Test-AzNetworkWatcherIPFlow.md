---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 8be10fd630bbc9d4e1952150728d144b5f552fe6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951728"
---
# <span data-ttu-id="e2d97-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e2d97-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="e2d97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2d97-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d97-103">패킷을 허용하거나 특정 대상에서 또는 거부할지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="e2d97-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2d97-104">SYNTAX</span></span>

### <span data-ttu-id="e2d97-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2d97-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d97-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e2d97-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d97-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e2d97-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2d97-108">설명</span><span class="sxs-lookup"><span data-stu-id="e2d97-108">DESCRIPTION</span></span>
<span data-ttu-id="e2d97-109">지정된 Test-AzNetworkWatcherIPFlow 및 로컬 및 원격, IP 주소 및 포트를 사용하여 지정된 방향이 있는 패킷의 경우 cmdlet은 패킷이 허용되거나 거부될지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="e2d97-110">예제</span><span class="sxs-lookup"><span data-stu-id="e2d97-110">EXAMPLES</span></span>

### <span data-ttu-id="e2d97-111">예제 1: 실행 Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e2d97-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="e2d97-112">이 구독에 대해 미국 중서부에 있는 Network Watcher를 을인 다음 VM을 얻게 하여 연결된 네트워크 인터페이스입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="e2d97-113">그런 다음 첫 번째 네트워크 인터페이스의 경우 Test-AzNetworkWatcherIPFlow 첫 번째 네트워크 인터페이스의 첫 번째 IP를 사용하여 인터넷의 IP에 대한 아웃바운드 연결을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="e2d97-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2d97-114">PARAMETERS</span></span>

### <span data-ttu-id="e2d97-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2d97-115">-AsJob</span></span>
<span data-ttu-id="e2d97-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e2d97-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2d97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d97-117">-DefaultProfile</span></span>
<span data-ttu-id="e2d97-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2d97-119">-방향</span><span class="sxs-lookup"><span data-stu-id="e2d97-119">-Direction</span></span>
<span data-ttu-id="e2d97-120">방향입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d97-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="e2d97-121">-LocalIPAddress</span></span>
<span data-ttu-id="e2d97-122">로컬 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-122">Local IP Address.</span></span>

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

### <span data-ttu-id="e2d97-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="e2d97-123">-LocalPort</span></span>
<span data-ttu-id="e2d97-124">로컬 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-124">Local Port.</span></span>

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

### <span data-ttu-id="e2d97-125">-Location</span><span class="sxs-lookup"><span data-stu-id="e2d97-125">-Location</span></span>
<span data-ttu-id="e2d97-126">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e2d97-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2d97-127">-NetworkWatcher</span></span>
<span data-ttu-id="e2d97-128">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="e2d97-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e2d97-129">-NetworkWatcherName</span></span>
<span data-ttu-id="e2d97-130">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="e2d97-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e2d97-131">-Protocol</span></span>
<span data-ttu-id="e2d97-132">프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d97-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="e2d97-133">-RemoteIPAddress</span></span>
<span data-ttu-id="e2d97-134">원격 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="e2d97-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="e2d97-135">-RemotePort</span></span>
<span data-ttu-id="e2d97-136">원격 포트.</span><span class="sxs-lookup"><span data-stu-id="e2d97-136">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d97-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d97-137">-ResourceGroupName</span></span>
<span data-ttu-id="e2d97-138">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e2d97-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="e2d97-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="e2d97-140">대상 네트워크 인터페이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-140">Target network interface Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d97-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e2d97-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="e2d97-142">대상 가상 머신 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="e2d97-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d97-143">CommonParameters</span></span>
<span data-ttu-id="e2d97-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d97-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d97-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e2d97-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d97-146">입력</span><span class="sxs-lookup"><span data-stu-id="e2d97-146">INPUTS</span></span>

### <span data-ttu-id="e2d97-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2d97-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e2d97-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e2d97-148">System.String</span></span>

## <span data-ttu-id="e2d97-149">출력</span><span class="sxs-lookup"><span data-stu-id="e2d97-149">OUTPUTS</span></span>

### <span data-ttu-id="e2d97-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="e2d97-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="e2d97-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2d97-151">NOTES</span></span>
<span data-ttu-id="e2d97-152">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, IP</span><span class="sxs-lookup"><span data-stu-id="e2d97-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="e2d97-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2d97-153">RELATED LINKS</span></span>

[<span data-ttu-id="e2d97-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2d97-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e2d97-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2d97-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e2d97-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2d97-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e2d97-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e2d97-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e2d97-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e2d97-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e2d97-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e2d97-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e2d97-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e2d97-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e2d97-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2d97-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2d97-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e2d97-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e2d97-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2d97-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2d97-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2d97-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2d97-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2d97-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2d97-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2d97-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e2d97-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e2d97-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e2d97-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e2d97-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e2d97-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2d97-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2d97-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2d97-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2d97-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2d97-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2d97-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e2d97-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e2d97-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2d97-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2d97-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2d97-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2d97-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e2d97-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e2d97-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e2d97-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e2d97-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e2d97-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e2d97-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e2d97-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e2d97-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e2d97-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e2d97-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2d97-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
