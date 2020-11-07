---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: dc8093a9e508084639fe64b68378cf44f41aa67d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870654"
---
# <span data-ttu-id="7de3c-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7de3c-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="7de3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7de3c-102">SYNOPSIS</span></span>
<span data-ttu-id="7de3c-103">패킷 캡처 리소스의 정보 및 속성 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="7de3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7de3c-104">SYNTAX</span></span>

### <span data-ttu-id="7de3c-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="7de3c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7de3c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7de3c-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7de3c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7de3c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7de3c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7de3c-108">DESCRIPTION</span></span>
<span data-ttu-id="7de3c-109">Get-AzNetworkWatcherPacketCapture는 패킷 캡처 리소스의 속성 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="7de3c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7de3c-110">EXAMPLES</span></span>

### <span data-ttu-id="7de3c-111">예제 1: 여러 필터를 사용 하 여 패킷 캡처를 만들고 해당 상태를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="7de3c-112">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="7de3c-113">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="7de3c-114">그런 다음 Get-AzNetworkWatcherPacketCapture를 호출 하 여 캡처 세션의 상태를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="7de3c-115">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="7de3c-116">New-AzNetworkWatcherPacketCapture 명령에서 직접 패킷 캡처에 대 한 참조를 만들면 모든 속성이 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="7de3c-117">Get-AzNetworkWatcherPacketCapture 명령을 호출 하 여 패킷 캡처의 모든 속성을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="7de3c-118">예제 2: 여러 필터를 사용 하 여 패킷 캡처를 만들고 해당 상태를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="7de3c-119">이 cmdlet은 nw1 네트워크 감시자에서 "PacketCapture"로 시작 하는 모든 PacketCaptures를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="7de3c-120">변수</span><span class="sxs-lookup"><span data-stu-id="7de3c-120">PARAMETERS</span></span>

### <span data-ttu-id="7de3c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7de3c-121">-AsJob</span></span>
<span data-ttu-id="7de3c-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7de3c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7de3c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de3c-123">-DefaultProfile</span></span>
<span data-ttu-id="7de3c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7de3c-125">-위치</span><span class="sxs-lookup"><span data-stu-id="7de3c-125">-Location</span></span>
<span data-ttu-id="7de3c-126">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7de3c-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7de3c-127">-NetworkWatcher</span></span>
<span data-ttu-id="7de3c-128">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="7de3c-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="7de3c-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7de3c-129">-NetworkWatcherName</span></span>
<span data-ttu-id="7de3c-130">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="7de3c-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="7de3c-131">-PacketCaptureName</span></span>
<span data-ttu-id="7de3c-132">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-132">The packet capture name.</span></span>

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

### <span data-ttu-id="7de3c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de3c-133">-ResourceGroupName</span></span>
<span data-ttu-id="7de3c-134">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7de3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de3c-135">CommonParameters</span></span>
<span data-ttu-id="7de3c-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7de3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de3c-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7de3c-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de3c-138">입력</span><span class="sxs-lookup"><span data-stu-id="7de3c-138">INPUTS</span></span>

### <span data-ttu-id="7de3c-139">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7de3c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7de3c-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7de3c-140">System.String</span></span>

## <span data-ttu-id="7de3c-141">출력</span><span class="sxs-lookup"><span data-stu-id="7de3c-141">OUTPUTS</span></span>

### <span data-ttu-id="7de3c-142">PSGetPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7de3c-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="7de3c-143">상속자</span><span class="sxs-lookup"><span data-stu-id="7de3c-143">NOTES</span></span>
<span data-ttu-id="7de3c-144">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="7de3c-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="7de3c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7de3c-145">RELATED LINKS</span></span>

[<span data-ttu-id="7de3c-146">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7de3c-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7de3c-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7de3c-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7de3c-148">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7de3c-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7de3c-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7de3c-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7de3c-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7de3c-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7de3c-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7de3c-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7de3c-152">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7de3c-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7de3c-153">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7de3c-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7de3c-154">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7de3c-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7de3c-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7de3c-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7de3c-156">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7de3c-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7de3c-157">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7de3c-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7de3c-158">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7de3c-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7de3c-159">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7de3c-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7de3c-160">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7de3c-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7de3c-161">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7de3c-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7de3c-162">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7de3c-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7de3c-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7de3c-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7de3c-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7de3c-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7de3c-165">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7de3c-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7de3c-166">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7de3c-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7de3c-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7de3c-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7de3c-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7de3c-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7de3c-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7de3c-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7de3c-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7de3c-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7de3c-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7de3c-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="7de3c-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7de3c-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

