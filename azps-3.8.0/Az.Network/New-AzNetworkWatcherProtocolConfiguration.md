---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 5358fa9898bca17f75c0111ef15b69e8cff4f75d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041835"
---
# <span data-ttu-id="5d028-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d028-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="5d028-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d028-102">SYNOPSIS</span></span>
<span data-ttu-id="5d028-103">새 프로토콜 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d028-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="5d028-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d028-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d028-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d028-105">DESCRIPTION</span></span>
<span data-ttu-id="5d028-106">New-AzNetworkWatcherProtocolConfiguration cmdlet은 새 프로토콜 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d028-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="5d028-107">이 개체는 연결 검사 세션 중에 지정 된 기준을 사용 하 여 프로토콜 구성을 제한 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d028-107">This object is used to restrict the protocol configuration during a connectivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="5d028-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5d028-108">EXAMPLES</span></span>

### <span data-ttu-id="5d028-109">예제 1: 프로토콜 구성을 사용 하 여 VM에서 웹 사이트로 네트워크 감시자 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="5d028-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="5d028-110">이 예제에서는 Azure의 VM에서 www.bing.com에 대 한 연결을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d028-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="5d028-111">변수</span><span class="sxs-lookup"><span data-stu-id="5d028-111">PARAMETERS</span></span>

### <span data-ttu-id="5d028-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d028-112">-DefaultProfile</span></span>
<span data-ttu-id="5d028-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d028-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d028-114">-헤더</span><span class="sxs-lookup"><span data-stu-id="5d028-114">-Header</span></span>
<span data-ttu-id="5d028-115">HTTP 헤더 목록</span><span class="sxs-lookup"><span data-stu-id="5d028-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d028-116">-메서드</span><span class="sxs-lookup"><span data-stu-id="5d028-116">-Method</span></span>
<span data-ttu-id="5d028-117">HTTP 메서드</span><span class="sxs-lookup"><span data-stu-id="5d028-117">HTTP method</span></span>

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

### <span data-ttu-id="5d028-118">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="5d028-118">-Protocol</span></span>
<span data-ttu-id="5d028-119">프로토콜 종류</span><span class="sxs-lookup"><span data-stu-id="5d028-119">Protocol type</span></span>

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

### <span data-ttu-id="5d028-120">-유효한 Statuscode</span><span class="sxs-lookup"><span data-stu-id="5d028-120">-ValidStatusCode</span></span>
<span data-ttu-id="5d028-121">유효한 상태 코드</span><span class="sxs-lookup"><span data-stu-id="5d028-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d028-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d028-122">CommonParameters</span></span>
<span data-ttu-id="5d028-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d028-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d028-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d028-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d028-125">입력</span><span class="sxs-lookup"><span data-stu-id="5d028-125">INPUTS</span></span>

### <span data-ttu-id="5d028-126">않아야</span><span class="sxs-lookup"><span data-stu-id="5d028-126">None</span></span>

## <span data-ttu-id="5d028-127">출력</span><span class="sxs-lookup"><span data-stu-id="5d028-127">OUTPUTS</span></span>

### <span data-ttu-id="5d028-128">PSNetworkWatcherProtocolConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5d028-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="5d028-129">상속자</span><span class="sxs-lookup"><span data-stu-id="5d028-129">NOTES</span></span>
<span data-ttu-id="5d028-130">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 패킷, 캡처, 트래픽, 필터</span><span class="sxs-lookup"><span data-stu-id="5d028-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="5d028-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d028-131">RELATED LINKS</span></span>

[<span data-ttu-id="5d028-132">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d028-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5d028-133">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d028-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5d028-134">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5d028-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5d028-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5d028-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5d028-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5d028-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5d028-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5d028-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5d028-138">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5d028-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5d028-139">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d028-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d028-140">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5d028-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5d028-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d028-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d028-142">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d028-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d028-143">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5d028-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5d028-144">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d028-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5d028-145">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5d028-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5d028-146">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5d028-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5d028-147">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d028-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d028-148">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d028-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d028-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d028-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d028-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5d028-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5d028-151">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d028-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d028-152">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d028-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5d028-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5d028-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5d028-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5d028-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5d028-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5d028-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5d028-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5d028-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5d028-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5d028-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="5d028-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5d028-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
