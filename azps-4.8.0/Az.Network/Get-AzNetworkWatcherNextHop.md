---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: cf120e8e9ca9e0dad8f4d430c7f207d40fcfab3b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204538"
---
# <span data-ttu-id="e0a3b-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e0a3b-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="e0a3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e0a3b-103">VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="e0a3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0a3b-104">SYNTAX</span></span>

### <span data-ttu-id="e0a3b-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="e0a3b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0a3b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e0a3b-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0a3b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e0a3b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0a3b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e0a3b-108">DESCRIPTION</span></span>
<span data-ttu-id="e0a3b-109">Get-AzNetworkWatcherNextHop cmdlet은 VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="e0a3b-110">다음 홉을 사용 하면 Azure 리소스의 유형, 해당 리소스의 연결 된 IP 주소, 경로를 담당 하는 라우팅 테이블 규칙이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="e0a3b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e0a3b-111">EXAMPLES</span></span>

### <span data-ttu-id="e0a3b-112">예제 1: 인터넷 IP와 통신할 때 다음 홉 받기</span><span class="sxs-lookup"><span data-stu-id="e0a3b-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="e0a3b-113">지정 된 가상 머신 (www.bing.com)의 기본 네트워크 인터페이스에서 아웃 바운드 통신용 다음 홉을 가져옵니다. 204.79.197.200)</span><span class="sxs-lookup"><span data-stu-id="e0a3b-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="e0a3b-114">변수</span><span class="sxs-lookup"><span data-stu-id="e0a3b-114">PARAMETERS</span></span>

### <span data-ttu-id="e0a3b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0a3b-115">-AsJob</span></span>
<span data-ttu-id="e0a3b-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e0a3b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0a3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0a3b-117">-DefaultProfile</span></span>
<span data-ttu-id="e0a3b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0a3b-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="e0a3b-119">-DestinationIPAddress</span></span>
<span data-ttu-id="e0a3b-120">대상 IP 주소</span><span class="sxs-lookup"><span data-stu-id="e0a3b-120">Destination IP address.</span></span>

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

### <span data-ttu-id="e0a3b-121">-위치</span><span class="sxs-lookup"><span data-stu-id="e0a3b-121">-Location</span></span>
<span data-ttu-id="e0a3b-122">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e0a3b-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0a3b-123">-NetworkWatcher</span></span>
<span data-ttu-id="e0a3b-124">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="e0a3b-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e0a3b-125">-NetworkWatcherName</span></span>
<span data-ttu-id="e0a3b-126">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="e0a3b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0a3b-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0a3b-128">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e0a3b-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="e0a3b-129">-SourceIPAddress</span></span>
<span data-ttu-id="e0a3b-130">원본 IP 주소</span><span class="sxs-lookup"><span data-stu-id="e0a3b-130">Source IP address.</span></span>

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

### <span data-ttu-id="e0a3b-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="e0a3b-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="e0a3b-132">대상 네트워크 인터페이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="e0a3b-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e0a3b-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="e0a3b-134">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="e0a3b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0a3b-135">CommonParameters</span></span>
<span data-ttu-id="e0a3b-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0a3b-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0a3b-138">입력</span><span class="sxs-lookup"><span data-stu-id="e0a3b-138">INPUTS</span></span>

### <span data-ttu-id="e0a3b-139">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0a3b-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e0a3b-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e0a3b-140">System.String</span></span>

## <span data-ttu-id="e0a3b-141">출력</span><span class="sxs-lookup"><span data-stu-id="e0a3b-141">OUTPUTS</span></span>

### <span data-ttu-id="e0a3b-142">PSNextHopResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e0a3b-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="e0a3b-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e0a3b-143">NOTES</span></span>
<span data-ttu-id="e0a3b-144">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="e0a3b-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="e0a3b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0a3b-145">RELATED LINKS</span></span>

[<span data-ttu-id="e0a3b-146">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0a3b-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e0a3b-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0a3b-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e0a3b-148">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0a3b-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e0a3b-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e0a3b-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e0a3b-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e0a3b-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e0a3b-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e0a3b-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e0a3b-152">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e0a3b-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e0a3b-153">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0a3b-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0a3b-154">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e0a3b-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e0a3b-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0a3b-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0a3b-156">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0a3b-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0a3b-157">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0a3b-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0a3b-158">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0a3b-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e0a3b-159">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e0a3b-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e0a3b-160">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e0a3b-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e0a3b-161">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0a3b-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0a3b-162">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0a3b-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0a3b-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0a3b-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0a3b-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e0a3b-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e0a3b-165">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0a3b-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0a3b-166">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0a3b-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0a3b-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e0a3b-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e0a3b-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e0a3b-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e0a3b-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e0a3b-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e0a3b-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e0a3b-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e0a3b-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e0a3b-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e0a3b-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0a3b-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
