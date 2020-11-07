---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 145f19778d9263911cd5df8b709bd18f80fc6f51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699927"
---
# <span data-ttu-id="f39fb-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f39fb-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="f39fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f39fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f39fb-103">특정 대상에서 패킷을 허용 또는 거부 하는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="f39fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f39fb-104">SYNTAX</span></span>

### <span data-ttu-id="f39fb-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="f39fb-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f39fb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f39fb-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f39fb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f39fb-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f39fb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f39fb-108">DESCRIPTION</span></span>
<span data-ttu-id="f39fb-109">지정 된 VM 리소스와 로컬 및 원격 IP 주소 및 포트를 사용 하는 지정 된 방향의 패킷에 대 한 Test-AzNetworkWatcherIPFlow cmdlet은 패킷이 허용 되는지 거부 되는지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="f39fb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f39fb-110">EXAMPLES</span></span>

### <span data-ttu-id="f39fb-111">예제 1: Test-AzNetworkWatcherIPFlow 실행</span><span class="sxs-lookup"><span data-stu-id="f39fb-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="f39fb-112">이 플랜에 대 한 서쪽 중앙 US의 네트워크 감시자를 다운로드 한 다음 VM과 연결 된 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="f39fb-113">그런 다음 첫 번째 네트워크 인터페이스에 대해 첫 번째 네트워크 인터페이스에서 인터넷 IP에 대 한 아웃 바운드 연결의 첫 번째 IP를 사용 하 여 Test-AzNetworkWatcherIPFlow를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="f39fb-114">변수</span><span class="sxs-lookup"><span data-stu-id="f39fb-114">PARAMETERS</span></span>

### <span data-ttu-id="f39fb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f39fb-115">-AsJob</span></span>
<span data-ttu-id="f39fb-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f39fb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f39fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39fb-117">-DefaultProfile</span></span>
<span data-ttu-id="f39fb-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f39fb-119">방향</span><span class="sxs-lookup"><span data-stu-id="f39fb-119">-Direction</span></span>
<span data-ttu-id="f39fb-120">지침.</span><span class="sxs-lookup"><span data-stu-id="f39fb-120">Direction.</span></span>

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

### <span data-ttu-id="f39fb-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="f39fb-121">-LocalIPAddress</span></span>
<span data-ttu-id="f39fb-122">로컬 IP 주소</span><span class="sxs-lookup"><span data-stu-id="f39fb-122">Local IP Address.</span></span>

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

### <span data-ttu-id="f39fb-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="f39fb-123">-LocalPort</span></span>
<span data-ttu-id="f39fb-124">로컬 포트.</span><span class="sxs-lookup"><span data-stu-id="f39fb-124">Local Port.</span></span>

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

### <span data-ttu-id="f39fb-125">-위치</span><span class="sxs-lookup"><span data-stu-id="f39fb-125">-Location</span></span>
<span data-ttu-id="f39fb-126">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f39fb-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f39fb-127">-NetworkWatcher</span></span>
<span data-ttu-id="f39fb-128">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="f39fb-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="f39fb-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f39fb-129">-NetworkWatcherName</span></span>
<span data-ttu-id="f39fb-130">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="f39fb-131">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="f39fb-131">-Protocol</span></span>
<span data-ttu-id="f39fb-132">프로토콜별.</span><span class="sxs-lookup"><span data-stu-id="f39fb-132">Protocol.</span></span>

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

### <span data-ttu-id="f39fb-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="f39fb-133">-RemoteIPAddress</span></span>
<span data-ttu-id="f39fb-134">원격 IP 주소</span><span class="sxs-lookup"><span data-stu-id="f39fb-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="f39fb-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="f39fb-135">-RemotePort</span></span>
<span data-ttu-id="f39fb-136">원격 포트.</span><span class="sxs-lookup"><span data-stu-id="f39fb-136">Remote port.</span></span>

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

### <span data-ttu-id="f39fb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39fb-137">-ResourceGroupName</span></span>
<span data-ttu-id="f39fb-138">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f39fb-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="f39fb-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f39fb-140">대상 네트워크 인터페이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="f39fb-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f39fb-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f39fb-142">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f39fb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39fb-143">CommonParameters</span></span>
<span data-ttu-id="f39fb-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f39fb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39fb-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39fb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39fb-146">입력</span><span class="sxs-lookup"><span data-stu-id="f39fb-146">INPUTS</span></span>

### <span data-ttu-id="f39fb-147">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f39fb-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f39fb-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f39fb-148">System.String</span></span>

## <span data-ttu-id="f39fb-149">출력</span><span class="sxs-lookup"><span data-stu-id="f39fb-149">OUTPUTS</span></span>

### <span data-ttu-id="f39fb-150">PSIPFlowVerifyResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f39fb-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="f39fb-151">상속자</span><span class="sxs-lookup"><span data-stu-id="f39fb-151">NOTES</span></span>
<span data-ttu-id="f39fb-152">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="f39fb-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="f39fb-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f39fb-153">RELATED LINKS</span></span>

[<span data-ttu-id="f39fb-154">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f39fb-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f39fb-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f39fb-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f39fb-156">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f39fb-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f39fb-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f39fb-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f39fb-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f39fb-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f39fb-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f39fb-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f39fb-160">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f39fb-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f39fb-161">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f39fb-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f39fb-162">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f39fb-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f39fb-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f39fb-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f39fb-164">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f39fb-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f39fb-165">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f39fb-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f39fb-166">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f39fb-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f39fb-167">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f39fb-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f39fb-168">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f39fb-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f39fb-169">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f39fb-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f39fb-170">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f39fb-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f39fb-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f39fb-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f39fb-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f39fb-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f39fb-173">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f39fb-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f39fb-174">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f39fb-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f39fb-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f39fb-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f39fb-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f39fb-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f39fb-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f39fb-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f39fb-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f39fb-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f39fb-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f39fb-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="f39fb-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f39fb-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)