---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 09d75e73cc6139bfa2c3d0d6293b07060a709f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711063"
---
# <span data-ttu-id="ae834-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ae834-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="ae834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae834-102">SYNOPSIS</span></span>
<span data-ttu-id="ae834-103">지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae834-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae834-104">SYNTAX</span></span>

### <span data-ttu-id="ae834-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae834-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae834-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ae834-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae834-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae834-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae834-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ae834-108">SetByLocation</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherLocation <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae834-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ae834-109">DESCRIPTION</span></span>
<span data-ttu-id="ae834-110">Get-AzureRmNetworkWatcherReachabilityReport는 지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-110">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="ae834-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ae834-111">EXAMPLES</span></span>

### <span data-ttu-id="ae834-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae834-112">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="ae834-113">미국 내에서 2017-10-10부터 2017-10-12 까지의 Azure 데이터 센터에 대 한 상대적 대기 시간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="ae834-114">변수</span><span class="sxs-lookup"><span data-stu-id="ae834-114">PARAMETERS</span></span>

### <span data-ttu-id="ae834-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae834-115">-AsJob</span></span>
<span data-ttu-id="ae834-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ae834-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae834-117">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="ae834-117">-City</span></span>
<span data-ttu-id="ae834-118">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-118">The name of the city.</span></span>

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

### <span data-ttu-id="ae834-119">-국가</span><span class="sxs-lookup"><span data-stu-id="ae834-119">-Country</span></span>
<span data-ttu-id="ae834-120">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-120">The name of the country.</span></span>

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

### <span data-ttu-id="ae834-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae834-121">-DefaultProfile</span></span>
<span data-ttu-id="ae834-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae834-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ae834-123">-EndTime</span></span>
<span data-ttu-id="ae834-124">Azure 연결 가능성 보고서의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="ae834-125">-위치</span><span class="sxs-lookup"><span data-stu-id="ae834-125">-Location</span></span>
<span data-ttu-id="ae834-126">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae834-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae834-127">-NetworkWatcher</span></span>
<span data-ttu-id="ae834-128">네트워크 감시자 리소스</span><span class="sxs-lookup"><span data-stu-id="ae834-128">The network watcher resource</span></span>

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

### <span data-ttu-id="ae834-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="ae834-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="ae834-130">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ae834-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ae834-131">-NetworkWatcherName</span></span>
<span data-ttu-id="ae834-132">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="ae834-133">-공급자</span><span class="sxs-lookup"><span data-stu-id="ae834-133">-Provider</span></span>
<span data-ttu-id="ae834-134">인터넷 서비스 공급자 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-134">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae834-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae834-135">-ResourceGroupName</span></span>
<span data-ttu-id="ae834-136">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ae834-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae834-137">-ResourceId</span></span>
<span data-ttu-id="ae834-138">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="ae834-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ae834-139">-StartTime</span></span>
<span data-ttu-id="ae834-140">Azure 연결 가능성 보고서의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="ae834-141">-상태</span><span class="sxs-lookup"><span data-stu-id="ae834-141">-State</span></span>
<span data-ttu-id="ae834-142">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-142">The name of the state.</span></span>

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

### <span data-ttu-id="ae834-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae834-143">CommonParameters</span></span>
<span data-ttu-id="ae834-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae834-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae834-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae834-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae834-146">입력</span><span class="sxs-lookup"><span data-stu-id="ae834-146">INPUTS</span></span>

### <span data-ttu-id="ae834-147">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae834-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ae834-148">매개 변수: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae834-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="ae834-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ae834-149">System.String</span></span>

## <span data-ttu-id="ae834-150">출력</span><span class="sxs-lookup"><span data-stu-id="ae834-150">OUTPUTS</span></span>

### <span data-ttu-id="ae834-151">PSAzureReachabilityReport에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ae834-151">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="ae834-152">상속자</span><span class="sxs-lookup"><span data-stu-id="ae834-152">NOTES</span></span>
<span data-ttu-id="ae834-153">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결성, 보고서</span><span class="sxs-lookup"><span data-stu-id="ae834-153">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="ae834-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae834-154">RELATED LINKS</span></span>

[<span data-ttu-id="ae834-155">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae834-155">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ae834-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae834-156">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ae834-157">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ae834-157">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ae834-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ae834-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ae834-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ae834-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ae834-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ae834-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ae834-161">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ae834-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ae834-162">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae834-162">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae834-163">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ae834-163">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ae834-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae834-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae834-165">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae834-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae834-166">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ae834-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ae834-167">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae834-167">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ae834-168">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ae834-168">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ae834-169">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ae834-169">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="ae834-170">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae834-170">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae834-171">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae834-171">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae834-172">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae834-172">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae834-173">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ae834-173">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ae834-174">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae834-174">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae834-175">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae834-175">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ae834-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ae834-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ae834-177">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ae834-177">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ae834-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ae834-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ae834-179">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ae834-179">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ae834-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ae834-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ae834-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ae834-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
