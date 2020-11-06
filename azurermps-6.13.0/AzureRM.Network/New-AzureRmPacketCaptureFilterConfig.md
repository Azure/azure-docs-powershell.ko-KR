---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: 3c69884e988b10f41da4d41d98318ee96c019112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537551"
---
# <span data-ttu-id="5820a-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5820a-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="5820a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5820a-102">SYNOPSIS</span></span>
<span data-ttu-id="5820a-103">새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5820a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5820a-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5820a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5820a-105">DESCRIPTION</span></span>
<span data-ttu-id="5820a-106">New-AzureRmPacketCaptureFilterConfig cmdlet은 새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="5820a-107">이 개체는 지정 된 기준을 사용 하 여 패킷 캡처 세션 중에 캡처한 패킷의 유형을 제한 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="5820a-108">New-AzureRmNetworkWatcherPacketCapture cmdlet은 여러 필터 개체를 허용 하 여 작성 가능한 캡처 세션을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="5820a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5820a-109">EXAMPLES</span></span>

### <span data-ttu-id="5820a-110">예제 1: 여러 필터를 사용 하 여 패킷 캡처 만들기</span><span class="sxs-lookup"><span data-stu-id="5820a-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="5820a-111">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="5820a-112">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="5820a-113">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="5820a-114">변수</span><span class="sxs-lookup"><span data-stu-id="5820a-114">PARAMETERS</span></span>

### <span data-ttu-id="5820a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5820a-115">-DefaultProfile</span></span>
<span data-ttu-id="5820a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5820a-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="5820a-117">-LocalIPAddress</span></span>
<span data-ttu-id="5820a-118">필터링 할 로컬 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="5820a-119">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="5820a-120">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="5820a-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="5820a-121">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="5820a-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="5820a-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="5820a-122">-LocalPort</span></span>
<span data-ttu-id="5820a-123">필터링 할 로컬 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="5820a-124">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="5820a-125">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="5820a-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="5820a-126">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="5820a-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="5820a-127">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="5820a-127">-Protocol</span></span>
<span data-ttu-id="5820a-128">필터링 할 Procotol를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="5820a-129">허용 되는 값 "TCP", "UDP", "모든"</span><span class="sxs-lookup"><span data-stu-id="5820a-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5820a-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="5820a-130">-RemoteIPAddress</span></span>
<span data-ttu-id="5820a-131">필터링 할 원격 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="5820a-132">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="5820a-133">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="5820a-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="5820a-134">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="5820a-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="5820a-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="5820a-135">-RemotePort</span></span>
<span data-ttu-id="5820a-136">필터링 할 원격 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="5820a-137">원격 포트 예제 입력: 단일 포트 항목의 경우 "80".</span><span class="sxs-lookup"><span data-stu-id="5820a-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="5820a-138">범위에 대 한 "80-85".</span><span class="sxs-lookup"><span data-stu-id="5820a-138">"80-85" for range.</span></span>
<span data-ttu-id="5820a-139">여러 항목에 대해 "80; 443;"</span><span class="sxs-lookup"><span data-stu-id="5820a-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="5820a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5820a-140">CommonParameters</span></span>
<span data-ttu-id="5820a-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5820a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5820a-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5820a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5820a-143">입력</span><span class="sxs-lookup"><span data-stu-id="5820a-143">INPUTS</span></span>

### <span data-ttu-id="5820a-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5820a-144">System.String</span></span>
<span data-ttu-id="5820a-145">매개 변수: Protocol (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5820a-145">Parameters: Protocol (ByValue)</span></span>

## <span data-ttu-id="5820a-146">출력</span><span class="sxs-lookup"><span data-stu-id="5820a-146">OUTPUTS</span></span>

### <span data-ttu-id="5820a-147">PSPacketCaptureFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5820a-147">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="5820a-148">상속자</span><span class="sxs-lookup"><span data-stu-id="5820a-148">NOTES</span></span>
<span data-ttu-id="5820a-149">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 패킷, 캡처, 트래픽, 필터</span><span class="sxs-lookup"><span data-stu-id="5820a-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="5820a-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5820a-150">RELATED LINKS</span></span>

[<span data-ttu-id="5820a-151">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5820a-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5820a-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5820a-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5820a-153">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5820a-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5820a-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5820a-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5820a-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5820a-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5820a-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5820a-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5820a-157">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5820a-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5820a-158">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5820a-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5820a-159">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5820a-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5820a-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5820a-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5820a-161">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5820a-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5820a-162">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5820a-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5820a-163">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5820a-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5820a-164">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5820a-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5820a-165">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5820a-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="5820a-166">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5820a-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5820a-167">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5820a-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5820a-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5820a-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5820a-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5820a-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5820a-170">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5820a-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5820a-171">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5820a-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5820a-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5820a-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5820a-173">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5820a-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5820a-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5820a-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5820a-175">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5820a-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5820a-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5820a-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="5820a-177">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5820a-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
