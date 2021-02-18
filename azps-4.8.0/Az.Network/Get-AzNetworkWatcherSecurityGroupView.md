---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: ec1b53799b92f0a68c20110dfe78f9af7b8391c2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410415"
---
# <span data-ttu-id="d2e64-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d2e64-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="d2e64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e64-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e64-103">VM에 적용된 구성된 유효 네트워크 보안 그룹 규칙을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="d2e64-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2e64-104">SYNTAX</span></span>

### <span data-ttu-id="d2e64-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="d2e64-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e64-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d2e64-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e64-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d2e64-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e64-108">설명</span><span class="sxs-lookup"><span data-stu-id="d2e64-108">DESCRIPTION</span></span>
<span data-ttu-id="d2e64-109">이 Get-AzNetworkWatcherSecurityGroupView VM에 적용된 구성되고 효과적인 네트워크 보안 그룹 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="d2e64-110">예제</span><span class="sxs-lookup"><span data-stu-id="d2e64-110">EXAMPLES</span></span>

### <span data-ttu-id="d2e64-111">예제 1: VM에서 보안 그룹 보기 호출</span><span class="sxs-lookup"><span data-stu-id="d2e64-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="d2e64-112">위의 예제에서는 먼저 지역 Network Watcher를, 해당 지역의 VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="d2e64-113">그런 다음 지정된 VM에서 보안 그룹 보기를 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="d2e64-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2e64-114">PARAMETERS</span></span>

### <span data-ttu-id="d2e64-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2e64-115">-AsJob</span></span>
<span data-ttu-id="d2e64-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d2e64-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2e64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e64-117">-DefaultProfile</span></span>
<span data-ttu-id="d2e64-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e64-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d2e64-119">-Location</span></span>
<span data-ttu-id="d2e64-120">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d2e64-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2e64-121">-NetworkWatcher</span></span>
<span data-ttu-id="d2e64-122">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="d2e64-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d2e64-123">-NetworkWatcherName</span></span>
<span data-ttu-id="d2e64-124">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="d2e64-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e64-125">-ResourceGroupName</span></span>
<span data-ttu-id="d2e64-126">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d2e64-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d2e64-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d2e64-128">대상 VM ID</span><span class="sxs-lookup"><span data-stu-id="d2e64-128">The target VM Id</span></span>

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

### <span data-ttu-id="d2e64-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e64-129">CommonParameters</span></span>
<span data-ttu-id="d2e64-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e64-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e64-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2e64-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e64-132">입력</span><span class="sxs-lookup"><span data-stu-id="d2e64-132">INPUTS</span></span>

### <span data-ttu-id="d2e64-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2e64-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d2e64-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d2e64-134">System.String</span></span>

## <span data-ttu-id="d2e64-135">출력</span><span class="sxs-lookup"><span data-stu-id="d2e64-135">OUTPUTS</span></span>

### <span data-ttu-id="d2e64-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="d2e64-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="d2e64-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2e64-137">NOTES</span></span>
<span data-ttu-id="d2e64-138">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, IP</span><span class="sxs-lookup"><span data-stu-id="d2e64-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="d2e64-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2e64-139">RELATED LINKS</span></span>

[<span data-ttu-id="d2e64-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2e64-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d2e64-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2e64-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d2e64-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d2e64-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d2e64-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d2e64-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d2e64-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d2e64-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d2e64-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d2e64-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d2e64-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d2e64-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d2e64-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2e64-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2e64-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d2e64-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d2e64-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2e64-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2e64-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2e64-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2e64-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2e64-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2e64-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2e64-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d2e64-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d2e64-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d2e64-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d2e64-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d2e64-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2e64-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2e64-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2e64-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2e64-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2e64-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2e64-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d2e64-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d2e64-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2e64-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2e64-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2e64-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d2e64-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d2e64-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d2e64-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d2e64-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d2e64-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d2e64-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d2e64-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d2e64-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d2e64-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d2e64-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d2e64-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d2e64-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
