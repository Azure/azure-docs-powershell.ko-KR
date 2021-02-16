---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 8a2bde41d0e7e09acc1ad10a9901f0cf26334d02
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400504"
---
# <span data-ttu-id="64397-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="64397-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="64397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64397-102">SYNOPSIS</span></span>
<span data-ttu-id="64397-103">리소스에 대한 흐름 로깅 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64397-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="64397-104">구문</span><span class="sxs-lookup"><span data-stu-id="64397-104">SYNTAX</span></span>

### <span data-ttu-id="64397-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="64397-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64397-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="64397-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64397-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="64397-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64397-108">설명</span><span class="sxs-lookup"><span data-stu-id="64397-108">DESCRIPTION</span></span>
<span data-ttu-id="64397-109">Get-AzNetworkWatcherFlowLogStatus cmdlet은 리소스에 대한 흐름 로깅 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64397-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span>
<span data-ttu-id="64397-110">상태에는 제공된 리소스에 대해 흐름 로깅을 사용할 수 있는지 여부, 로그를 보낼 구성된 저장소 계정 및 로그에 대한 보존 정책이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="64397-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span>
<span data-ttu-id="64397-111">현재 네트워크 보안 그룹은 흐름 로깅에 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="64397-111">Currently Network Security Groups are supported for flow logging.</span></span>

## <span data-ttu-id="64397-112">예제</span><span class="sxs-lookup"><span data-stu-id="64397-112">EXAMPLES</span></span>

### <span data-ttu-id="64397-113">예제 1: 지정된 NSG에 대한 흐름 로깅 상태 확인</span><span class="sxs-lookup"><span data-stu-id="64397-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="64397-114">이 예제에서는 네트워크 보안 그룹에 대한 흐름 로깅 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64397-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="64397-115">지정된 NSG에는 흐름 로깅이 사용하도록 설정되어 있으며 기본 형식 및 보존 정책 집합이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="64397-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="64397-116">예제 2: 지정된 NSG에 대한 흐름 로깅 및 트래픽 분석 상태 확인</span><span class="sxs-lookup"><span data-stu-id="64397-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="64397-117">이 예제에서는 네트워크 보안 그룹에 대한 흐름 로깅 및 트래픽 분석 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="64397-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="64397-118">지정된 NSG에는 흐름 로깅 및 트래픽 분석이 사용하도록 설정되어 있으며 기본 형식 및 보존 정책 집합이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="64397-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="64397-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64397-119">PARAMETERS</span></span>

### <span data-ttu-id="64397-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64397-120">-AsJob</span></span>
<span data-ttu-id="64397-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="64397-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64397-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64397-122">-DefaultProfile</span></span>
<span data-ttu-id="64397-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64397-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64397-124">-Location</span><span class="sxs-lookup"><span data-stu-id="64397-124">-Location</span></span>
<span data-ttu-id="64397-125">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="64397-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="64397-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64397-126">-NetworkWatcher</span></span>
<span data-ttu-id="64397-127">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="64397-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="64397-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="64397-128">-NetworkWatcherName</span></span>
<span data-ttu-id="64397-129">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64397-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="64397-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64397-130">-ResourceGroupName</span></span>
<span data-ttu-id="64397-131">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64397-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="64397-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="64397-132">-TargetResourceId</span></span>
<span data-ttu-id="64397-133">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="64397-133">The target resource ID.</span></span>

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

### <span data-ttu-id="64397-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64397-134">CommonParameters</span></span>
<span data-ttu-id="64397-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64397-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64397-136">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64397-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64397-137">입력</span><span class="sxs-lookup"><span data-stu-id="64397-137">INPUTS</span></span>

### <span data-ttu-id="64397-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64397-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="64397-139">System.String</span><span class="sxs-lookup"><span data-stu-id="64397-139">System.String</span></span>

## <span data-ttu-id="64397-140">출력</span><span class="sxs-lookup"><span data-stu-id="64397-140">OUTPUTS</span></span>

### <span data-ttu-id="64397-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="64397-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="64397-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64397-142">NOTES</span></span>
<span data-ttu-id="64397-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 감시자, 흐름, 로그, 흐름 로그, 로깅</span><span class="sxs-lookup"><span data-stu-id="64397-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="64397-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64397-144">RELATED LINKS</span></span>

[<span data-ttu-id="64397-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64397-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="64397-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64397-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="64397-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="64397-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="64397-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="64397-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="64397-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="64397-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="64397-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="64397-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="64397-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="64397-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="64397-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64397-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64397-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="64397-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="64397-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64397-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64397-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64397-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64397-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="64397-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="64397-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="64397-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="64397-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="64397-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="64397-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="64397-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="64397-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64397-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64397-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64397-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64397-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64397-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64397-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="64397-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="64397-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64397-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64397-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64397-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="64397-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="64397-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="64397-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="64397-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="64397-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="64397-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="64397-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="64397-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="64397-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="64397-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="64397-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="64397-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
