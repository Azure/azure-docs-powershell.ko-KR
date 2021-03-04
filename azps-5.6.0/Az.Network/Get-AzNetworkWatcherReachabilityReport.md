---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 72aa9748cddee0a8ff894463e569d15a2fa01ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954379"
---
# <span data-ttu-id="c53db-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c53db-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="c53db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c53db-102">SYNOPSIS</span></span>
<span data-ttu-id="c53db-103">지정된 위치에서 Azure 지역으로 인터넷 서비스 공급자에 대한 상대 대기 시간 점수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="c53db-104">구문</span><span class="sxs-lookup"><span data-stu-id="c53db-104">SYNTAX</span></span>

### <span data-ttu-id="c53db-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c53db-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c53db-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c53db-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c53db-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c53db-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c53db-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c53db-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c53db-109">설명</span><span class="sxs-lookup"><span data-stu-id="c53db-109">DESCRIPTION</span></span>
<span data-ttu-id="c53db-110">이 Get-AzNetworkWatcherReachabilityReport 지정된 위치에서 Azure 지역으로 인터넷 서비스 공급자에 대한 상대 대기 시간 점수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="c53db-111">예제</span><span class="sxs-lookup"><span data-stu-id="c53db-111">EXAMPLES</span></span>

### <span data-ttu-id="c53db-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c53db-112">Example 1</span></span>
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

<span data-ttu-id="c53db-113">2017-10-10-2017-10-12 미국 서부의 Azure Data Center에 대한 상대 대기 시간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="c53db-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c53db-114">Example 2</span></span>

<span data-ttu-id="c53db-115">지정된 위치에서 Azure 지역으로 인터넷 서비스 공급자에 대한 상대 대기 시간 점수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="c53db-116">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="c53db-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="c53db-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c53db-117">PARAMETERS</span></span>

### <span data-ttu-id="c53db-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c53db-118">-AsJob</span></span>
<span data-ttu-id="c53db-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c53db-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c53db-120">-City</span><span class="sxs-lookup"><span data-stu-id="c53db-120">-City</span></span>
<span data-ttu-id="c53db-121">도시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-121">The name of the city.</span></span>

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

### <span data-ttu-id="c53db-122">-Country</span><span class="sxs-lookup"><span data-stu-id="c53db-122">-Country</span></span>
<span data-ttu-id="c53db-123">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-123">The name of the country.</span></span>

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

### <span data-ttu-id="c53db-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53db-124">-DefaultProfile</span></span>
<span data-ttu-id="c53db-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c53db-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c53db-126">-EndTime</span></span>
<span data-ttu-id="c53db-127">Azure 도달성 보고서의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="c53db-128">-Location</span><span class="sxs-lookup"><span data-stu-id="c53db-128">-Location</span></span>
<span data-ttu-id="c53db-129">쿼리 범위를 지정하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="c53db-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c53db-130">-NetworkWatcher</span></span>
<span data-ttu-id="c53db-131">네트워크 감시자 리소스</span><span class="sxs-lookup"><span data-stu-id="c53db-131">The network watcher resource</span></span>

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

### <span data-ttu-id="c53db-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="c53db-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="c53db-133">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c53db-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c53db-134">-NetworkWatcherName</span></span>
<span data-ttu-id="c53db-135">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="c53db-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="c53db-136">-Provider</span></span>
<span data-ttu-id="c53db-137">인터넷 서비스 공급자 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="c53db-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53db-138">-ResourceGroupName</span></span>
<span data-ttu-id="c53db-139">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c53db-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c53db-140">-ResourceId</span></span>
<span data-ttu-id="c53db-141">네트워크 감시자 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="c53db-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c53db-142">-StartTime</span></span>
<span data-ttu-id="c53db-143">Azure 도달성 보고서의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="c53db-144">-State</span><span class="sxs-lookup"><span data-stu-id="c53db-144">-State</span></span>
<span data-ttu-id="c53db-145">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-145">The name of the state.</span></span>

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

### <span data-ttu-id="c53db-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53db-146">CommonParameters</span></span>
<span data-ttu-id="c53db-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c53db-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53db-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c53db-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53db-149">입력</span><span class="sxs-lookup"><span data-stu-id="c53db-149">INPUTS</span></span>

### <span data-ttu-id="c53db-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c53db-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c53db-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c53db-151">System.String</span></span>

## <span data-ttu-id="c53db-152">출력</span><span class="sxs-lookup"><span data-stu-id="c53db-152">OUTPUTS</span></span>

### <span data-ttu-id="c53db-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c53db-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="c53db-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c53db-154">NOTES</span></span>
<span data-ttu-id="c53db-155">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 도달성, 보고서</span><span class="sxs-lookup"><span data-stu-id="c53db-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="c53db-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c53db-156">RELATED LINKS</span></span>

[<span data-ttu-id="c53db-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c53db-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c53db-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c53db-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c53db-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c53db-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c53db-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c53db-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c53db-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c53db-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c53db-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c53db-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c53db-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c53db-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c53db-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c53db-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c53db-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c53db-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c53db-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c53db-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c53db-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c53db-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c53db-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c53db-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c53db-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c53db-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c53db-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c53db-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c53db-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c53db-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c53db-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c53db-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c53db-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c53db-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c53db-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c53db-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c53db-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c53db-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c53db-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c53db-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c53db-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c53db-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c53db-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c53db-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c53db-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c53db-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c53db-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c53db-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c53db-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c53db-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c53db-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c53db-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c53db-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c53db-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
