---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5399c97f076f1402b20b91798d2db215d00af8b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699942"
---
# <span data-ttu-id="b60d8-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b60d8-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="b60d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b60d8-103">Azure에서 네트워킹 리소스에 대 한 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="b60d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b60d8-104">SYNTAX</span></span>

### <span data-ttu-id="b60d8-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="b60d8-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b60d8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b60d8-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b60d8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b60d8-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b60d8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b60d8-108">DESCRIPTION</span></span>
<span data-ttu-id="b60d8-109">Start-AzNetworkWatcherResourceTroubleshooting cmdlet은 Azure에서 네트워킹 리소스에 대 한 문제 해결을 시작 하 고 잠재적인 문제 및 완화에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="b60d8-110">현재 가상 네트워크 게이트웨이 및 연결이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="b60d8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b60d8-111">EXAMPLES</span></span>

### <span data-ttu-id="b60d8-112">예제 1: 가상 네트워크 게이트웨이에서 문제 해결 시작</span><span class="sxs-lookup"><span data-stu-id="b60d8-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="b60d8-113">위의 샘플에서는 가상 네트워크 게이트웨이에서 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="b60d8-114">작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="b60d8-115">변수</span><span class="sxs-lookup"><span data-stu-id="b60d8-115">PARAMETERS</span></span>

### <span data-ttu-id="b60d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60d8-116">-DefaultProfile</span></span>
<span data-ttu-id="b60d8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60d8-118">-위치</span><span class="sxs-lookup"><span data-stu-id="b60d8-118">-Location</span></span>
<span data-ttu-id="b60d8-119">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b60d8-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b60d8-120">-NetworkWatcher</span></span>
<span data-ttu-id="b60d8-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="b60d8-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="b60d8-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b60d8-122">-NetworkWatcherName</span></span>
<span data-ttu-id="b60d8-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="b60d8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60d8-124">-ResourceGroupName</span></span>
<span data-ttu-id="b60d8-125">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b60d8-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="b60d8-126">-StorageId</span></span>
<span data-ttu-id="b60d8-127">저장소 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-127">The storage ID.</span></span>

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

### <span data-ttu-id="b60d8-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="b60d8-128">-StoragePath</span></span>
<span data-ttu-id="b60d8-129">저장소 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-129">The storage path.</span></span>

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

### <span data-ttu-id="b60d8-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b60d8-130">-TargetResourceId</span></span>
<span data-ttu-id="b60d8-131">문제를 해결할 리소스의 리소스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="b60d8-132">예제 형식: "/subscriptions/$ {subscriptionId}/resourceGroups//$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="b60d8-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="b60d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60d8-133">CommonParameters</span></span>
<span data-ttu-id="b60d8-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b60d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60d8-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60d8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60d8-136">입력</span><span class="sxs-lookup"><span data-stu-id="b60d8-136">INPUTS</span></span>

### <span data-ttu-id="b60d8-137">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b60d8-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b60d8-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b60d8-138">System.String</span></span>

## <span data-ttu-id="b60d8-139">출력</span><span class="sxs-lookup"><span data-stu-id="b60d8-139">OUTPUTS</span></span>

### <span data-ttu-id="b60d8-140">PSTroubleshootingResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b60d8-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="b60d8-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b60d8-141">NOTES</span></span>
<span data-ttu-id="b60d8-142">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="b60d8-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="b60d8-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b60d8-143">RELATED LINKS</span></span>

[<span data-ttu-id="b60d8-144">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b60d8-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b60d8-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b60d8-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b60d8-146">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b60d8-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b60d8-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b60d8-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b60d8-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b60d8-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b60d8-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b60d8-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b60d8-150">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b60d8-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b60d8-151">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b60d8-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b60d8-152">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b60d8-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b60d8-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b60d8-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b60d8-154">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b60d8-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b60d8-155">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b60d8-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b60d8-156">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b60d8-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b60d8-157">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b60d8-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b60d8-158">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b60d8-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b60d8-159">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b60d8-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b60d8-160">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b60d8-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b60d8-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b60d8-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b60d8-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b60d8-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b60d8-163">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b60d8-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b60d8-164">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b60d8-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b60d8-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b60d8-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b60d8-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b60d8-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b60d8-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b60d8-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b60d8-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b60d8-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b60d8-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b60d8-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b60d8-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b60d8-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)