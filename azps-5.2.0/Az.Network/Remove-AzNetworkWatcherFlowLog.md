---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 9906af7da12f76650ebbe45ff764da78c90ef340
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345122"
---
# <span data-ttu-id="4acd6-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4acd6-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="4acd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4acd6-102">SYNOPSIS</span></span>
<span data-ttu-id="4acd6-103">지정된 흐름 로그 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="4acd6-104">구문</span><span class="sxs-lookup"><span data-stu-id="4acd6-104">SYNTAX</span></span>

### <span data-ttu-id="4acd6-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4acd6-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4acd6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4acd6-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4acd6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4acd6-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4acd6-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4acd6-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4acd6-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4acd6-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4acd6-110">설명</span><span class="sxs-lookup"><span data-stu-id="4acd6-110">DESCRIPTION</span></span>
<span data-ttu-id="4acd6-111">지정된 흐름 로그 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="4acd6-112">예제</span><span class="sxs-lookup"><span data-stu-id="4acd6-112">EXAMPLES</span></span>

### <span data-ttu-id="4acd6-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="4acd6-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="4acd6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4acd6-114">PARAMETERS</span></span>

### <span data-ttu-id="4acd6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4acd6-115">-AsJob</span></span>
<span data-ttu-id="4acd6-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4acd6-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4acd6-117">-DefaultProfile</span></span>
<span data-ttu-id="4acd6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4acd6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4acd6-119">-InputObject</span></span>
<span data-ttu-id="4acd6-120">흐름 로그 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4acd6-121">-Location</span><span class="sxs-lookup"><span data-stu-id="4acd6-121">-Location</span></span>
<span data-ttu-id="4acd6-122">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4acd6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4acd6-123">-Name</span></span>
<span data-ttu-id="4acd6-124">흐름 로그 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd6-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4acd6-125">-NetworkWatcher</span></span>
<span data-ttu-id="4acd6-126">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="4acd6-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4acd6-127">-NetworkWatcherName</span></span>
<span data-ttu-id="4acd6-128">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="4acd6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4acd6-129">-PassThru</span></span>
<span data-ttu-id="4acd6-130">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="4acd6-130">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4acd6-131">-ResourceGroupName</span></span>
<span data-ttu-id="4acd6-132">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4acd6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4acd6-133">-ResourceId</span></span>
<span data-ttu-id="4acd6-134">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-134">Resource ID.</span></span>

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

### <span data-ttu-id="4acd6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4acd6-135">-Confirm</span></span>
<span data-ttu-id="4acd6-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4acd6-137">-WhatIf</span></span>
<span data-ttu-id="4acd6-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4acd6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4acd6-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4acd6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4acd6-140">CommonParameters</span></span>
<span data-ttu-id="4acd6-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4acd6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4acd6-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4acd6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4acd6-143">입력</span><span class="sxs-lookup"><span data-stu-id="4acd6-143">INPUTS</span></span>

### <span data-ttu-id="4acd6-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4acd6-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4acd6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4acd6-145">System.String</span></span>

### <span data-ttu-id="4acd6-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="4acd6-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="4acd6-147">출력</span><span class="sxs-lookup"><span data-stu-id="4acd6-147">OUTPUTS</span></span>

### <span data-ttu-id="4acd6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4acd6-148">System.Boolean</span></span>

## <span data-ttu-id="4acd6-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4acd6-149">NOTES</span></span>

## <span data-ttu-id="4acd6-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4acd6-150">RELATED LINKS</span></span>

[<span data-ttu-id="4acd6-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4acd6-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4acd6-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4acd6-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4acd6-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4acd6-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4acd6-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4acd6-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4acd6-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4acd6-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4acd6-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4acd6-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4acd6-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4acd6-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4acd6-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4acd6-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4acd6-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4acd6-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4acd6-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4acd6-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4acd6-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4acd6-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4acd6-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4acd6-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4acd6-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4acd6-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4acd6-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4acd6-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4acd6-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4acd6-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4acd6-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4acd6-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4acd6-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4acd6-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4acd6-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4acd6-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4acd6-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4acd6-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4acd6-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4acd6-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4acd6-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4acd6-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4acd6-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4acd6-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4acd6-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4acd6-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4acd6-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4acd6-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4acd6-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4acd6-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4acd6-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4acd6-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="4acd6-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4acd6-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="4acd6-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4acd6-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="4acd6-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4acd6-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="4acd6-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="4acd6-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
