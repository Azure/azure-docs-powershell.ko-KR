---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: db3e3e529fd5c056acf793cd14280ef688c58a81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379828"
---
# <span data-ttu-id="6ff0b-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6ff0b-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="6ff0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ff0b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff0b-103">이전에 실행했거나 현재 실행 중인 문제 해결 작업에서 문제 해결 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="6ff0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ff0b-104">SYNTAX</span></span>

### <span data-ttu-id="6ff0b-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ff0b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ff0b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6ff0b-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ff0b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6ff0b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff0b-108">설명</span><span class="sxs-lookup"><span data-stu-id="6ff0b-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff0b-109">Get-AzNetworkWatcherTroubleshootingResult cmdlet은 이전에 실행했거나 현재 실행 중인 작업에서 문제 해결 Start-AzNetworkWatcherResourceTroubleshooting 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="6ff0b-110">문제 해결 작업이 현재 진행 중인 경우 이 작업을 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="6ff0b-111">현재 Virtual Network 게이트웨이 및 연결이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="6ff0b-112">예제</span><span class="sxs-lookup"><span data-stu-id="6ff0b-112">EXAMPLES</span></span>

### <span data-ttu-id="6ff0b-113">예제 1: Virtual Network 게이트웨이에서 문제 해결 시작 및 결과 검색</span><span class="sxs-lookup"><span data-stu-id="6ff0b-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="6ff0b-114">위의 샘플은 가상 네트워크 게이트웨이에서 문제 해결을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="6ff0b-115">작업을 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="6ff0b-116">문제 해결이 시작된 후 Get-AzNetworkWatcherTroubleshootingResult 결과를 검색하기 위해 리소스에 대한 호출을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="6ff0b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ff0b-117">PARAMETERS</span></span>

### <span data-ttu-id="6ff0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff0b-118">-DefaultProfile</span></span>
<span data-ttu-id="6ff0b-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ff0b-120">-Location</span><span class="sxs-lookup"><span data-stu-id="6ff0b-120">-Location</span></span>
<span data-ttu-id="6ff0b-121">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6ff0b-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0b-122">-NetworkWatcher</span></span>
<span data-ttu-id="6ff0b-123">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="6ff0b-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6ff0b-124">-NetworkWatcherName</span></span>
<span data-ttu-id="6ff0b-125">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="6ff0b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff0b-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ff0b-127">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6ff0b-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6ff0b-128">-TargetResourceId</span></span>
<span data-ttu-id="6ff0b-129">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-129">The target resource ID.</span></span>

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

### <span data-ttu-id="6ff0b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff0b-130">CommonParameters</span></span>
<span data-ttu-id="6ff0b-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff0b-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ff0b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff0b-133">입력</span><span class="sxs-lookup"><span data-stu-id="6ff0b-133">INPUTS</span></span>

### <span data-ttu-id="6ff0b-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0b-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6ff0b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6ff0b-135">System.String</span></span>

## <span data-ttu-id="6ff0b-136">출력</span><span class="sxs-lookup"><span data-stu-id="6ff0b-136">OUTPUTS</span></span>

### <span data-ttu-id="6ff0b-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6ff0b-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="6ff0b-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ff0b-138">NOTES</span></span>
<span data-ttu-id="6ff0b-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="6ff0b-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="6ff0b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ff0b-140">RELATED LINKS</span></span>

[<span data-ttu-id="6ff0b-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0b-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6ff0b-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0b-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6ff0b-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0b-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6ff0b-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6ff0b-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6ff0b-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6ff0b-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6ff0b-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6ff0b-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6ff0b-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6ff0b-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6ff0b-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6ff0b-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6ff0b-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6ff0b-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6ff0b-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6ff0b-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6ff0b-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6ff0b-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6ff0b-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6ff0b-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6ff0b-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ff0b-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6ff0b-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6ff0b-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6ff0b-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6ff0b-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6ff0b-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0b-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0b-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0b-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0b-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0b-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0b-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6ff0b-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6ff0b-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0b-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0b-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0b-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0b-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6ff0b-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6ff0b-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6ff0b-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6ff0b-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6ff0b-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6ff0b-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6ff0b-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6ff0b-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6ff0b-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6ff0b-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0b-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)