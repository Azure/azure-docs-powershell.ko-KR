---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218344"
---
# <span data-ttu-id="55b74-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="55b74-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="55b74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55b74-102">SYNOPSIS</span></span>
<span data-ttu-id="55b74-103">지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="55b74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55b74-104">SYNTAX</span></span>

### <span data-ttu-id="55b74-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="55b74-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55b74-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="55b74-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55b74-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="55b74-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55b74-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="55b74-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55b74-109">설명은</span><span class="sxs-lookup"><span data-stu-id="55b74-109">DESCRIPTION</span></span>
<span data-ttu-id="55b74-110">Get-AzNetworkWatcherReachabilityReport는 지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="55b74-111">예제의</span><span class="sxs-lookup"><span data-stu-id="55b74-111">EXAMPLES</span></span>

### <span data-ttu-id="55b74-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="55b74-112">Example 1</span></span>
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

<span data-ttu-id="55b74-113">미국 내에서 2017-10-10부터 2017-10-12 까지의 Azure 데이터 센터에 대 한 상대적 대기 시간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="55b74-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="55b74-114">Example 2</span></span>

<span data-ttu-id="55b74-115">지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="55b74-116">생성</span><span class="sxs-lookup"><span data-stu-id="55b74-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="55b74-117">변수</span><span class="sxs-lookup"><span data-stu-id="55b74-117">PARAMETERS</span></span>

### <span data-ttu-id="55b74-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55b74-118">-AsJob</span></span>
<span data-ttu-id="55b74-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="55b74-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55b74-120">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="55b74-120">-City</span></span>
<span data-ttu-id="55b74-121">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-121">The name of the city.</span></span>

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

### <span data-ttu-id="55b74-122">-국가</span><span class="sxs-lookup"><span data-stu-id="55b74-122">-Country</span></span>
<span data-ttu-id="55b74-123">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-123">The name of the country.</span></span>

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

### <span data-ttu-id="55b74-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b74-124">-DefaultProfile</span></span>
<span data-ttu-id="55b74-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55b74-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="55b74-126">-EndTime</span></span>
<span data-ttu-id="55b74-127">Azure 연결 가능성 보고서의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="55b74-128">-위치</span><span class="sxs-lookup"><span data-stu-id="55b74-128">-Location</span></span>
<span data-ttu-id="55b74-129">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="55b74-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55b74-130">-NetworkWatcher</span></span>
<span data-ttu-id="55b74-131">네트워크 감시자 리소스</span><span class="sxs-lookup"><span data-stu-id="55b74-131">The network watcher resource</span></span>

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

### <span data-ttu-id="55b74-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="55b74-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="55b74-133">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="55b74-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="55b74-134">-NetworkWatcherName</span></span>
<span data-ttu-id="55b74-135">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="55b74-136">-공급자</span><span class="sxs-lookup"><span data-stu-id="55b74-136">-Provider</span></span>
<span data-ttu-id="55b74-137">인터넷 서비스 공급자 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="55b74-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b74-138">-ResourceGroupName</span></span>
<span data-ttu-id="55b74-139">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="55b74-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55b74-140">-ResourceId</span></span>
<span data-ttu-id="55b74-141">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="55b74-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="55b74-142">-StartTime</span></span>
<span data-ttu-id="55b74-143">Azure 연결 가능성 보고서의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="55b74-144">-상태</span><span class="sxs-lookup"><span data-stu-id="55b74-144">-State</span></span>
<span data-ttu-id="55b74-145">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-145">The name of the state.</span></span>

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

### <span data-ttu-id="55b74-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b74-146">CommonParameters</span></span>
<span data-ttu-id="55b74-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55b74-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b74-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="55b74-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b74-149">입력</span><span class="sxs-lookup"><span data-stu-id="55b74-149">INPUTS</span></span>

### <span data-ttu-id="55b74-150">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55b74-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="55b74-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="55b74-151">System.String</span></span>

## <span data-ttu-id="55b74-152">출력</span><span class="sxs-lookup"><span data-stu-id="55b74-152">OUTPUTS</span></span>

### <span data-ttu-id="55b74-153">PSAzureReachabilityReport에 대 한.</span><span class="sxs-lookup"><span data-stu-id="55b74-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="55b74-154">상속자</span><span class="sxs-lookup"><span data-stu-id="55b74-154">NOTES</span></span>
<span data-ttu-id="55b74-155">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결성, 보고서</span><span class="sxs-lookup"><span data-stu-id="55b74-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="55b74-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55b74-156">RELATED LINKS</span></span>

[<span data-ttu-id="55b74-157">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55b74-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="55b74-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55b74-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="55b74-159">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55b74-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="55b74-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="55b74-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="55b74-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="55b74-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="55b74-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="55b74-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="55b74-163">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="55b74-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="55b74-164">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55b74-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="55b74-165">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="55b74-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="55b74-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55b74-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="55b74-167">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55b74-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="55b74-168">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55b74-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="55b74-169">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="55b74-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="55b74-170">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="55b74-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="55b74-171">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="55b74-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="55b74-172">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55b74-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55b74-173">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55b74-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55b74-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55b74-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55b74-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="55b74-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="55b74-176">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55b74-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55b74-177">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55b74-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55b74-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="55b74-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="55b74-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="55b74-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="55b74-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="55b74-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="55b74-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="55b74-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="55b74-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="55b74-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="55b74-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55b74-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
