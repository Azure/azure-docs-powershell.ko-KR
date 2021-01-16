---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345146"
---
# <span data-ttu-id="79b43-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79b43-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="79b43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79b43-102">SYNOPSIS</span></span>
<span data-ttu-id="79b43-103">Network Watcher를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="79b43-104">구문</span><span class="sxs-lookup"><span data-stu-id="79b43-104">SYNTAX</span></span>

### <span data-ttu-id="79b43-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="79b43-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b43-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="79b43-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b43-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="79b43-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b43-108">설명</span><span class="sxs-lookup"><span data-stu-id="79b43-108">DESCRIPTION</span></span>
<span data-ttu-id="79b43-109">이 Remove-AzNetworkWatcher cmdlet은 Network Watcher 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="79b43-110">예제</span><span class="sxs-lookup"><span data-stu-id="79b43-110">EXAMPLES</span></span>

### <span data-ttu-id="79b43-111">예제 1: Network Watcher 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="79b43-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="79b43-112">이 예제에서는 리소스 그룹에 Network Watcher를 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="79b43-113">구독당 지역당 하나의 Network Watcher만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="79b43-114">가상 네트워크를 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="79b43-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79b43-115">PARAMETERS</span></span>

### <span data-ttu-id="79b43-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79b43-116">-AsJob</span></span>
<span data-ttu-id="79b43-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="79b43-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79b43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b43-118">-DefaultProfile</span></span>
<span data-ttu-id="79b43-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b43-120">-Location</span><span class="sxs-lookup"><span data-stu-id="79b43-120">-Location</span></span>
<span data-ttu-id="79b43-121">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="79b43-122">-Name</span><span class="sxs-lookup"><span data-stu-id="79b43-122">-Name</span></span>
<span data-ttu-id="79b43-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-123">The resource name.</span></span>

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

### <span data-ttu-id="79b43-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79b43-124">-NetworkWatcher</span></span>
<span data-ttu-id="79b43-125">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="79b43-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79b43-126">-PassThru</span></span>
<span data-ttu-id="79b43-127">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="79b43-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b43-128">-ResourceGroupName</span></span>
<span data-ttu-id="79b43-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-129">The resource group name.</span></span>

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

### <span data-ttu-id="79b43-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79b43-130">-Confirm</span></span>
<span data-ttu-id="79b43-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b43-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b43-132">-WhatIf</span></span>
<span data-ttu-id="79b43-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="79b43-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b43-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b43-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b43-135">CommonParameters</span></span>
<span data-ttu-id="79b43-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79b43-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b43-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="79b43-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b43-138">입력</span><span class="sxs-lookup"><span data-stu-id="79b43-138">INPUTS</span></span>

### <span data-ttu-id="79b43-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79b43-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="79b43-140">System.String</span><span class="sxs-lookup"><span data-stu-id="79b43-140">System.String</span></span>

## <span data-ttu-id="79b43-141">출력</span><span class="sxs-lookup"><span data-stu-id="79b43-141">OUTPUTS</span></span>

### <span data-ttu-id="79b43-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79b43-142">System.Boolean</span></span>

## <span data-ttu-id="79b43-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="79b43-143">NOTES</span></span>
<span data-ttu-id="79b43-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="79b43-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="79b43-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79b43-145">RELATED LINKS</span></span>

[<span data-ttu-id="79b43-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79b43-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="79b43-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79b43-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="79b43-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79b43-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="79b43-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="79b43-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="79b43-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="79b43-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="79b43-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="79b43-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="79b43-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="79b43-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="79b43-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="79b43-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="79b43-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="79b43-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="79b43-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="79b43-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="79b43-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="79b43-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="79b43-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="79b43-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="79b43-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="79b43-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="79b43-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="79b43-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="79b43-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="79b43-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="79b43-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79b43-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79b43-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79b43-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79b43-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79b43-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79b43-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="79b43-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="79b43-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79b43-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79b43-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79b43-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79b43-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="79b43-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="79b43-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="79b43-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="79b43-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="79b43-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="79b43-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="79b43-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="79b43-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="79b43-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="79b43-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79b43-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
