---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: f38250a4beed7eb05f758e17a1d3d17f1d76f86e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400198"
---
# <span data-ttu-id="1c9c7-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c9c7-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="1c9c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9c7-103">새 Network Watcher 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="1c9c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c9c7-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c9c7-105">설명</span><span class="sxs-lookup"><span data-stu-id="1c9c7-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9c7-106">New-AzNetworkWatcher cmdlet은 새 Network Watcher 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="1c9c7-107">예제</span><span class="sxs-lookup"><span data-stu-id="1c9c7-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9c7-108">예제 1: Network Watcher 만들기</span><span class="sxs-lookup"><span data-stu-id="1c9c7-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="1c9c7-109">이 예제에서는 새로 만든 리소스 그룹 내에서 새 Network Watcher를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="1c9c7-110">구독당 지역당 하나의 Network Watcher만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="1c9c7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c9c7-111">PARAMETERS</span></span>

### <span data-ttu-id="1c9c7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9c7-112">-DefaultProfile</span></span>
<span data-ttu-id="1c9c7-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c9c7-114">-Location</span><span class="sxs-lookup"><span data-stu-id="1c9c7-114">-Location</span></span>
<span data-ttu-id="1c9c7-115">위치.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-115">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9c7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1c9c7-116">-Name</span></span>
<span data-ttu-id="1c9c7-117">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9c7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c9c7-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c9c7-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9c7-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c9c7-120">-Tag</span></span>
<span data-ttu-id="1c9c7-121">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1c9c7-122">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1c9c7-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9c7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c9c7-123">-Confirm</span></span>
<span data-ttu-id="1c9c7-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9c7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9c7-125">-WhatIf</span></span>
<span data-ttu-id="1c9c7-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c9c7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c9c7-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9c7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9c7-128">CommonParameters</span></span>
<span data-ttu-id="1c9c7-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9c7-130">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1c9c7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9c7-131">입력</span><span class="sxs-lookup"><span data-stu-id="1c9c7-131">INPUTS</span></span>

### <span data-ttu-id="1c9c7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1c9c7-132">System.String</span></span>

### <span data-ttu-id="1c9c7-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c9c7-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1c9c7-134">출력</span><span class="sxs-lookup"><span data-stu-id="1c9c7-134">OUTPUTS</span></span>

### <span data-ttu-id="1c9c7-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c9c7-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="1c9c7-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c9c7-136">NOTES</span></span>
<span data-ttu-id="1c9c7-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="1c9c7-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="1c9c7-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c9c7-138">RELATED LINKS</span></span>

[<span data-ttu-id="1c9c7-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c9c7-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1c9c7-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c9c7-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1c9c7-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c9c7-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1c9c7-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1c9c7-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1c9c7-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1c9c7-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1c9c7-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1c9c7-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1c9c7-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1c9c7-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1c9c7-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c9c7-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c9c7-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1c9c7-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1c9c7-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c9c7-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c9c7-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c9c7-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c9c7-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c9c7-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c9c7-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c9c7-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1c9c7-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1c9c7-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1c9c7-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1c9c7-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1c9c7-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c9c7-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c9c7-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c9c7-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c9c7-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c9c7-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c9c7-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1c9c7-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1c9c7-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c9c7-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c9c7-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c9c7-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c9c7-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1c9c7-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1c9c7-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1c9c7-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1c9c7-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1c9c7-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1c9c7-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1c9c7-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1c9c7-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1c9c7-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1c9c7-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c9c7-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
