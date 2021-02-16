---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: dcdd4ef2fd6ca3481d9bb3f8333174307be7e3f6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404085"
---
# <span data-ttu-id="1daba-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1daba-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="1daba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1daba-102">SYNOPSIS</span></span>
<span data-ttu-id="1daba-103">인터넷 서비스 공급자의 상대적 대기 시간 점수를 지정된 위치에서 Azure 지역으로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="1daba-104">구문</span><span class="sxs-lookup"><span data-stu-id="1daba-104">SYNTAX</span></span>

### <span data-ttu-id="1daba-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1daba-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1daba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1daba-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1daba-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1daba-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1daba-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1daba-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1daba-109">설명</span><span class="sxs-lookup"><span data-stu-id="1daba-109">DESCRIPTION</span></span>
<span data-ttu-id="1daba-110">이 Get-AzNetworkWatcherReachabilityReport 지정된 위치에서 Azure 지역으로 인터넷 서비스 공급자에 대한 상대적 대기 시간 점수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="1daba-111">예제</span><span class="sxs-lookup"><span data-stu-id="1daba-111">EXAMPLES</span></span>

### <span data-ttu-id="1daba-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1daba-112">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="1daba-113">미국 내 2017-10-10에서 2017-10-12까지 미국 서부의 Azure 데이터 센터에 대한 상대적 대기 시간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="1daba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1daba-114">PARAMETERS</span></span>

### <span data-ttu-id="1daba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1daba-115">-AsJob</span></span>
<span data-ttu-id="1daba-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1daba-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1daba-117">-City</span><span class="sxs-lookup"><span data-stu-id="1daba-117">-City</span></span>
<span data-ttu-id="1daba-118">도시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-118">The name of the city.</span></span>

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

### <span data-ttu-id="1daba-119">-Country</span><span class="sxs-lookup"><span data-stu-id="1daba-119">-Country</span></span>
<span data-ttu-id="1daba-120">국가 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-120">The name of the country.</span></span>

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

### <span data-ttu-id="1daba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1daba-121">-DefaultProfile</span></span>
<span data-ttu-id="1daba-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1daba-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1daba-123">-EndTime</span></span>
<span data-ttu-id="1daba-124">Azure 도달 가능성 보고서의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-124">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1daba-125">-Location</span><span class="sxs-lookup"><span data-stu-id="1daba-125">-Location</span></span>
<span data-ttu-id="1daba-126">쿼리 범위를 지정하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1daba-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1daba-127">-NetworkWatcher</span></span>
<span data-ttu-id="1daba-128">Network Watcher 리소스</span><span class="sxs-lookup"><span data-stu-id="1daba-128">The network watcher resource</span></span>

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

### <span data-ttu-id="1daba-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="1daba-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="1daba-130">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1daba-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1daba-131">-NetworkWatcherName</span></span>
<span data-ttu-id="1daba-132">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-132">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1daba-133">-Provider</span><span class="sxs-lookup"><span data-stu-id="1daba-133">-Provider</span></span>
<span data-ttu-id="1daba-134">인터넷 서비스 공급자 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-134">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1daba-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1daba-135">-ResourceGroupName</span></span>
<span data-ttu-id="1daba-136">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-136">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1daba-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1daba-137">-ResourceId</span></span>
<span data-ttu-id="1daba-138">Network Watcher 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-138">The Id of network watcher resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1daba-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1daba-139">-StartTime</span></span>
<span data-ttu-id="1daba-140">Azure 도달 가능성 보고서의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-140">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1daba-141">-State</span><span class="sxs-lookup"><span data-stu-id="1daba-141">-State</span></span>
<span data-ttu-id="1daba-142">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-142">The name of the state.</span></span>

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

### <span data-ttu-id="1daba-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1daba-143">CommonParameters</span></span>
<span data-ttu-id="1daba-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1daba-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1daba-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1daba-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1daba-146">입력</span><span class="sxs-lookup"><span data-stu-id="1daba-146">INPUTS</span></span>

### <span data-ttu-id="1daba-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1daba-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1daba-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1daba-148">System.String</span></span>

## <span data-ttu-id="1daba-149">출력</span><span class="sxs-lookup"><span data-stu-id="1daba-149">OUTPUTS</span></span>

### <span data-ttu-id="1daba-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1daba-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="1daba-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1daba-151">NOTES</span></span>
<span data-ttu-id="1daba-152">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 가능성, 보고서</span><span class="sxs-lookup"><span data-stu-id="1daba-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="1daba-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1daba-153">RELATED LINKS</span></span>

[<span data-ttu-id="1daba-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1daba-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1daba-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1daba-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1daba-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1daba-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1daba-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1daba-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1daba-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1daba-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1daba-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1daba-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1daba-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1daba-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1daba-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1daba-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1daba-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1daba-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1daba-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1daba-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1daba-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1daba-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1daba-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1daba-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1daba-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1daba-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1daba-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1daba-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1daba-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1daba-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1daba-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1daba-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1daba-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1daba-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1daba-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1daba-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1daba-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1daba-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1daba-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1daba-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1daba-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1daba-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1daba-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1daba-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1daba-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1daba-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1daba-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1daba-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1daba-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1daba-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1daba-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1daba-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1daba-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1daba-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
