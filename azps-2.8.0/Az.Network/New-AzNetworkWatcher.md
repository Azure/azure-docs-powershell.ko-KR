---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 30b8fda9c29608759360e396f5dcecde3c9b95d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871381"
---
# <span data-ttu-id="30136-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="30136-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="30136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30136-102">SYNOPSIS</span></span>
<span data-ttu-id="30136-103">새 네트워크 감시자 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30136-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="30136-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30136-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30136-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30136-105">DESCRIPTION</span></span>
<span data-ttu-id="30136-106">New-AzNetworkWatcher cmdlet은 새 네트워크 감시자 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30136-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="30136-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30136-107">EXAMPLES</span></span>

### <span data-ttu-id="30136-108">예제 1: 네트워크 감시자 만들기</span><span class="sxs-lookup"><span data-stu-id="30136-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="30136-109">이 예제에서는 새로 만든 리소스 그룹 내에 새 네트워크 감시자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30136-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="30136-110">구독 당 지역 당 하나의 네트워크 감시자만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30136-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="30136-111">변수</span><span class="sxs-lookup"><span data-stu-id="30136-111">PARAMETERS</span></span>

### <span data-ttu-id="30136-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30136-112">-DefaultProfile</span></span>
<span data-ttu-id="30136-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30136-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30136-114">-위치</span><span class="sxs-lookup"><span data-stu-id="30136-114">-Location</span></span>
<span data-ttu-id="30136-115">Location.</span><span class="sxs-lookup"><span data-stu-id="30136-115">Location.</span></span>

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

### <span data-ttu-id="30136-116">-이름</span><span class="sxs-lookup"><span data-stu-id="30136-116">-Name</span></span>
<span data-ttu-id="30136-117">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30136-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30136-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30136-118">-ResourceGroupName</span></span>
<span data-ttu-id="30136-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30136-119">The resource group name.</span></span>

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

### <span data-ttu-id="30136-120">태그</span><span class="sxs-lookup"><span data-stu-id="30136-120">-Tag</span></span>
<span data-ttu-id="30136-121">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="30136-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30136-122">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="30136-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30136-123">-확인</span><span class="sxs-lookup"><span data-stu-id="30136-123">-Confirm</span></span>
<span data-ttu-id="30136-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30136-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30136-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30136-125">-WhatIf</span></span>
<span data-ttu-id="30136-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30136-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30136-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30136-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30136-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30136-128">CommonParameters</span></span>
<span data-ttu-id="30136-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30136-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30136-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30136-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30136-131">입력</span><span class="sxs-lookup"><span data-stu-id="30136-131">INPUTS</span></span>

### <span data-ttu-id="30136-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="30136-132">System.String</span></span>

### <span data-ttu-id="30136-133">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="30136-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="30136-134">출력</span><span class="sxs-lookup"><span data-stu-id="30136-134">OUTPUTS</span></span>

### <span data-ttu-id="30136-135">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="30136-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="30136-136">상속자</span><span class="sxs-lookup"><span data-stu-id="30136-136">NOTES</span></span>
<span data-ttu-id="30136-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="30136-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="30136-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30136-138">RELATED LINKS</span></span>

[<span data-ttu-id="30136-139">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="30136-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="30136-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="30136-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="30136-141">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="30136-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="30136-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="30136-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="30136-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="30136-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="30136-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="30136-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="30136-145">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="30136-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="30136-146">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30136-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="30136-147">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="30136-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="30136-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30136-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="30136-149">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30136-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="30136-150">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30136-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="30136-151">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="30136-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="30136-152">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="30136-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="30136-153">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="30136-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="30136-154">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="30136-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="30136-155">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="30136-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="30136-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="30136-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="30136-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="30136-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="30136-158">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="30136-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="30136-159">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="30136-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="30136-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="30136-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="30136-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="30136-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="30136-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="30136-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="30136-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="30136-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="30136-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="30136-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="30136-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="30136-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
