---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a4e9c9a928d3a6c3ddeb7afa754cc957089a2283
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216413"
---
# <span data-ttu-id="9ba15-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9ba15-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="9ba15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba15-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba15-103">지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="9ba15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ba15-104">SYNTAX</span></span>

### <span data-ttu-id="9ba15-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9ba15-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ba15-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9ba15-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba15-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9ba15-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba15-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ba15-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ba15-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9ba15-109">DESCRIPTION</span></span>
<span data-ttu-id="9ba15-110">Get-AzNetworkWatcherReachabilityProvidersList에는 지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="9ba15-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9ba15-111">EXAMPLES</span></span>

### <span data-ttu-id="9ba15-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ba15-112">Example 1</span></span>
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

<span data-ttu-id="9ba15-113">미국 내에서 Azure Data Center에 대해 시애틀에 있는 사용 가능한 모든 공급자 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="9ba15-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9ba15-114">Example 2</span></span>

<span data-ttu-id="9ba15-115">지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="9ba15-116">생성</span><span class="sxs-lookup"><span data-stu-id="9ba15-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="9ba15-117">변수</span><span class="sxs-lookup"><span data-stu-id="9ba15-117">PARAMETERS</span></span>

### <span data-ttu-id="9ba15-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ba15-118">-AsJob</span></span>
<span data-ttu-id="9ba15-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9ba15-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ba15-120">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="9ba15-120">-City</span></span>
<span data-ttu-id="9ba15-121">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-121">The name of the city.</span></span>

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

### <span data-ttu-id="9ba15-122">-국가</span><span class="sxs-lookup"><span data-stu-id="9ba15-122">-Country</span></span>
<span data-ttu-id="9ba15-123">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-123">The name of the country.</span></span>

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

### <span data-ttu-id="9ba15-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba15-124">-DefaultProfile</span></span>
<span data-ttu-id="9ba15-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ba15-126">-위치</span><span class="sxs-lookup"><span data-stu-id="9ba15-126">-Location</span></span>
<span data-ttu-id="9ba15-127">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="9ba15-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ba15-128">-NetworkWatcher</span></span>
<span data-ttu-id="9ba15-129">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="9ba15-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="9ba15-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="9ba15-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="9ba15-131">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9ba15-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9ba15-132">-NetworkWatcherName</span></span>
<span data-ttu-id="9ba15-133">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="9ba15-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba15-134">-ResourceGroupName</span></span>
<span data-ttu-id="9ba15-135">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9ba15-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ba15-136">-ResourceId</span></span>
<span data-ttu-id="9ba15-137">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="9ba15-138">-상태</span><span class="sxs-lookup"><span data-stu-id="9ba15-138">-State</span></span>
<span data-ttu-id="9ba15-139">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-139">The name of the state.</span></span>

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

### <span data-ttu-id="9ba15-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba15-140">CommonParameters</span></span>
<span data-ttu-id="9ba15-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba15-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ba15-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba15-143">입력</span><span class="sxs-lookup"><span data-stu-id="9ba15-143">INPUTS</span></span>

### <span data-ttu-id="9ba15-144">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ba15-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9ba15-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ba15-145">System.String</span></span>

## <span data-ttu-id="9ba15-146">출력</span><span class="sxs-lookup"><span data-stu-id="9ba15-146">OUTPUTS</span></span>

### <span data-ttu-id="9ba15-147">PSAvailableProvidersList에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9ba15-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="9ba15-148">상속자</span><span class="sxs-lookup"><span data-stu-id="9ba15-148">NOTES</span></span>
<span data-ttu-id="9ba15-149">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="9ba15-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="9ba15-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ba15-150">RELATED LINKS</span></span>

[<span data-ttu-id="9ba15-151">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ba15-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9ba15-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ba15-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9ba15-153">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ba15-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9ba15-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9ba15-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9ba15-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9ba15-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9ba15-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9ba15-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9ba15-157">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9ba15-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9ba15-158">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ba15-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ba15-159">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9ba15-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9ba15-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ba15-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ba15-161">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ba15-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ba15-162">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ba15-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ba15-163">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ba15-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9ba15-164">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9ba15-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9ba15-165">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9ba15-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9ba15-166">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ba15-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ba15-167">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ba15-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ba15-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ba15-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ba15-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9ba15-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9ba15-170">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ba15-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ba15-171">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ba15-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ba15-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9ba15-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9ba15-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9ba15-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9ba15-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9ba15-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9ba15-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9ba15-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9ba15-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9ba15-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9ba15-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ba15-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
