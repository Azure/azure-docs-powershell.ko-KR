---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f04fade3fcee4651c71432e7648fbec9725b6b01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951984"
---
# <span data-ttu-id="2f6cd-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f6cd-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2f6cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="2f6cd-103">연결 모니터 시작</span><span class="sxs-lookup"><span data-stu-id="2f6cd-103">Start a connection monitor</span></span>

## <span data-ttu-id="2f6cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f6cd-104">SYNTAX</span></span>

### <span data-ttu-id="2f6cd-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2f6cd-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f6cd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2f6cd-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f6cd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2f6cd-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f6cd-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f6cd-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f6cd-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f6cd-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f6cd-110">설명</span><span class="sxs-lookup"><span data-stu-id="2f6cd-110">DESCRIPTION</span></span>
<span data-ttu-id="2f6cd-111">Start-AzNetworkWatcherConnectionMonitor cmdlet이 지정된 연결 모니터를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="2f6cd-112">예제</span><span class="sxs-lookup"><span data-stu-id="2f6cd-112">EXAMPLES</span></span>

### <span data-ttu-id="2f6cd-113">예제 1: 연결 모니터 시작</span><span class="sxs-lookup"><span data-stu-id="2f6cd-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="2f6cd-114">이 예제에서는 이름 및 네트워크 감시자에 의해 지정된 연결 모니터를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="2f6cd-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2f6cd-115">PARAMETERS</span></span>

### <span data-ttu-id="2f6cd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f6cd-116">-AsJob</span></span>
<span data-ttu-id="2f6cd-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2f6cd-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f6cd-118">-DefaultProfile</span></span>
<span data-ttu-id="2f6cd-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f6cd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f6cd-120">-InputObject</span></span>
<span data-ttu-id="2f6cd-121">연결 모니터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-122">-Location</span><span class="sxs-lookup"><span data-stu-id="2f6cd-122">-Location</span></span>
<span data-ttu-id="2f6cd-123">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2f6cd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2f6cd-124">-Name</span></span>
<span data-ttu-id="2f6cd-125">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f6cd-126">-NetworkWatcher</span></span>
<span data-ttu-id="2f6cd-127">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="2f6cd-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2f6cd-128">-NetworkWatcherName</span></span>
<span data-ttu-id="2f6cd-129">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f6cd-130">-PassThru</span></span>
<span data-ttu-id="2f6cd-131">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-131">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f6cd-132">-ResourceGroupName</span></span>
<span data-ttu-id="2f6cd-133">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f6cd-134">-ResourceId</span></span>
<span data-ttu-id="2f6cd-135">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-136">-확인</span><span class="sxs-lookup"><span data-stu-id="2f6cd-136">-Confirm</span></span>
<span data-ttu-id="2f6cd-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f6cd-138">-WhatIf</span></span>
<span data-ttu-id="2f6cd-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f6cd-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f6cd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6cd-141">CommonParameters</span></span>
<span data-ttu-id="2f6cd-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f6cd-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2f6cd-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6cd-144">입력</span><span class="sxs-lookup"><span data-stu-id="2f6cd-144">INPUTS</span></span>

### <span data-ttu-id="2f6cd-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f6cd-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2f6cd-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2f6cd-146">System.String</span></span>

### <span data-ttu-id="2f6cd-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2f6cd-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="2f6cd-148">출력</span><span class="sxs-lookup"><span data-stu-id="2f6cd-148">OUTPUTS</span></span>

### <span data-ttu-id="2f6cd-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f6cd-149">System.Boolean</span></span>

## <span data-ttu-id="2f6cd-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f6cd-150">NOTES</span></span>
<span data-ttu-id="2f6cd-151">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="2f6cd-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="2f6cd-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f6cd-152">RELATED LINKS</span></span>

[<span data-ttu-id="2f6cd-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f6cd-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2f6cd-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f6cd-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2f6cd-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f6cd-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2f6cd-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2f6cd-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2f6cd-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2f6cd-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2f6cd-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2f6cd-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2f6cd-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2f6cd-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2f6cd-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f6cd-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f6cd-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2f6cd-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2f6cd-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f6cd-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f6cd-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f6cd-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f6cd-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f6cd-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f6cd-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f6cd-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f6cd-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2f6cd-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2f6cd-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f6cd-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f6cd-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f6cd-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f6cd-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f6cd-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f6cd-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f6cd-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f6cd-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f6cd-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2f6cd-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2f6cd-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2f6cd-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2f6cd-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2f6cd-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2f6cd-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2f6cd-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f6cd-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f6cd-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2f6cd-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2f6cd-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2f6cd-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2f6cd-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2f6cd-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2f6cd-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2f6cd-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
