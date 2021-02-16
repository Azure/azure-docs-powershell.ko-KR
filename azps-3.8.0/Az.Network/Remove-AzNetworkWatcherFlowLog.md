---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5c8532502e4e74b94a9d0c1e252c8d1cea9ddad8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398599"
---
# <span data-ttu-id="32ee5-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="32ee5-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="32ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="32ee5-103">지정된 흐름 로그 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="32ee5-104">구문</span><span class="sxs-lookup"><span data-stu-id="32ee5-104">SYNTAX</span></span>

### <span data-ttu-id="32ee5-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="32ee5-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ee5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="32ee5-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ee5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="32ee5-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ee5-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="32ee5-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ee5-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="32ee5-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32ee5-110">설명</span><span class="sxs-lookup"><span data-stu-id="32ee5-110">DESCRIPTION</span></span>
<span data-ttu-id="32ee5-111">지정된 흐름 로그 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="32ee5-112">예제</span><span class="sxs-lookup"><span data-stu-id="32ee5-112">EXAMPLES</span></span>

### <span data-ttu-id="32ee5-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="32ee5-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="32ee5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32ee5-114">PARAMETERS</span></span>

### <span data-ttu-id="32ee5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32ee5-115">-AsJob</span></span>
<span data-ttu-id="32ee5-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="32ee5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32ee5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ee5-117">-DefaultProfile</span></span>
<span data-ttu-id="32ee5-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32ee5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32ee5-119">-InputObject</span></span>
<span data-ttu-id="32ee5-120">흐름 로그 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-120">Flow log object.</span></span>

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

### <span data-ttu-id="32ee5-121">-Location</span><span class="sxs-lookup"><span data-stu-id="32ee5-121">-Location</span></span>
<span data-ttu-id="32ee5-122">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="32ee5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="32ee5-123">-Name</span></span>
<span data-ttu-id="32ee5-124">흐름 로그 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-124">The flow log name.</span></span>

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

### <span data-ttu-id="32ee5-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32ee5-125">-NetworkWatcher</span></span>
<span data-ttu-id="32ee5-126">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="32ee5-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="32ee5-127">-NetworkWatcherName</span></span>
<span data-ttu-id="32ee5-128">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="32ee5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32ee5-129">-PassThru</span></span>
<span data-ttu-id="32ee5-130">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="32ee5-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="32ee5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32ee5-131">-ResourceGroupName</span></span>
<span data-ttu-id="32ee5-132">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="32ee5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32ee5-133">-ResourceId</span></span>
<span data-ttu-id="32ee5-134">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-134">Resource ID.</span></span>

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

### <span data-ttu-id="32ee5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32ee5-135">-Confirm</span></span>
<span data-ttu-id="32ee5-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32ee5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32ee5-137">-WhatIf</span></span>
<span data-ttu-id="32ee5-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="32ee5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32ee5-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32ee5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ee5-140">CommonParameters</span></span>
<span data-ttu-id="32ee5-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32ee5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ee5-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32ee5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ee5-143">입력</span><span class="sxs-lookup"><span data-stu-id="32ee5-143">INPUTS</span></span>

### <span data-ttu-id="32ee5-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32ee5-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="32ee5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="32ee5-145">System.String</span></span>

### <span data-ttu-id="32ee5-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="32ee5-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="32ee5-147">출력</span><span class="sxs-lookup"><span data-stu-id="32ee5-147">OUTPUTS</span></span>

### <span data-ttu-id="32ee5-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32ee5-148">System.Boolean</span></span>

## <span data-ttu-id="32ee5-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32ee5-149">NOTES</span></span>

## <span data-ttu-id="32ee5-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32ee5-150">RELATED LINKS</span></span>

[<span data-ttu-id="32ee5-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32ee5-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="32ee5-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32ee5-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="32ee5-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32ee5-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="32ee5-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="32ee5-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="32ee5-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="32ee5-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="32ee5-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="32ee5-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="32ee5-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="32ee5-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="32ee5-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32ee5-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32ee5-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="32ee5-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="32ee5-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32ee5-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32ee5-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32ee5-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32ee5-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32ee5-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32ee5-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="32ee5-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="32ee5-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="32ee5-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="32ee5-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="32ee5-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="32ee5-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32ee5-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32ee5-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32ee5-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32ee5-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32ee5-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32ee5-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="32ee5-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="32ee5-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32ee5-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32ee5-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32ee5-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32ee5-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="32ee5-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="32ee5-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="32ee5-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="32ee5-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="32ee5-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="32ee5-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="32ee5-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="32ee5-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="32ee5-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="32ee5-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32ee5-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32ee5-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="32ee5-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="32ee5-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="32ee5-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="32ee5-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="32ee5-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)
