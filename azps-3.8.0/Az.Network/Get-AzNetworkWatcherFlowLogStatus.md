---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2b24877b155695e7a080fc4b06823548572e550f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878165"
---
# <span data-ttu-id="ea9a3-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ea9a3-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="ea9a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9a3-103">리소스에 대 한 흐름 로깅의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="ea9a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea9a3-104">SYNTAX</span></span>

### <span data-ttu-id="ea9a3-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea9a3-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea9a3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ea9a3-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea9a3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ea9a3-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea9a3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ea9a3-108">DESCRIPTION</span></span>
<span data-ttu-id="ea9a3-109">Get-AzNetworkWatcherFlowLogStatus cmdlet은 리소스에 대 한 흐름 로깅의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="ea9a3-110">상태에는 제공 된 리소스에 대해 흐름 로깅이 사용 되는지 여부, 로그를 보낼 구성 된 저장소 계정, 로그에 대 한 보존 정책이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="ea9a3-111">현재 네트워크 보안 그룹은 유동 로깅에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="ea9a3-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ea9a3-112">EXAMPLES</span></span>

### <span data-ttu-id="ea9a3-113">예제 1: 지정 된 NSG에 대 한 흐름 로깅 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea9a3-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
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

<span data-ttu-id="ea9a3-114">이 예제에서는 네트워크 보안 그룹에 대 한 흐름 로깅 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="ea9a3-115">지정 된 NSG에 흐름 로깅 사용, 기본 형식 및 보존 정책 집합이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="ea9a3-116">예제 2: 지정 된 NSG에 대 한 흐름 로깅 및 트래픽 분석 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea9a3-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
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

<span data-ttu-id="ea9a3-117">이 예제에서는 네트워크 보안 그룹에 대 한 흐름 로깅 및 트래픽 분석 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="ea9a3-118">지정 된 NSG에 흐름 로깅 및 트래픽 분석을 사용 하도록 설정 하 고 기본 형식이 있으며 보존 정책이 설정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="ea9a3-119">변수</span><span class="sxs-lookup"><span data-stu-id="ea9a3-119">PARAMETERS</span></span>

### <span data-ttu-id="ea9a3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea9a3-120">-AsJob</span></span>
<span data-ttu-id="ea9a3-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ea9a3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea9a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9a3-122">-DefaultProfile</span></span>
<span data-ttu-id="ea9a3-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea9a3-124">-위치</span><span class="sxs-lookup"><span data-stu-id="ea9a3-124">-Location</span></span>
<span data-ttu-id="ea9a3-125">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ea9a3-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea9a3-126">-NetworkWatcher</span></span>
<span data-ttu-id="ea9a3-127">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="ea9a3-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ea9a3-128">-NetworkWatcherName</span></span>
<span data-ttu-id="ea9a3-129">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="ea9a3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea9a3-130">-ResourceGroupName</span></span>
<span data-ttu-id="ea9a3-131">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ea9a3-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ea9a3-132">-TargetResourceId</span></span>
<span data-ttu-id="ea9a3-133">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-133">The target resource ID.</span></span>

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

### <span data-ttu-id="ea9a3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9a3-134">CommonParameters</span></span>
<span data-ttu-id="ea9a3-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9a3-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea9a3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9a3-137">입력</span><span class="sxs-lookup"><span data-stu-id="ea9a3-137">INPUTS</span></span>

### <span data-ttu-id="ea9a3-138">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea9a3-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ea9a3-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea9a3-139">System.String</span></span>

## <span data-ttu-id="ea9a3-140">출력</span><span class="sxs-lookup"><span data-stu-id="ea9a3-140">OUTPUTS</span></span>

### <span data-ttu-id="ea9a3-141">Microsoft. 네트워크 모델. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="ea9a3-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="ea9a3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="ea9a3-142">NOTES</span></span>
<span data-ttu-id="ea9a3-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 흐름, 로그, flowlog, 로깅</span><span class="sxs-lookup"><span data-stu-id="ea9a3-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="ea9a3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea9a3-144">RELATED LINKS</span></span>

[<span data-ttu-id="ea9a3-145">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea9a3-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ea9a3-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea9a3-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ea9a3-147">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ea9a3-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ea9a3-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ea9a3-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ea9a3-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ea9a3-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ea9a3-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ea9a3-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ea9a3-151">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ea9a3-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ea9a3-152">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea9a3-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea9a3-153">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ea9a3-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ea9a3-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea9a3-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea9a3-155">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea9a3-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea9a3-156">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea9a3-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea9a3-157">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea9a3-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ea9a3-158">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ea9a3-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ea9a3-159">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ea9a3-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ea9a3-160">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ea9a3-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ea9a3-161">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ea9a3-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ea9a3-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ea9a3-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ea9a3-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ea9a3-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ea9a3-164">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ea9a3-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ea9a3-165">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ea9a3-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ea9a3-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ea9a3-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ea9a3-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ea9a3-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ea9a3-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ea9a3-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ea9a3-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ea9a3-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ea9a3-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ea9a3-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ea9a3-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ea9a3-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
