---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226677"
---
# <span data-ttu-id="da88b-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="da88b-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="da88b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da88b-102">SYNOPSIS</span></span>
<span data-ttu-id="da88b-103">VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="da88b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da88b-104">SYNTAX</span></span>

### <span data-ttu-id="da88b-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="da88b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da88b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="da88b-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da88b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="da88b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da88b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="da88b-108">DESCRIPTION</span></span>
<span data-ttu-id="da88b-109">Get-AzNetworkWatcherSecurityGroupView를 사용 하 여 VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="da88b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="da88b-110">EXAMPLES</span></span>

### <span data-ttu-id="da88b-111">예제 1: VM에서 보안 그룹 보기 호출 하기</span><span class="sxs-lookup"><span data-stu-id="da88b-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="da88b-112">위 예제에서는 먼저 지역 네트워크 감시자를 얻은 다음 지역에서 VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="da88b-113">그런 다음 지정 된 VM에서 보안 그룹 보기 호출을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="da88b-114">변수</span><span class="sxs-lookup"><span data-stu-id="da88b-114">PARAMETERS</span></span>

### <span data-ttu-id="da88b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da88b-115">-AsJob</span></span>
<span data-ttu-id="da88b-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="da88b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da88b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da88b-117">-DefaultProfile</span></span>
<span data-ttu-id="da88b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da88b-119">-위치</span><span class="sxs-lookup"><span data-stu-id="da88b-119">-Location</span></span>
<span data-ttu-id="da88b-120">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="da88b-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da88b-121">-NetworkWatcher</span></span>
<span data-ttu-id="da88b-122">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="da88b-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="da88b-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="da88b-123">-NetworkWatcherName</span></span>
<span data-ttu-id="da88b-124">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="da88b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da88b-125">-ResourceGroupName</span></span>
<span data-ttu-id="da88b-126">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="da88b-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="da88b-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="da88b-128">대상 VM Id</span><span class="sxs-lookup"><span data-stu-id="da88b-128">The target VM Id</span></span>

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

### <span data-ttu-id="da88b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da88b-129">CommonParameters</span></span>
<span data-ttu-id="da88b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da88b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da88b-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da88b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da88b-132">입력</span><span class="sxs-lookup"><span data-stu-id="da88b-132">INPUTS</span></span>

### <span data-ttu-id="da88b-133">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da88b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="da88b-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da88b-134">System.String</span></span>

## <span data-ttu-id="da88b-135">출력</span><span class="sxs-lookup"><span data-stu-id="da88b-135">OUTPUTS</span></span>

### <span data-ttu-id="da88b-136">Microsoft. 네트워크 모델. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="da88b-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="da88b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="da88b-137">NOTES</span></span>
<span data-ttu-id="da88b-138">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="da88b-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="da88b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da88b-139">RELATED LINKS</span></span>

[<span data-ttu-id="da88b-140">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da88b-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="da88b-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da88b-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="da88b-142">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da88b-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="da88b-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="da88b-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="da88b-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="da88b-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="da88b-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="da88b-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="da88b-146">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="da88b-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="da88b-147">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da88b-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da88b-148">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="da88b-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="da88b-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da88b-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da88b-150">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da88b-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da88b-151">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da88b-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da88b-152">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="da88b-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="da88b-153">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="da88b-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="da88b-154">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="da88b-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="da88b-155">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="da88b-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="da88b-156">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="da88b-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="da88b-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="da88b-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="da88b-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="da88b-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="da88b-159">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="da88b-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="da88b-160">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="da88b-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="da88b-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="da88b-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="da88b-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="da88b-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="da88b-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="da88b-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="da88b-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="da88b-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="da88b-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="da88b-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="da88b-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="da88b-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
