---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 227bd70bd67ff29015223becc6788f5043ae4776
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400317"
---
# <span data-ttu-id="667bb-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="667bb-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="667bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667bb-102">SYNOPSIS</span></span>
<span data-ttu-id="667bb-103">지정된 Azure 지역에 사용 가능한 모든 인터넷 서비스 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="667bb-104">구문</span><span class="sxs-lookup"><span data-stu-id="667bb-104">SYNTAX</span></span>

### <span data-ttu-id="667bb-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="667bb-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="667bb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="667bb-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="667bb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="667bb-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="667bb-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="667bb-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="667bb-109">설명</span><span class="sxs-lookup"><span data-stu-id="667bb-109">DESCRIPTION</span></span>
<span data-ttu-id="667bb-110">이 Get-AzNetworkWatcherReachabilityProvidersList 지정된 Azure 지역에 사용 가능한 모든 인터넷 서비스 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="667bb-111">예제</span><span class="sxs-lookup"><span data-stu-id="667bb-111">EXAMPLES</span></span>

### <span data-ttu-id="667bb-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="667bb-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="667bb-113">미국 서부의 Azure 데이터 센터용 시애틀, WA에서 사용 가능한 모든 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="667bb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="667bb-114">PARAMETERS</span></span>

### <span data-ttu-id="667bb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="667bb-115">-AsJob</span></span>
<span data-ttu-id="667bb-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="667bb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="667bb-117">-City</span><span class="sxs-lookup"><span data-stu-id="667bb-117">-City</span></span>
<span data-ttu-id="667bb-118">도시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-118">The name of the city.</span></span>

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

### <span data-ttu-id="667bb-119">-Country</span><span class="sxs-lookup"><span data-stu-id="667bb-119">-Country</span></span>
<span data-ttu-id="667bb-120">국가 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-120">The name of the country.</span></span>

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

### <span data-ttu-id="667bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667bb-121">-DefaultProfile</span></span>
<span data-ttu-id="667bb-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="667bb-123">-Location</span><span class="sxs-lookup"><span data-stu-id="667bb-123">-Location</span></span>
<span data-ttu-id="667bb-124">쿼리 범위를 지정하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="667bb-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="667bb-125">-NetworkWatcher</span></span>
<span data-ttu-id="667bb-126">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="667bb-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="667bb-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="667bb-128">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="667bb-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="667bb-129">-NetworkWatcherName</span></span>
<span data-ttu-id="667bb-130">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="667bb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667bb-131">-ResourceGroupName</span></span>
<span data-ttu-id="667bb-132">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="667bb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="667bb-133">-ResourceId</span></span>
<span data-ttu-id="667bb-134">Network Watcher 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="667bb-135">-State</span><span class="sxs-lookup"><span data-stu-id="667bb-135">-State</span></span>
<span data-ttu-id="667bb-136">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-136">The name of the state.</span></span>

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

### <span data-ttu-id="667bb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667bb-137">CommonParameters</span></span>
<span data-ttu-id="667bb-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="667bb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667bb-139">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="667bb-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667bb-140">입력</span><span class="sxs-lookup"><span data-stu-id="667bb-140">INPUTS</span></span>

### <span data-ttu-id="667bb-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="667bb-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="667bb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="667bb-142">System.String</span></span>

## <span data-ttu-id="667bb-143">출력</span><span class="sxs-lookup"><span data-stu-id="667bb-143">OUTPUTS</span></span>

### <span data-ttu-id="667bb-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="667bb-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="667bb-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="667bb-145">NOTES</span></span>
<span data-ttu-id="667bb-146">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 다음, 홉</span><span class="sxs-lookup"><span data-stu-id="667bb-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="667bb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="667bb-147">RELATED LINKS</span></span>

[<span data-ttu-id="667bb-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="667bb-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="667bb-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="667bb-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="667bb-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="667bb-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="667bb-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="667bb-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="667bb-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="667bb-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="667bb-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="667bb-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="667bb-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="667bb-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="667bb-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="667bb-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="667bb-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="667bb-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="667bb-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="667bb-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="667bb-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="667bb-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="667bb-159">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="667bb-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="667bb-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="667bb-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="667bb-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="667bb-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="667bb-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="667bb-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="667bb-163">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="667bb-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="667bb-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="667bb-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="667bb-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="667bb-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="667bb-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="667bb-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="667bb-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="667bb-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="667bb-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="667bb-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="667bb-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="667bb-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="667bb-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="667bb-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="667bb-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="667bb-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="667bb-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="667bb-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="667bb-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="667bb-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="667bb-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="667bb-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
