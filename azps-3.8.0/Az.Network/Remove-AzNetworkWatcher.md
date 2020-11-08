---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 7723d717a35f4c5e3e693bc5ff115b484df5fa2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044064"
---
# <span data-ttu-id="b4ddd-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4ddd-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="b4ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ddd-103">네트워크 감시자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="b4ddd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4ddd-104">SYNTAX</span></span>

### <span data-ttu-id="b4ddd-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b4ddd-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ddd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b4ddd-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4ddd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b4ddd-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4ddd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b4ddd-108">DESCRIPTION</span></span>
<span data-ttu-id="b4ddd-109">Remove-AzNetworkWatcher cmdlet은 네트워크 감시자 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="b4ddd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b4ddd-110">EXAMPLES</span></span>

### <span data-ttu-id="b4ddd-111">예제 1: 네트워크 감시자 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="b4ddd-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="b4ddd-112">이 예제에서는 리소스 그룹에 네트워크 감시자를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="b4ddd-113">구독 당 지역 당 하나의 네트워크 감시자만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="b4ddd-114">가상 네트워크를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="b4ddd-115">변수</span><span class="sxs-lookup"><span data-stu-id="b4ddd-115">PARAMETERS</span></span>

### <span data-ttu-id="b4ddd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4ddd-116">-AsJob</span></span>
<span data-ttu-id="b4ddd-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b4ddd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4ddd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ddd-118">-DefaultProfile</span></span>
<span data-ttu-id="b4ddd-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4ddd-120">-위치</span><span class="sxs-lookup"><span data-stu-id="b4ddd-120">-Location</span></span>
<span data-ttu-id="b4ddd-121">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b4ddd-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b4ddd-122">-Name</span></span>
<span data-ttu-id="b4ddd-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ddd-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4ddd-124">-NetworkWatcher</span></span>
<span data-ttu-id="b4ddd-125">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="b4ddd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4ddd-126">-PassThru</span></span>
<span data-ttu-id="b4ddd-127">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="b4ddd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ddd-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4ddd-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-129">The resource group name.</span></span>

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

### <span data-ttu-id="b4ddd-130">-확인</span><span class="sxs-lookup"><span data-stu-id="b4ddd-130">-Confirm</span></span>
<span data-ttu-id="b4ddd-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4ddd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4ddd-132">-WhatIf</span></span>
<span data-ttu-id="b4ddd-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ddd-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4ddd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ddd-135">CommonParameters</span></span>
<span data-ttu-id="b4ddd-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ddd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ddd-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ddd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ddd-138">입력</span><span class="sxs-lookup"><span data-stu-id="b4ddd-138">INPUTS</span></span>

### <span data-ttu-id="b4ddd-139">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4ddd-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b4ddd-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4ddd-140">System.String</span></span>

## <span data-ttu-id="b4ddd-141">출력</span><span class="sxs-lookup"><span data-stu-id="b4ddd-141">OUTPUTS</span></span>

### <span data-ttu-id="b4ddd-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b4ddd-142">System.Boolean</span></span>

## <span data-ttu-id="b4ddd-143">상속자</span><span class="sxs-lookup"><span data-stu-id="b4ddd-143">NOTES</span></span>
<span data-ttu-id="b4ddd-144">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="b4ddd-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b4ddd-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4ddd-145">RELATED LINKS</span></span>

[<span data-ttu-id="b4ddd-146">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4ddd-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b4ddd-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4ddd-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b4ddd-148">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4ddd-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b4ddd-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b4ddd-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b4ddd-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b4ddd-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b4ddd-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b4ddd-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b4ddd-152">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b4ddd-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b4ddd-153">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4ddd-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4ddd-154">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b4ddd-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b4ddd-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4ddd-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4ddd-156">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4ddd-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4ddd-157">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b4ddd-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b4ddd-158">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4ddd-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b4ddd-159">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b4ddd-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b4ddd-160">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b4ddd-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b4ddd-161">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4ddd-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4ddd-162">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4ddd-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4ddd-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4ddd-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4ddd-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b4ddd-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b4ddd-165">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4ddd-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4ddd-166">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4ddd-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b4ddd-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b4ddd-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b4ddd-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b4ddd-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b4ddd-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b4ddd-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b4ddd-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b4ddd-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b4ddd-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b4ddd-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b4ddd-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b4ddd-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
