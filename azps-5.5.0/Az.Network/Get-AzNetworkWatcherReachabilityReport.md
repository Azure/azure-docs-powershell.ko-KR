---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: f29ab593ffac847ec6b089efdc39bc594ad1d785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412846"
---
# <span data-ttu-id="72942-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="72942-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="72942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72942-102">SYNOPSIS</span></span>
<span data-ttu-id="72942-103">인터넷 서비스 공급자의 상대적 대기 시간 점수를 지정된 위치에서 Azure 지역으로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="72942-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="72942-104">구문</span><span class="sxs-lookup"><span data-stu-id="72942-104">SYNTAX</span></span>

### <span data-ttu-id="72942-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="72942-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72942-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="72942-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72942-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72942-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72942-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="72942-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72942-109">설명</span><span class="sxs-lookup"><span data-stu-id="72942-109">DESCRIPTION</span></span>
<span data-ttu-id="72942-110">이 Get-AzNetworkWatcherReachabilityReport 지정된 위치에서 Azure 지역으로 인터넷 서비스 공급자에 대한 상대적 대기 시간 점수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="72942-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="72942-111">예제</span><span class="sxs-lookup"><span data-stu-id="72942-111">EXAMPLES</span></span>

### <span data-ttu-id="72942-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="72942-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="72942-113">미국 내 2017-10-10에서 2017-10-12까지 미국 서부의 Azure 데이터 센터에 대한 상대적 대기 시간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="72942-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="72942-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="72942-114">Example 2</span></span>

<span data-ttu-id="72942-115">인터넷 서비스 공급자의 상대적 대기 시간 점수를 지정된 위치에서 Azure 지역으로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="72942-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="72942-116">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="72942-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="72942-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72942-117">PARAMETERS</span></span>

### <span data-ttu-id="72942-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72942-118">-AsJob</span></span>
<span data-ttu-id="72942-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="72942-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72942-120">-City</span><span class="sxs-lookup"><span data-stu-id="72942-120">-City</span></span>
<span data-ttu-id="72942-121">도시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-121">The name of the city.</span></span>

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

### <span data-ttu-id="72942-122">-Country</span><span class="sxs-lookup"><span data-stu-id="72942-122">-Country</span></span>
<span data-ttu-id="72942-123">국가 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-123">The name of the country.</span></span>

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

### <span data-ttu-id="72942-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72942-124">-DefaultProfile</span></span>
<span data-ttu-id="72942-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72942-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="72942-126">-EndTime</span></span>
<span data-ttu-id="72942-127">Azure 도달 가능성 보고서의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="72942-128">-Location</span><span class="sxs-lookup"><span data-stu-id="72942-128">-Location</span></span>
<span data-ttu-id="72942-129">쿼리 범위를 지정하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="72942-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72942-130">-NetworkWatcher</span></span>
<span data-ttu-id="72942-131">Network Watcher 리소스</span><span class="sxs-lookup"><span data-stu-id="72942-131">The network watcher resource</span></span>

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

### <span data-ttu-id="72942-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="72942-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="72942-133">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="72942-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="72942-134">-NetworkWatcherName</span></span>
<span data-ttu-id="72942-135">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="72942-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="72942-136">-Provider</span></span>
<span data-ttu-id="72942-137">인터넷 서비스 공급자 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="72942-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72942-138">-ResourceGroupName</span></span>
<span data-ttu-id="72942-139">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="72942-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72942-140">-ResourceId</span></span>
<span data-ttu-id="72942-141">Network Watcher 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="72942-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="72942-142">-StartTime</span></span>
<span data-ttu-id="72942-143">Azure 도달 가능성 보고서의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="72942-144">-State</span><span class="sxs-lookup"><span data-stu-id="72942-144">-State</span></span>
<span data-ttu-id="72942-145">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72942-145">The name of the state.</span></span>

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

### <span data-ttu-id="72942-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72942-146">CommonParameters</span></span>
<span data-ttu-id="72942-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="72942-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72942-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="72942-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72942-149">입력</span><span class="sxs-lookup"><span data-stu-id="72942-149">INPUTS</span></span>

### <span data-ttu-id="72942-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72942-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="72942-151">System.String</span><span class="sxs-lookup"><span data-stu-id="72942-151">System.String</span></span>

## <span data-ttu-id="72942-152">출력</span><span class="sxs-lookup"><span data-stu-id="72942-152">OUTPUTS</span></span>

### <span data-ttu-id="72942-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="72942-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="72942-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="72942-154">NOTES</span></span>
<span data-ttu-id="72942-155">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 가능성, 보고서</span><span class="sxs-lookup"><span data-stu-id="72942-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="72942-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72942-156">RELATED LINKS</span></span>

[<span data-ttu-id="72942-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72942-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="72942-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72942-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="72942-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="72942-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="72942-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="72942-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="72942-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="72942-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="72942-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="72942-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="72942-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="72942-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="72942-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72942-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72942-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="72942-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="72942-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72942-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72942-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72942-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72942-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="72942-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="72942-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="72942-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="72942-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="72942-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="72942-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="72942-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="72942-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72942-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72942-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72942-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72942-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72942-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72942-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="72942-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="72942-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72942-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72942-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72942-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="72942-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="72942-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="72942-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="72942-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="72942-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="72942-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="72942-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="72942-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="72942-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="72942-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="72942-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="72942-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
