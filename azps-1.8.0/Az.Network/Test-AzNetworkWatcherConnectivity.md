---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 6b689a96a4f737b2f92b4146f71faff7a09d8d36
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402714"
---
# <span data-ttu-id="b4ea9-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b4ea9-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="b4ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ea9-103">지정된 원본 VM 및 대상에 대한 연결 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="b4ea9-104">구문</span><span class="sxs-lookup"><span data-stu-id="b4ea9-104">SYNTAX</span></span>

### <span data-ttu-id="b4ea9-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="b4ea9-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4ea9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b4ea9-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4ea9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b4ea9-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4ea9-108">설명</span><span class="sxs-lookup"><span data-stu-id="b4ea9-108">DESCRIPTION</span></span>
<span data-ttu-id="b4ea9-109">Test-AzNetworkWatcherConnectivity cmdlet은 지정된 원본 VM 및 대상에 대한 연결 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="b4ea9-110">원본과 대상 간의 연결을 설정하지 못하면 cmdlet에서 문제의 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="b4ea9-111">예제</span><span class="sxs-lookup"><span data-stu-id="b4ea9-111">EXAMPLES</span></span>

### <span data-ttu-id="b4ea9-112">예제 1: VM에서 웹 사이트로 Network Watcher 연결 테스트</span><span class="sxs-lookup"><span data-stu-id="b4ea9-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="b4ea9-113">이 예제에서는 Azure의 VM에서 VM으로의 연결을 www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="b4ea9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4ea9-114">PARAMETERS</span></span>

### <span data-ttu-id="b4ea9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4ea9-115">-AsJob</span></span>
<span data-ttu-id="b4ea9-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b4ea9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4ea9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ea9-117">-DefaultProfile</span></span>
<span data-ttu-id="b4ea9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4ea9-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b4ea9-119">-DestinationAddress</span></span>
<span data-ttu-id="b4ea9-120">연결 시도를 할 리소스의 IP 주소 또는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea9-121">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="b4ea9-121">-DestinationId</span></span>
<span data-ttu-id="b4ea9-122">연결 시도를 할 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-122">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea9-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b4ea9-123">-DestinationPort</span></span>
<span data-ttu-id="b4ea9-124">연결이 확인될 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-124">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea9-125">-Location</span><span class="sxs-lookup"><span data-stu-id="b4ea9-125">-Location</span></span>
<span data-ttu-id="b4ea9-126">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b4ea9-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4ea9-127">-NetworkWatcher</span></span>
<span data-ttu-id="b4ea9-128">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="b4ea9-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b4ea9-129">-NetworkWatcherName</span></span>
<span data-ttu-id="b4ea9-130">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea9-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4ea9-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="b4ea9-132">연결이 수행될 프로토칼 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-132">Protocal configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ea9-133">-ResourceGroupName</span></span>
<span data-ttu-id="b4ea9-134">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b4ea9-135">-SourceId</span><span class="sxs-lookup"><span data-stu-id="b4ea9-135">-SourceId</span></span>
<span data-ttu-id="b4ea9-136">연결 검사를 시작할 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="b4ea9-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b4ea9-137">-SourcePort</span></span>
<span data-ttu-id="b4ea9-138">연결 검사를 수행할 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-138">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4ea9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ea9-139">CommonParameters</span></span>
<span data-ttu-id="b4ea9-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ea9-141">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b4ea9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ea9-142">입력</span><span class="sxs-lookup"><span data-stu-id="b4ea9-142">INPUTS</span></span>

### <span data-ttu-id="b4ea9-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b4ea9-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b4ea9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b4ea9-144">System.String</span></span>

### <span data-ttu-id="b4ea9-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b4ea9-145">System.Int32</span></span>

## <span data-ttu-id="b4ea9-146">출력</span><span class="sxs-lookup"><span data-stu-id="b4ea9-146">OUTPUTS</span></span>

### <span data-ttu-id="b4ea9-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="b4ea9-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="b4ea9-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b4ea9-148">NOTES</span></span>
<span data-ttu-id="b4ea9-149">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자</span><span class="sxs-lookup"><span data-stu-id="b4ea9-149">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b4ea9-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4ea9-150">RELATED LINKS</span></span>

<span data-ttu-id="b4ea9-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="b4ea9-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="b4ea9-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="b4ea9-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="b4ea9-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="b4ea9-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="b4ea9-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="b4ea9-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span></span>
