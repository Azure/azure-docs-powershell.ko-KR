---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 4886277bb994e0fe3a33645916660658a8367f1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951995"
---
# <span data-ttu-id="c7d2c-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c7d2c-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="c7d2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d2c-103">Azure의 네트워킹 리소스에서 문제 해결을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="c7d2c-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7d2c-104">SYNTAX</span></span>

### <span data-ttu-id="c7d2c-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="c7d2c-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d2c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c7d2c-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d2c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c7d2c-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d2c-108">설명</span><span class="sxs-lookup"><span data-stu-id="c7d2c-108">DESCRIPTION</span></span>
<span data-ttu-id="c7d2c-109">Start-AzNetworkWatcherResourceTroubleshooting cmdlet은 Azure의 네트워킹 리소스에 대한 문제 해결을 시작하고 잠재적인 문제 및 완화에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="c7d2c-110">현재 Virtual Network Gateway 및 연결이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="c7d2c-111">예제</span><span class="sxs-lookup"><span data-stu-id="c7d2c-111">EXAMPLES</span></span>

### <span data-ttu-id="c7d2c-112">예제 1: 가상 네트워크 게이트웨이에서 문제 해결 시작</span><span class="sxs-lookup"><span data-stu-id="c7d2c-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="c7d2c-113">위의 샘플은 가상 네트워크 게이트웨이에서 문제 해결을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="c7d2c-114">작업을 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="c7d2c-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c7d2c-115">PARAMETERS</span></span>

### <span data-ttu-id="c7d2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d2c-116">-DefaultProfile</span></span>
<span data-ttu-id="c7d2c-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7d2c-118">-Location</span><span class="sxs-lookup"><span data-stu-id="c7d2c-118">-Location</span></span>
<span data-ttu-id="c7d2c-119">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c7d2c-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d2c-120">-NetworkWatcher</span></span>
<span data-ttu-id="c7d2c-121">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="c7d2c-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c7d2c-122">-NetworkWatcherName</span></span>
<span data-ttu-id="c7d2c-123">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="c7d2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7d2c-125">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c7d2c-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="c7d2c-126">-StorageId</span></span>
<span data-ttu-id="c7d2c-127">저장소 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-127">The storage ID.</span></span>

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

### <span data-ttu-id="c7d2c-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="c7d2c-128">-StoragePath</span></span>
<span data-ttu-id="c7d2c-129">저장소 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-129">The storage path.</span></span>

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

### <span data-ttu-id="c7d2c-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c7d2c-130">-TargetResourceId</span></span>
<span data-ttu-id="c7d2c-131">문제 해결을 위한 리소스의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="c7d2c-132">예제 형식: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="c7d2c-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="c7d2c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d2c-133">CommonParameters</span></span>
<span data-ttu-id="c7d2c-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d2c-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c7d2c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d2c-136">입력</span><span class="sxs-lookup"><span data-stu-id="c7d2c-136">INPUTS</span></span>

### <span data-ttu-id="c7d2c-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d2c-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c7d2c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c7d2c-138">System.String</span></span>

## <span data-ttu-id="c7d2c-139">출력</span><span class="sxs-lookup"><span data-stu-id="c7d2c-139">OUTPUTS</span></span>

### <span data-ttu-id="c7d2c-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c7d2c-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="c7d2c-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7d2c-141">NOTES</span></span>
<span data-ttu-id="c7d2c-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="c7d2c-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="c7d2c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7d2c-143">RELATED LINKS</span></span>

[<span data-ttu-id="c7d2c-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d2c-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c7d2c-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d2c-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c7d2c-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7d2c-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c7d2c-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c7d2c-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c7d2c-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c7d2c-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c7d2c-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c7d2c-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c7d2c-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c7d2c-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c7d2c-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7d2c-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7d2c-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c7d2c-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c7d2c-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7d2c-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7d2c-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7d2c-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7d2c-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7d2c-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c7d2c-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7d2c-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c7d2c-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c7d2c-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c7d2c-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c7d2c-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c7d2c-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d2c-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d2c-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d2c-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d2c-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d2c-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d2c-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7d2c-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c7d2c-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d2c-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d2c-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d2c-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c7d2c-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c7d2c-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c7d2c-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c7d2c-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c7d2c-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c7d2c-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c7d2c-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c7d2c-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c7d2c-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c7d2c-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c7d2c-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7d2c-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
