---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c4e70253a42fc577ba283919fb3ab2eeb9701c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872106"
---
# <span data-ttu-id="59d1b-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="59d1b-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="59d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="59d1b-103">연결 모니터 시작</span><span class="sxs-lookup"><span data-stu-id="59d1b-103">Start a connection monitor</span></span>

## <span data-ttu-id="59d1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59d1b-104">SYNTAX</span></span>

### <span data-ttu-id="59d1b-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="59d1b-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d1b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="59d1b-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d1b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="59d1b-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d1b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="59d1b-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59d1b-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="59d1b-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d1b-110">설명은</span><span class="sxs-lookup"><span data-stu-id="59d1b-110">DESCRIPTION</span></span>
<span data-ttu-id="59d1b-111">Start-AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="59d1b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="59d1b-112">EXAMPLES</span></span>

### <span data-ttu-id="59d1b-113">예제 1: 연결 모니터 시작</span><span class="sxs-lookup"><span data-stu-id="59d1b-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="59d1b-114">이 예제에서는 이름 및 네트워크 감시자에 의해 지정 된 연결 모니터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="59d1b-115">변수</span><span class="sxs-lookup"><span data-stu-id="59d1b-115">PARAMETERS</span></span>

### <span data-ttu-id="59d1b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59d1b-116">-AsJob</span></span>
<span data-ttu-id="59d1b-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="59d1b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59d1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d1b-118">-DefaultProfile</span></span>
<span data-ttu-id="59d1b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d1b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59d1b-120">-InputObject</span></span>
<span data-ttu-id="59d1b-121">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="59d1b-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="59d1b-122">-위치</span><span class="sxs-lookup"><span data-stu-id="59d1b-122">-Location</span></span>
<span data-ttu-id="59d1b-123">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="59d1b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="59d1b-124">-Name</span></span>
<span data-ttu-id="59d1b-125">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="59d1b-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="59d1b-126">-NetworkWatcher</span></span>
<span data-ttu-id="59d1b-127">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="59d1b-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="59d1b-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="59d1b-128">-NetworkWatcherName</span></span>
<span data-ttu-id="59d1b-129">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="59d1b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59d1b-130">-PassThru</span></span>
<span data-ttu-id="59d1b-131">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="59d1b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d1b-132">-ResourceGroupName</span></span>
<span data-ttu-id="59d1b-133">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="59d1b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59d1b-134">-ResourceId</span></span>
<span data-ttu-id="59d1b-135">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-135">Resource ID.</span></span>

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

### <span data-ttu-id="59d1b-136">-확인</span><span class="sxs-lookup"><span data-stu-id="59d1b-136">-Confirm</span></span>
<span data-ttu-id="59d1b-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d1b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d1b-138">-WhatIf</span></span>
<span data-ttu-id="59d1b-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d1b-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d1b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d1b-141">CommonParameters</span></span>
<span data-ttu-id="59d1b-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59d1b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d1b-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d1b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d1b-144">입력</span><span class="sxs-lookup"><span data-stu-id="59d1b-144">INPUTS</span></span>

### <span data-ttu-id="59d1b-145">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="59d1b-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="59d1b-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="59d1b-146">System.String</span></span>

### <span data-ttu-id="59d1b-147">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="59d1b-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="59d1b-148">출력</span><span class="sxs-lookup"><span data-stu-id="59d1b-148">OUTPUTS</span></span>

### <span data-ttu-id="59d1b-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="59d1b-149">System.Boolean</span></span>

## <span data-ttu-id="59d1b-150">상속자</span><span class="sxs-lookup"><span data-stu-id="59d1b-150">NOTES</span></span>
<span data-ttu-id="59d1b-151">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="59d1b-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="59d1b-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59d1b-152">RELATED LINKS</span></span>

[<span data-ttu-id="59d1b-153">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="59d1b-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="59d1b-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="59d1b-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="59d1b-155">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="59d1b-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="59d1b-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="59d1b-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="59d1b-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="59d1b-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="59d1b-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="59d1b-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="59d1b-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="59d1b-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="59d1b-160">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="59d1b-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="59d1b-161">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="59d1b-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="59d1b-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="59d1b-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="59d1b-163">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="59d1b-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="59d1b-164">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="59d1b-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="59d1b-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="59d1b-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="59d1b-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="59d1b-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="59d1b-167">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="59d1b-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="59d1b-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="59d1b-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="59d1b-169">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="59d1b-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="59d1b-170">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="59d1b-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="59d1b-171">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="59d1b-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="59d1b-172">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="59d1b-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="59d1b-173">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="59d1b-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="59d1b-174">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="59d1b-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="59d1b-175">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="59d1b-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="59d1b-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="59d1b-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="59d1b-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="59d1b-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="59d1b-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="59d1b-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="59d1b-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="59d1b-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
