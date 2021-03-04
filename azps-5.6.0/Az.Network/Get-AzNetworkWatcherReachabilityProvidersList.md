---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 0d9d5867007c25db64cf8232ec9b66591362eef4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954384"
---
# <span data-ttu-id="92f67-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="92f67-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="92f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f67-102">SYNOPSIS</span></span>
<span data-ttu-id="92f67-103">지정된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="92f67-104">구문</span><span class="sxs-lookup"><span data-stu-id="92f67-104">SYNTAX</span></span>

### <span data-ttu-id="92f67-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="92f67-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92f67-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="92f67-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92f67-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="92f67-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92f67-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="92f67-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f67-109">설명</span><span class="sxs-lookup"><span data-stu-id="92f67-109">DESCRIPTION</span></span>
<span data-ttu-id="92f67-110">이 Get-AzNetworkWatcherReachabilityProvidersList Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="92f67-111">예제</span><span class="sxs-lookup"><span data-stu-id="92f67-111">EXAMPLES</span></span>

### <span data-ttu-id="92f67-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="92f67-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="92f67-113">미국 서부의 Azure Data Center용 시애틀의 사용 가능한 모든 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="92f67-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="92f67-114">Example 2</span></span>

<span data-ttu-id="92f67-115">지정된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="92f67-116">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="92f67-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="92f67-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="92f67-117">PARAMETERS</span></span>

### <span data-ttu-id="92f67-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92f67-118">-AsJob</span></span>
<span data-ttu-id="92f67-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="92f67-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92f67-120">-City</span><span class="sxs-lookup"><span data-stu-id="92f67-120">-City</span></span>
<span data-ttu-id="92f67-121">도시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-121">The name of the city.</span></span>

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

### <span data-ttu-id="92f67-122">-Country</span><span class="sxs-lookup"><span data-stu-id="92f67-122">-Country</span></span>
<span data-ttu-id="92f67-123">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-123">The name of the country.</span></span>

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

### <span data-ttu-id="92f67-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f67-124">-DefaultProfile</span></span>
<span data-ttu-id="92f67-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f67-126">-Location</span><span class="sxs-lookup"><span data-stu-id="92f67-126">-Location</span></span>
<span data-ttu-id="92f67-127">쿼리 범위를 지정하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="92f67-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="92f67-128">-NetworkWatcher</span></span>
<span data-ttu-id="92f67-129">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="92f67-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="92f67-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="92f67-131">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="92f67-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="92f67-132">-NetworkWatcherName</span></span>
<span data-ttu-id="92f67-133">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="92f67-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f67-134">-ResourceGroupName</span></span>
<span data-ttu-id="92f67-135">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="92f67-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92f67-136">-ResourceId</span></span>
<span data-ttu-id="92f67-137">네트워크 감시자 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="92f67-138">-State</span><span class="sxs-lookup"><span data-stu-id="92f67-138">-State</span></span>
<span data-ttu-id="92f67-139">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-139">The name of the state.</span></span>

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

### <span data-ttu-id="92f67-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f67-140">CommonParameters</span></span>
<span data-ttu-id="92f67-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92f67-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f67-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92f67-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f67-143">입력</span><span class="sxs-lookup"><span data-stu-id="92f67-143">INPUTS</span></span>

### <span data-ttu-id="92f67-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="92f67-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="92f67-145">System.String</span><span class="sxs-lookup"><span data-stu-id="92f67-145">System.String</span></span>

## <span data-ttu-id="92f67-146">출력</span><span class="sxs-lookup"><span data-stu-id="92f67-146">OUTPUTS</span></span>

### <span data-ttu-id="92f67-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="92f67-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="92f67-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92f67-148">NOTES</span></span>
<span data-ttu-id="92f67-149">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 다음, 홉</span><span class="sxs-lookup"><span data-stu-id="92f67-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="92f67-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92f67-150">RELATED LINKS</span></span>

[<span data-ttu-id="92f67-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="92f67-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="92f67-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="92f67-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="92f67-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="92f67-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="92f67-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="92f67-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="92f67-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="92f67-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="92f67-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="92f67-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="92f67-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="92f67-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="92f67-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92f67-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="92f67-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="92f67-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="92f67-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92f67-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="92f67-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92f67-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="92f67-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92f67-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="92f67-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="92f67-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="92f67-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="92f67-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="92f67-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="92f67-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="92f67-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92f67-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92f67-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92f67-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92f67-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92f67-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92f67-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="92f67-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="92f67-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92f67-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92f67-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92f67-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92f67-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="92f67-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="92f67-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="92f67-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="92f67-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="92f67-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="92f67-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="92f67-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="92f67-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="92f67-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="92f67-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92f67-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
