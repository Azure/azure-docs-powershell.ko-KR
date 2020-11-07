---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: f40b7e28bce34ef9e4cc289bed7f8c4524ef49d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870117"
---
# <span data-ttu-id="3d5a6-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3d5a6-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="3d5a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5a6-103">VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="3d5a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d5a6-104">SYNTAX</span></span>

### <span data-ttu-id="3d5a6-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d5a6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d5a6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3d5a6-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d5a6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3d5a6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d5a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3d5a6-108">DESCRIPTION</span></span>
<span data-ttu-id="3d5a6-109">Get-AzNetworkWatcherSecurityGroupView를 사용 하 여 VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="3d5a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3d5a6-110">EXAMPLES</span></span>

### <span data-ttu-id="3d5a6-111">예제 1: VM에서 보안 그룹 보기 호출 하기</span><span class="sxs-lookup"><span data-stu-id="3d5a6-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="3d5a6-112">위 예제에서는 먼저 지역 네트워크 감시자를 얻은 다음 지역에서 VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="3d5a6-113">그런 다음 지정 된 VM에서 보안 그룹 보기 호출을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="3d5a6-114">변수</span><span class="sxs-lookup"><span data-stu-id="3d5a6-114">PARAMETERS</span></span>

### <span data-ttu-id="3d5a6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d5a6-115">-AsJob</span></span>
<span data-ttu-id="3d5a6-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3d5a6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d5a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5a6-117">-DefaultProfile</span></span>
<span data-ttu-id="3d5a6-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d5a6-119">-위치</span><span class="sxs-lookup"><span data-stu-id="3d5a6-119">-Location</span></span>
<span data-ttu-id="3d5a6-120">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3d5a6-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5a6-121">-NetworkWatcher</span></span>
<span data-ttu-id="3d5a6-122">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="3d5a6-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3d5a6-123">-NetworkWatcherName</span></span>
<span data-ttu-id="3d5a6-124">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="3d5a6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d5a6-125">-ResourceGroupName</span></span>
<span data-ttu-id="3d5a6-126">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3d5a6-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3d5a6-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="3d5a6-128">대상 VM Id</span><span class="sxs-lookup"><span data-stu-id="3d5a6-128">The target VM Id</span></span>

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

### <span data-ttu-id="3d5a6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5a6-129">CommonParameters</span></span>
<span data-ttu-id="3d5a6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5a6-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d5a6-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5a6-132">입력</span><span class="sxs-lookup"><span data-stu-id="3d5a6-132">INPUTS</span></span>

### <span data-ttu-id="3d5a6-133">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5a6-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3d5a6-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d5a6-134">System.String</span></span>

## <span data-ttu-id="3d5a6-135">출력</span><span class="sxs-lookup"><span data-stu-id="3d5a6-135">OUTPUTS</span></span>

### <span data-ttu-id="3d5a6-136">Microsoft. 네트워크 모델. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="3d5a6-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="3d5a6-137">상속자</span><span class="sxs-lookup"><span data-stu-id="3d5a6-137">NOTES</span></span>
<span data-ttu-id="3d5a6-138">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="3d5a6-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="3d5a6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d5a6-139">RELATED LINKS</span></span>

[<span data-ttu-id="3d5a6-140">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5a6-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3d5a6-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5a6-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3d5a6-142">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d5a6-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3d5a6-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3d5a6-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3d5a6-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3d5a6-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3d5a6-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3d5a6-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3d5a6-146">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3d5a6-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3d5a6-147">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d5a6-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d5a6-148">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3d5a6-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3d5a6-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d5a6-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d5a6-150">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d5a6-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d5a6-151">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d5a6-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d5a6-152">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d5a6-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3d5a6-153">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3d5a6-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3d5a6-154">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3d5a6-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3d5a6-155">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d5a6-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d5a6-156">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d5a6-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d5a6-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d5a6-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d5a6-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3d5a6-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3d5a6-159">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d5a6-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d5a6-160">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d5a6-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d5a6-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3d5a6-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3d5a6-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3d5a6-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3d5a6-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3d5a6-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3d5a6-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3d5a6-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3d5a6-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3d5a6-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="3d5a6-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d5a6-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
