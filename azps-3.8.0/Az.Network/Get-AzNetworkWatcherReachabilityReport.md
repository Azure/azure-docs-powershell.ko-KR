---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 0ad2b1fa6278e085a57d94f2fec9be2c6853993d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878145"
---
# <span data-ttu-id="97c66-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="97c66-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="97c66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c66-102">SYNOPSIS</span></span>
<span data-ttu-id="97c66-103">지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="97c66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97c66-104">SYNTAX</span></span>

### <span data-ttu-id="97c66-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="97c66-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c66-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="97c66-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c66-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="97c66-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97c66-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="97c66-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97c66-109">설명은</span><span class="sxs-lookup"><span data-stu-id="97c66-109">DESCRIPTION</span></span>
<span data-ttu-id="97c66-110">Get-AzNetworkWatcherReachabilityReport는 지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="97c66-111">예제의</span><span class="sxs-lookup"><span data-stu-id="97c66-111">EXAMPLES</span></span>

### <span data-ttu-id="97c66-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="97c66-112">Example 1</span></span>
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

<span data-ttu-id="97c66-113">미국 내에서 2017-10-10부터 2017-10-12 까지의 Azure 데이터 센터에 대 한 상대적 대기 시간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="97c66-114">변수</span><span class="sxs-lookup"><span data-stu-id="97c66-114">PARAMETERS</span></span>

### <span data-ttu-id="97c66-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97c66-115">-AsJob</span></span>
<span data-ttu-id="97c66-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="97c66-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97c66-117">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="97c66-117">-City</span></span>
<span data-ttu-id="97c66-118">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-118">The name of the city.</span></span>

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

### <span data-ttu-id="97c66-119">-국가</span><span class="sxs-lookup"><span data-stu-id="97c66-119">-Country</span></span>
<span data-ttu-id="97c66-120">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-120">The name of the country.</span></span>

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

### <span data-ttu-id="97c66-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c66-121">-DefaultProfile</span></span>
<span data-ttu-id="97c66-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97c66-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="97c66-123">-EndTime</span></span>
<span data-ttu-id="97c66-124">Azure 연결 가능성 보고서의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="97c66-125">-위치</span><span class="sxs-lookup"><span data-stu-id="97c66-125">-Location</span></span>
<span data-ttu-id="97c66-126">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="97c66-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97c66-127">-NetworkWatcher</span></span>
<span data-ttu-id="97c66-128">네트워크 감시자 리소스</span><span class="sxs-lookup"><span data-stu-id="97c66-128">The network watcher resource</span></span>

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

### <span data-ttu-id="97c66-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="97c66-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="97c66-130">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="97c66-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="97c66-131">-NetworkWatcherName</span></span>
<span data-ttu-id="97c66-132">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="97c66-133">-공급자</span><span class="sxs-lookup"><span data-stu-id="97c66-133">-Provider</span></span>
<span data-ttu-id="97c66-134">인터넷 서비스 공급자 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="97c66-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c66-135">-ResourceGroupName</span></span>
<span data-ttu-id="97c66-136">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="97c66-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97c66-137">-ResourceId</span></span>
<span data-ttu-id="97c66-138">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="97c66-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="97c66-139">-StartTime</span></span>
<span data-ttu-id="97c66-140">Azure 연결 가능성 보고서의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="97c66-141">-상태</span><span class="sxs-lookup"><span data-stu-id="97c66-141">-State</span></span>
<span data-ttu-id="97c66-142">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-142">The name of the state.</span></span>

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

### <span data-ttu-id="97c66-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c66-143">CommonParameters</span></span>
<span data-ttu-id="97c66-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97c66-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c66-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97c66-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c66-146">입력</span><span class="sxs-lookup"><span data-stu-id="97c66-146">INPUTS</span></span>

### <span data-ttu-id="97c66-147">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97c66-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="97c66-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="97c66-148">System.String</span></span>

## <span data-ttu-id="97c66-149">출력</span><span class="sxs-lookup"><span data-stu-id="97c66-149">OUTPUTS</span></span>

### <span data-ttu-id="97c66-150">PSAzureReachabilityReport에 대 한.</span><span class="sxs-lookup"><span data-stu-id="97c66-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="97c66-151">상속자</span><span class="sxs-lookup"><span data-stu-id="97c66-151">NOTES</span></span>
<span data-ttu-id="97c66-152">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결성, 보고서</span><span class="sxs-lookup"><span data-stu-id="97c66-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="97c66-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97c66-153">RELATED LINKS</span></span>

[<span data-ttu-id="97c66-154">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97c66-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="97c66-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97c66-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="97c66-156">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="97c66-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="97c66-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="97c66-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="97c66-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="97c66-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="97c66-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="97c66-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="97c66-160">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="97c66-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="97c66-161">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="97c66-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="97c66-162">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="97c66-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="97c66-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="97c66-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="97c66-164">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="97c66-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="97c66-165">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="97c66-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="97c66-166">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="97c66-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="97c66-167">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="97c66-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="97c66-168">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="97c66-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="97c66-169">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="97c66-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="97c66-170">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="97c66-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="97c66-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="97c66-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="97c66-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="97c66-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="97c66-173">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="97c66-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="97c66-174">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="97c66-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="97c66-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="97c66-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="97c66-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="97c66-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="97c66-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="97c66-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="97c66-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="97c66-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="97c66-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="97c66-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="97c66-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="97c66-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)