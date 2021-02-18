---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 83ff992b20c24606d09889d0bc49fd9520ef6efb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410211"
---
# <span data-ttu-id="c7bf8-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bf8-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="c7bf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bf8-103">Network Watcher를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="c7bf8-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7bf8-104">SYNTAX</span></span>

### <span data-ttu-id="c7bf8-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c7bf8-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7bf8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c7bf8-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7bf8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c7bf8-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7bf8-108">설명</span><span class="sxs-lookup"><span data-stu-id="c7bf8-108">DESCRIPTION</span></span>
<span data-ttu-id="c7bf8-109">Remove-AzNetworkWatcher cmdlet은 Network Watcher 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="c7bf8-110">예제</span><span class="sxs-lookup"><span data-stu-id="c7bf8-110">EXAMPLES</span></span>

### <span data-ttu-id="c7bf8-111">예제 1: Network Watcher 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="c7bf8-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="c7bf8-112">이 예제에서는 리소스 그룹에 Network Watcher를 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c7bf8-113">구독당 지역당 하나의 Network Watcher만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="c7bf8-114">가상 네트워크를 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="c7bf8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7bf8-115">PARAMETERS</span></span>

### <span data-ttu-id="c7bf8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7bf8-116">-AsJob</span></span>
<span data-ttu-id="c7bf8-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c7bf8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7bf8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bf8-118">-DefaultProfile</span></span>
<span data-ttu-id="c7bf8-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7bf8-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c7bf8-120">-Location</span></span>
<span data-ttu-id="c7bf8-121">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c7bf8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c7bf8-122">-Name</span></span>
<span data-ttu-id="c7bf8-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf8-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bf8-124">-NetworkWatcher</span></span>
<span data-ttu-id="c7bf8-125">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="c7bf8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7bf8-126">-PassThru</span></span>
<span data-ttu-id="c7bf8-127">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-127">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7bf8-128">-ResourceGroupName</span></span>
<span data-ttu-id="c7bf8-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bf8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7bf8-130">-Confirm</span></span>
<span data-ttu-id="c7bf8-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7bf8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7bf8-132">-WhatIf</span></span>
<span data-ttu-id="c7bf8-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c7bf8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7bf8-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7bf8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bf8-135">CommonParameters</span></span>
<span data-ttu-id="c7bf8-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bf8-137">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bf8-138">입력</span><span class="sxs-lookup"><span data-stu-id="c7bf8-138">INPUTS</span></span>

### <span data-ttu-id="c7bf8-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bf8-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c7bf8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c7bf8-140">System.String</span></span>

## <span data-ttu-id="c7bf8-141">출력</span><span class="sxs-lookup"><span data-stu-id="c7bf8-141">OUTPUTS</span></span>

### <span data-ttu-id="c7bf8-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c7bf8-142">System.Boolean</span></span>

## <span data-ttu-id="c7bf8-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7bf8-143">NOTES</span></span>
<span data-ttu-id="c7bf8-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="c7bf8-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="c7bf8-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7bf8-145">RELATED LINKS</span></span>

[<span data-ttu-id="c7bf8-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bf8-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c7bf8-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bf8-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c7bf8-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7bf8-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c7bf8-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c7bf8-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c7bf8-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c7bf8-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c7bf8-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c7bf8-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c7bf8-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c7bf8-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c7bf8-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7bf8-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7bf8-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c7bf8-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c7bf8-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7bf8-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7bf8-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7bf8-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7bf8-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7bf8-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7bf8-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7bf8-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c7bf8-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c7bf8-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c7bf8-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c7bf8-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c7bf8-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7bf8-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7bf8-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7bf8-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7bf8-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7bf8-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7bf8-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7bf8-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c7bf8-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7bf8-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7bf8-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7bf8-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7bf8-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c7bf8-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c7bf8-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c7bf8-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c7bf8-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c7bf8-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c7bf8-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c7bf8-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c7bf8-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c7bf8-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c7bf8-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7bf8-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
