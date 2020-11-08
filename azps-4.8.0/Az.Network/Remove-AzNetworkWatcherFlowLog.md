---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 9906af7da12f76650ebbe45ff764da78c90ef340
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203908"
---
# <span data-ttu-id="9cad4-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9cad4-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="9cad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cad4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cad4-103">지정 된 흐름 로그 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="9cad4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9cad4-104">SYNTAX</span></span>

### <span data-ttu-id="9cad4-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9cad4-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cad4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9cad4-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cad4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9cad4-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cad4-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9cad4-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cad4-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9cad4-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cad4-110">설명은</span><span class="sxs-lookup"><span data-stu-id="9cad4-110">DESCRIPTION</span></span>
<span data-ttu-id="9cad4-111">지정 된 흐름 로그 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="9cad4-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9cad4-112">EXAMPLES</span></span>

### <span data-ttu-id="9cad4-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9cad4-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="9cad4-114">변수</span><span class="sxs-lookup"><span data-stu-id="9cad4-114">PARAMETERS</span></span>

### <span data-ttu-id="9cad4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cad4-115">-AsJob</span></span>
<span data-ttu-id="9cad4-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9cad4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cad4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cad4-117">-DefaultProfile</span></span>
<span data-ttu-id="9cad4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cad4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cad4-119">-InputObject</span></span>
<span data-ttu-id="9cad4-120">흐름 로그 개체.</span><span class="sxs-lookup"><span data-stu-id="9cad4-120">Flow log object.</span></span>

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

### <span data-ttu-id="9cad4-121">-위치</span><span class="sxs-lookup"><span data-stu-id="9cad4-121">-Location</span></span>
<span data-ttu-id="9cad4-122">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9cad4-123">-이름</span><span class="sxs-lookup"><span data-stu-id="9cad4-123">-Name</span></span>
<span data-ttu-id="9cad4-124">흐름 로그 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-124">The flow log name.</span></span>

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

### <span data-ttu-id="9cad4-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9cad4-125">-NetworkWatcher</span></span>
<span data-ttu-id="9cad4-126">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="9cad4-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="9cad4-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9cad4-127">-NetworkWatcherName</span></span>
<span data-ttu-id="9cad4-128">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="9cad4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cad4-129">-PassThru</span></span>
<span data-ttu-id="9cad4-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="9cad4-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9cad4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cad4-131">-ResourceGroupName</span></span>
<span data-ttu-id="9cad4-132">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9cad4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cad4-133">-ResourceId</span></span>
<span data-ttu-id="9cad4-134">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-134">Resource ID.</span></span>

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

### <span data-ttu-id="9cad4-135">-확인</span><span class="sxs-lookup"><span data-stu-id="9cad4-135">-Confirm</span></span>
<span data-ttu-id="9cad4-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cad4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cad4-137">-WhatIf</span></span>
<span data-ttu-id="9cad4-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cad4-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cad4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cad4-140">CommonParameters</span></span>
<span data-ttu-id="9cad4-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cad4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cad4-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9cad4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cad4-143">입력</span><span class="sxs-lookup"><span data-stu-id="9cad4-143">INPUTS</span></span>

### <span data-ttu-id="9cad4-144">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9cad4-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9cad4-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9cad4-145">System.String</span></span>

### <span data-ttu-id="9cad4-146">Microsoft. 네트워크 모델. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="9cad4-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="9cad4-147">출력</span><span class="sxs-lookup"><span data-stu-id="9cad4-147">OUTPUTS</span></span>

### <span data-ttu-id="9cad4-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9cad4-148">System.Boolean</span></span>

## <span data-ttu-id="9cad4-149">상속자</span><span class="sxs-lookup"><span data-stu-id="9cad4-149">NOTES</span></span>

## <span data-ttu-id="9cad4-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cad4-150">RELATED LINKS</span></span>

[<span data-ttu-id="9cad4-151">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9cad4-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9cad4-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9cad4-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9cad4-153">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9cad4-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9cad4-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9cad4-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9cad4-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9cad4-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9cad4-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9cad4-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9cad4-157">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9cad4-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9cad4-158">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9cad4-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9cad4-159">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9cad4-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9cad4-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9cad4-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9cad4-161">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9cad4-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9cad4-162">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9cad4-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9cad4-163">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cad4-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9cad4-164">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9cad4-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9cad4-165">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9cad4-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9cad4-166">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9cad4-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9cad4-167">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9cad4-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9cad4-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9cad4-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9cad4-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9cad4-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9cad4-170">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9cad4-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9cad4-171">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9cad4-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9cad4-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9cad4-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9cad4-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9cad4-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9cad4-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9cad4-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9cad4-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9cad4-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9cad4-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9cad4-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9cad4-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9cad4-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="9cad4-178">새로운 AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9cad4-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="9cad4-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9cad4-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="9cad4-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9cad4-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
