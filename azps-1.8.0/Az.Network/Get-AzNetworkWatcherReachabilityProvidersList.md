---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: cf35292be5005a957e245370a5b15b78bb7d4fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700519"
---
# <span data-ttu-id="4623d-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4623d-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="4623d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4623d-102">SYNOPSIS</span></span>
<span data-ttu-id="4623d-103">지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="4623d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4623d-104">SYNTAX</span></span>

### <span data-ttu-id="4623d-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4623d-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4623d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4623d-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4623d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4623d-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4623d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4623d-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4623d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="4623d-109">DESCRIPTION</span></span>
<span data-ttu-id="4623d-110">Get-AzNetworkWatcherReachabilityProvidersList에는 지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="4623d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4623d-111">EXAMPLES</span></span>

### <span data-ttu-id="4623d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4623d-112">Example 1</span></span>
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

<span data-ttu-id="4623d-113">미국 내에서 Azure Data Center에 대해 시애틀에 있는 사용 가능한 모든 공급자 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="4623d-114">변수</span><span class="sxs-lookup"><span data-stu-id="4623d-114">PARAMETERS</span></span>

### <span data-ttu-id="4623d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4623d-115">-AsJob</span></span>
<span data-ttu-id="4623d-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4623d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4623d-117">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="4623d-117">-City</span></span>
<span data-ttu-id="4623d-118">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-118">The name of the city.</span></span>

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

### <span data-ttu-id="4623d-119">-국가</span><span class="sxs-lookup"><span data-stu-id="4623d-119">-Country</span></span>
<span data-ttu-id="4623d-120">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-120">The name of the country.</span></span>

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

### <span data-ttu-id="4623d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4623d-121">-DefaultProfile</span></span>
<span data-ttu-id="4623d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4623d-123">-위치</span><span class="sxs-lookup"><span data-stu-id="4623d-123">-Location</span></span>
<span data-ttu-id="4623d-124">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="4623d-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4623d-125">-NetworkWatcher</span></span>
<span data-ttu-id="4623d-126">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="4623d-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="4623d-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="4623d-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="4623d-128">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4623d-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4623d-129">-NetworkWatcherName</span></span>
<span data-ttu-id="4623d-130">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="4623d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4623d-131">-ResourceGroupName</span></span>
<span data-ttu-id="4623d-132">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4623d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4623d-133">-ResourceId</span></span>
<span data-ttu-id="4623d-134">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="4623d-135">-상태</span><span class="sxs-lookup"><span data-stu-id="4623d-135">-State</span></span>
<span data-ttu-id="4623d-136">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-136">The name of the state.</span></span>

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

### <span data-ttu-id="4623d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4623d-137">CommonParameters</span></span>
<span data-ttu-id="4623d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4623d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4623d-139">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4623d-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4623d-140">입력</span><span class="sxs-lookup"><span data-stu-id="4623d-140">INPUTS</span></span>

### <span data-ttu-id="4623d-141">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4623d-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4623d-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4623d-142">System.String</span></span>

## <span data-ttu-id="4623d-143">출력</span><span class="sxs-lookup"><span data-stu-id="4623d-143">OUTPUTS</span></span>

### <span data-ttu-id="4623d-144">PSAvailableProvidersList에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4623d-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="4623d-145">상속자</span><span class="sxs-lookup"><span data-stu-id="4623d-145">NOTES</span></span>
<span data-ttu-id="4623d-146">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="4623d-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="4623d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4623d-147">RELATED LINKS</span></span>

[<span data-ttu-id="4623d-148">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4623d-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4623d-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4623d-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4623d-150">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4623d-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4623d-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4623d-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4623d-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4623d-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4623d-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4623d-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4623d-154">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4623d-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4623d-155">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4623d-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4623d-156">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4623d-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4623d-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4623d-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4623d-158">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4623d-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4623d-159">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4623d-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4623d-160">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4623d-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4623d-161">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4623d-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4623d-162">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4623d-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4623d-163">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4623d-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4623d-164">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4623d-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4623d-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4623d-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4623d-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4623d-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4623d-167">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4623d-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4623d-168">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4623d-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4623d-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4623d-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4623d-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4623d-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4623d-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4623d-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4623d-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4623d-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4623d-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4623d-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4623d-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4623d-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
