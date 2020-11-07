---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 8296a680db76e1e7b3aedb15896f41ad0fba8e2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878169"
---
# <span data-ttu-id="055f2-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="055f2-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="055f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="055f2-102">SYNOPSIS</span></span>
<span data-ttu-id="055f2-103">지정 된 구독 및 지역에서 흐름 로그 리소스 또는 흐름 로그 리소스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="055f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="055f2-104">SYNTAX</span></span>

### <span data-ttu-id="055f2-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="055f2-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="055f2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="055f2-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="055f2-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="055f2-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="055f2-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="055f2-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="055f2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="055f2-109">DESCRIPTION</span></span>
<span data-ttu-id="055f2-110">지정 된 구독 및 지역에서 흐름 로그 리소스 또는 흐름 로그 리소스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="055f2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="055f2-111">EXAMPLES</span></span>

### <span data-ttu-id="055f2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="055f2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="055f2-113">이름: pstest Id:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid t e m/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag: W/ProvisioningState: 성공 위치: e us TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft./networkSecurityGroups StorageId: MyNSG s/Microsoft. Storage/Storageid/MySTorage 활성화 됨: 실제 보존 정책: {"일": true} 형식: {"유형": "JSON", "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": True, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "e", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/FlowLogsV2Demo/", "OperationalInsights": 60}</span><span class="sxs-lookup"><span data-stu-id="055f2-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="055f2-114">변수</span><span class="sxs-lookup"><span data-stu-id="055f2-114">PARAMETERS</span></span>

### <span data-ttu-id="055f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055f2-115">-DefaultProfile</span></span>
<span data-ttu-id="055f2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055f2-117">-위치</span><span class="sxs-lookup"><span data-stu-id="055f2-117">-Location</span></span>
<span data-ttu-id="055f2-118">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055f2-119">-이름</span><span class="sxs-lookup"><span data-stu-id="055f2-119">-Name</span></span>
<span data-ttu-id="055f2-120">흐름 로그 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055f2-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="055f2-121">-NetworkWatcher</span></span>
<span data-ttu-id="055f2-122">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="055f2-122">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="055f2-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="055f2-123">-NetworkWatcherName</span></span>
<span data-ttu-id="055f2-124">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055f2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="055f2-125">-ResourceGroupName</span></span>
<span data-ttu-id="055f2-126">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055f2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="055f2-127">-ResourceId</span></span>
<span data-ttu-id="055f2-128">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055f2-129">CommonParameters</span></span>
<span data-ttu-id="055f2-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="055f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055f2-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="055f2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055f2-132">입력</span><span class="sxs-lookup"><span data-stu-id="055f2-132">INPUTS</span></span>

### <span data-ttu-id="055f2-133">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="055f2-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="055f2-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="055f2-134">System.String</span></span>

## <span data-ttu-id="055f2-135">출력</span><span class="sxs-lookup"><span data-stu-id="055f2-135">OUTPUTS</span></span>

### <span data-ttu-id="055f2-136">Microsoft. 네트워크 모델. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="055f2-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="055f2-137">상속자</span><span class="sxs-lookup"><span data-stu-id="055f2-137">NOTES</span></span>

## <span data-ttu-id="055f2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="055f2-138">RELATED LINKS</span></span>

[<span data-ttu-id="055f2-139">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="055f2-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="055f2-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="055f2-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="055f2-141">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="055f2-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="055f2-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="055f2-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="055f2-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="055f2-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="055f2-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="055f2-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="055f2-145">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="055f2-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="055f2-146">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="055f2-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="055f2-147">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="055f2-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="055f2-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="055f2-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="055f2-149">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="055f2-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="055f2-150">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="055f2-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="055f2-151">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="055f2-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="055f2-152">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="055f2-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="055f2-153">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="055f2-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="055f2-154">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="055f2-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="055f2-155">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="055f2-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="055f2-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="055f2-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="055f2-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="055f2-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="055f2-158">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="055f2-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="055f2-159">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="055f2-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="055f2-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="055f2-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="055f2-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="055f2-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="055f2-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="055f2-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="055f2-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="055f2-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="055f2-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="055f2-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="055f2-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="055f2-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="055f2-166">새로운 AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="055f2-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog)

[<span data-ttu-id="055f2-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="055f2-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="055f2-168">제거-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="055f2-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog)
