---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 49c7dc8359d0745f54aa94dc5cd1e7ce9a0e2307
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954272"
---
# <span data-ttu-id="c85c6-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c85c6-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="c85c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c85c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c85c6-103">이전에 실행되거나 현재 실행 중인 문제 해결 작업에서 문제 해결 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="c85c6-104">구문</span><span class="sxs-lookup"><span data-stu-id="c85c6-104">SYNTAX</span></span>

### <span data-ttu-id="c85c6-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="c85c6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c85c6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c85c6-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c85c6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c85c6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c85c6-108">설명</span><span class="sxs-lookup"><span data-stu-id="c85c6-108">DESCRIPTION</span></span>
<span data-ttu-id="c85c6-109">Get-AzNetworkWatcherTroubleshootingResult cmdlet은 이전에 실행되거나 현재 실행 중인 작업에서 문제 해결 Start-AzNetworkWatcherResourceTroubleshooting 합니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="c85c6-110">문제 해결 작업이 현재 진행 중인 경우 이 작업을 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="c85c6-111">현재 Virtual Network Gateway 및 연결이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="c85c6-112">예제</span><span class="sxs-lookup"><span data-stu-id="c85c6-112">EXAMPLES</span></span>

### <span data-ttu-id="c85c6-113">예제 1: Virtual Network Gateway에서 문제 해결 시작 및 결과 검색</span><span class="sxs-lookup"><span data-stu-id="c85c6-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="c85c6-114">위의 샘플은 가상 네트워크 게이트웨이에서 문제 해결을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="c85c6-115">작업을 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="c85c6-116">문제 해결이 시작되면 이 Get-AzNetworkWatcherTroubleshootingResult 결과를 검색하기 위해 리소스에 대한 호출이 호출됩니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="c85c6-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c85c6-117">PARAMETERS</span></span>

### <span data-ttu-id="c85c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c85c6-118">-DefaultProfile</span></span>
<span data-ttu-id="c85c6-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c85c6-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c85c6-120">-Location</span></span>
<span data-ttu-id="c85c6-121">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c85c6-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c85c6-122">-NetworkWatcher</span></span>
<span data-ttu-id="c85c6-123">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="c85c6-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c85c6-124">-NetworkWatcherName</span></span>
<span data-ttu-id="c85c6-125">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-125">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c85c6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c85c6-126">-ResourceGroupName</span></span>
<span data-ttu-id="c85c6-127">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c85c6-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c85c6-128">-TargetResourceId</span></span>
<span data-ttu-id="c85c6-129">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-129">The target resource ID.</span></span>

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

### <span data-ttu-id="c85c6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c85c6-130">CommonParameters</span></span>
<span data-ttu-id="c85c6-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c85c6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c85c6-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c85c6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c85c6-133">입력</span><span class="sxs-lookup"><span data-stu-id="c85c6-133">INPUTS</span></span>

### <span data-ttu-id="c85c6-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c85c6-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c85c6-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c85c6-135">System.String</span></span>

## <span data-ttu-id="c85c6-136">출력</span><span class="sxs-lookup"><span data-stu-id="c85c6-136">OUTPUTS</span></span>

### <span data-ttu-id="c85c6-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c85c6-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="c85c6-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c85c6-138">NOTES</span></span>
<span data-ttu-id="c85c6-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="c85c6-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="c85c6-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c85c6-140">RELATED LINKS</span></span>

[<span data-ttu-id="c85c6-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c85c6-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c85c6-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c85c6-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c85c6-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c85c6-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c85c6-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c85c6-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c85c6-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c85c6-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c85c6-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c85c6-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c85c6-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c85c6-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c85c6-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c85c6-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c85c6-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c85c6-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c85c6-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c85c6-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c85c6-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c85c6-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c85c6-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c85c6-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c85c6-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c85c6-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c85c6-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c85c6-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c85c6-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c85c6-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c85c6-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c85c6-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c85c6-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c85c6-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c85c6-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c85c6-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c85c6-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c85c6-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c85c6-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c85c6-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c85c6-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c85c6-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c85c6-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c85c6-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c85c6-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c85c6-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c85c6-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c85c6-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c85c6-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c85c6-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c85c6-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c85c6-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c85c6-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c85c6-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
