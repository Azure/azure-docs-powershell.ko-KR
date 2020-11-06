---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 4cb80bec513459797790ae04c3e26a2f25fe95db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531985"
---
# <span data-ttu-id="13f7b-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="13f7b-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="13f7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="13f7b-103">지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13f7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13f7b-104">SYNTAX</span></span>

### <span data-ttu-id="13f7b-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="13f7b-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f7b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="13f7b-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f7b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="13f7b-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f7b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="13f7b-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13f7b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="13f7b-109">DESCRIPTION</span></span>
<span data-ttu-id="13f7b-110">Get-AzureRmNetworkWatcherReachabilityProvidersList에는 지정 된 Azure 지역에 대해 사용 가능한 모든 인터넷 서비스 공급자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-110">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="13f7b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="13f7b-111">EXAMPLES</span></span>

### <span data-ttu-id="13f7b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="13f7b-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="13f7b-113">미국 내에서 Azure Data Center에 대해 시애틀에 있는 사용 가능한 모든 공급자 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="13f7b-114">변수</span><span class="sxs-lookup"><span data-stu-id="13f7b-114">PARAMETERS</span></span>

### <span data-ttu-id="13f7b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13f7b-115">-AsJob</span></span>
<span data-ttu-id="13f7b-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="13f7b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13f7b-117">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="13f7b-117">-City</span></span>
<span data-ttu-id="13f7b-118">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-118">The name of the city.</span></span>

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

### <span data-ttu-id="13f7b-119">-국가</span><span class="sxs-lookup"><span data-stu-id="13f7b-119">-Country</span></span>
<span data-ttu-id="13f7b-120">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-120">The name of the country.</span></span>

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

### <span data-ttu-id="13f7b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f7b-121">-DefaultProfile</span></span>
<span data-ttu-id="13f7b-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f7b-123">-위치</span><span class="sxs-lookup"><span data-stu-id="13f7b-123">-Location</span></span>
<span data-ttu-id="13f7b-124">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="13f7b-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="13f7b-125">-NetworkWatcher</span></span>
<span data-ttu-id="13f7b-126">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="13f7b-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="13f7b-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="13f7b-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="13f7b-128">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="13f7b-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="13f7b-129">-NetworkWatcherName</span></span>
<span data-ttu-id="13f7b-130">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="13f7b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f7b-131">-ResourceGroupName</span></span>
<span data-ttu-id="13f7b-132">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="13f7b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13f7b-133">-ResourceId</span></span>
<span data-ttu-id="13f7b-134">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="13f7b-135">-상태</span><span class="sxs-lookup"><span data-stu-id="13f7b-135">-State</span></span>
<span data-ttu-id="13f7b-136">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-136">The name of the state.</span></span>

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

### <span data-ttu-id="13f7b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f7b-137">CommonParameters</span></span>
<span data-ttu-id="13f7b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f7b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f7b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f7b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f7b-140">입력</span><span class="sxs-lookup"><span data-stu-id="13f7b-140">INPUTS</span></span>

### <span data-ttu-id="13f7b-141">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="13f7b-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="13f7b-142">매개 변수: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13f7b-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="13f7b-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13f7b-143">System.String</span></span>

## <span data-ttu-id="13f7b-144">출력</span><span class="sxs-lookup"><span data-stu-id="13f7b-144">OUTPUTS</span></span>

### <span data-ttu-id="13f7b-145">PSAvailableProvidersList에 대 한.</span><span class="sxs-lookup"><span data-stu-id="13f7b-145">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="13f7b-146">상속자</span><span class="sxs-lookup"><span data-stu-id="13f7b-146">NOTES</span></span>
<span data-ttu-id="13f7b-147">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="13f7b-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="13f7b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13f7b-148">RELATED LINKS</span></span>

[<span data-ttu-id="13f7b-149">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="13f7b-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="13f7b-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="13f7b-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="13f7b-151">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="13f7b-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="13f7b-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="13f7b-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="13f7b-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="13f7b-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="13f7b-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="13f7b-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="13f7b-155">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="13f7b-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="13f7b-156">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="13f7b-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="13f7b-157">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="13f7b-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="13f7b-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="13f7b-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="13f7b-159">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="13f7b-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="13f7b-160">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="13f7b-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="13f7b-161">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="13f7b-161">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="13f7b-162">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="13f7b-162">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="13f7b-163">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="13f7b-163">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="13f7b-164">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="13f7b-164">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="13f7b-165">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="13f7b-165">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="13f7b-166">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="13f7b-166">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="13f7b-167">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="13f7b-167">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="13f7b-168">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="13f7b-168">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="13f7b-169">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="13f7b-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="13f7b-170">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="13f7b-170">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="13f7b-171">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="13f7b-171">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="13f7b-172">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="13f7b-172">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="13f7b-173">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="13f7b-173">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="13f7b-174">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="13f7b-174">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="13f7b-175">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="13f7b-175">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
