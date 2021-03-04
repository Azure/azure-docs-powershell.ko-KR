---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: a948dc37f778ff7a44a9e1478cfe138f2fefb113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954400"
---
# <span data-ttu-id="f9e7c-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f9e7c-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="f9e7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e7c-103">VM에서 다음 홉을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="f9e7c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9e7c-104">SYNTAX</span></span>

### <span data-ttu-id="f9e7c-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9e7c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9e7c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f9e7c-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9e7c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f9e7c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9e7c-108">설명</span><span class="sxs-lookup"><span data-stu-id="f9e7c-108">DESCRIPTION</span></span>
<span data-ttu-id="f9e7c-109">Get-AzNetworkWatcherNextHop cmdlet은 VM에서 다음 홉을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="f9e7c-110">다음 홉을 사용하면 Azure 리소스의 유형, 해당 리소스의 연결된 IP 주소 및 경로를 담당하는 라우팅 테이블 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="f9e7c-111">예제</span><span class="sxs-lookup"><span data-stu-id="f9e7c-111">EXAMPLES</span></span>

### <span data-ttu-id="f9e7c-112">예제 1: 인터넷 IP와 통신할 때 다음 홉을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="f9e7c-113">지정된 Virtual Machine의 기본 네트워크 인터페이스에서 204.79.197.200(www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="f9e7c-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="f9e7c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9e7c-114">PARAMETERS</span></span>

### <span data-ttu-id="f9e7c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9e7c-115">-AsJob</span></span>
<span data-ttu-id="f9e7c-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f9e7c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9e7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e7c-117">-DefaultProfile</span></span>
<span data-ttu-id="f9e7c-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9e7c-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="f9e7c-119">-DestinationIPAddress</span></span>
<span data-ttu-id="f9e7c-120">대상 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-120">Destination IP address.</span></span>

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

### <span data-ttu-id="f9e7c-121">-Location</span><span class="sxs-lookup"><span data-stu-id="f9e7c-121">-Location</span></span>
<span data-ttu-id="f9e7c-122">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f9e7c-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f9e7c-123">-NetworkWatcher</span></span>
<span data-ttu-id="f9e7c-124">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="f9e7c-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f9e7c-125">-NetworkWatcherName</span></span>
<span data-ttu-id="f9e7c-126">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="f9e7c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e7c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9e7c-128">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f9e7c-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="f9e7c-129">-SourceIPAddress</span></span>
<span data-ttu-id="f9e7c-130">원본 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-130">Source IP address.</span></span>

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

### <span data-ttu-id="f9e7c-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="f9e7c-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f9e7c-132">대상 네트워크 인터페이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="f9e7c-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f9e7c-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f9e7c-134">대상 가상 머신 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f9e7c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e7c-135">CommonParameters</span></span>
<span data-ttu-id="f9e7c-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9e7c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e7c-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9e7c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e7c-138">입력</span><span class="sxs-lookup"><span data-stu-id="f9e7c-138">INPUTS</span></span>

### <span data-ttu-id="f9e7c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f9e7c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f9e7c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f9e7c-140">System.String</span></span>

## <span data-ttu-id="f9e7c-141">출력</span><span class="sxs-lookup"><span data-stu-id="f9e7c-141">OUTPUTS</span></span>

### <span data-ttu-id="f9e7c-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="f9e7c-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="f9e7c-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9e7c-143">NOTES</span></span>
<span data-ttu-id="f9e7c-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 다음, 홉</span><span class="sxs-lookup"><span data-stu-id="f9e7c-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="f9e7c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9e7c-145">RELATED LINKS</span></span>

[<span data-ttu-id="f9e7c-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f9e7c-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f9e7c-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f9e7c-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f9e7c-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f9e7c-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f9e7c-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f9e7c-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f9e7c-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f9e7c-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f9e7c-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f9e7c-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f9e7c-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f9e7c-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f9e7c-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f9e7c-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f9e7c-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f9e7c-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f9e7c-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f9e7c-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f9e7c-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f9e7c-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f9e7c-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f9e7c-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f9e7c-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e7c-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f9e7c-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f9e7c-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f9e7c-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f9e7c-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f9e7c-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f9e7c-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f9e7c-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f9e7c-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f9e7c-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f9e7c-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f9e7c-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f9e7c-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f9e7c-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f9e7c-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f9e7c-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f9e7c-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f9e7c-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f9e7c-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f9e7c-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f9e7c-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f9e7c-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f9e7c-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f9e7c-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f9e7c-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f9e7c-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f9e7c-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f9e7c-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f9e7c-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
