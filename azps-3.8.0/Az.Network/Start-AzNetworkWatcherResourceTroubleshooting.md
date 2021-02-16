---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5f707b4e6a2610f8a62ce807c5549ee03e6697d8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408834"
---
# <span data-ttu-id="96493-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="96493-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="96493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96493-102">SYNOPSIS</span></span>
<span data-ttu-id="96493-103">Azure의 네트워킹 리소스에서 문제 해결을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="96493-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="96493-104">구문</span><span class="sxs-lookup"><span data-stu-id="96493-104">SYNTAX</span></span>

### <span data-ttu-id="96493-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="96493-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96493-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="96493-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96493-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="96493-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96493-108">설명</span><span class="sxs-lookup"><span data-stu-id="96493-108">DESCRIPTION</span></span>
<span data-ttu-id="96493-109">이 Start-AzNetworkWatcherResourceTroubleshooting cmdlet은 Azure의 네트워킹 리소스에 대한 문제 해결을 시작하고 잠재적인 문제 및 완화에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="96493-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="96493-110">현재 Virtual Network 게이트웨이 및 연결이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="96493-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="96493-111">예제</span><span class="sxs-lookup"><span data-stu-id="96493-111">EXAMPLES</span></span>

### <span data-ttu-id="96493-112">예제 1: Virtual Network 게이트웨이에서 문제 해결 시작</span><span class="sxs-lookup"><span data-stu-id="96493-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="96493-113">위의 샘플은 가상 네트워크 게이트웨이에서 문제 해결을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="96493-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="96493-114">작업을 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96493-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="96493-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96493-115">PARAMETERS</span></span>

### <span data-ttu-id="96493-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96493-116">-DefaultProfile</span></span>
<span data-ttu-id="96493-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96493-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96493-118">-Location</span><span class="sxs-lookup"><span data-stu-id="96493-118">-Location</span></span>
<span data-ttu-id="96493-119">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="96493-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="96493-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96493-120">-NetworkWatcher</span></span>
<span data-ttu-id="96493-121">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="96493-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="96493-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="96493-122">-NetworkWatcherName</span></span>
<span data-ttu-id="96493-123">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96493-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="96493-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96493-124">-ResourceGroupName</span></span>
<span data-ttu-id="96493-125">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96493-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="96493-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="96493-126">-StorageId</span></span>
<span data-ttu-id="96493-127">저장소 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="96493-127">The storage ID.</span></span>

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

### <span data-ttu-id="96493-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="96493-128">-StoragePath</span></span>
<span data-ttu-id="96493-129">저장소 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="96493-129">The storage path.</span></span>

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

### <span data-ttu-id="96493-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="96493-130">-TargetResourceId</span></span>
<span data-ttu-id="96493-131">문제를 해결할 리소스의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="96493-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="96493-132">예제 형식: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="96493-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="96493-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96493-133">CommonParameters</span></span>
<span data-ttu-id="96493-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96493-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96493-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96493-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96493-136">입력</span><span class="sxs-lookup"><span data-stu-id="96493-136">INPUTS</span></span>

### <span data-ttu-id="96493-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96493-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="96493-138">System.String</span><span class="sxs-lookup"><span data-stu-id="96493-138">System.String</span></span>

## <span data-ttu-id="96493-139">출력</span><span class="sxs-lookup"><span data-stu-id="96493-139">OUTPUTS</span></span>

### <span data-ttu-id="96493-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="96493-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="96493-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96493-141">NOTES</span></span>
<span data-ttu-id="96493-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="96493-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="96493-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96493-143">RELATED LINKS</span></span>

[<span data-ttu-id="96493-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96493-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="96493-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96493-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="96493-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="96493-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="96493-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="96493-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="96493-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="96493-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="96493-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="96493-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="96493-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="96493-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="96493-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96493-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="96493-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="96493-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="96493-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96493-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="96493-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96493-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="96493-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96493-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="96493-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="96493-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="96493-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="96493-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="96493-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="96493-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="96493-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="96493-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="96493-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="96493-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="96493-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="96493-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="96493-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="96493-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="96493-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="96493-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="96493-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="96493-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="96493-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="96493-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="96493-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="96493-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="96493-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="96493-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="96493-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="96493-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="96493-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="96493-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="96493-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="96493-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
