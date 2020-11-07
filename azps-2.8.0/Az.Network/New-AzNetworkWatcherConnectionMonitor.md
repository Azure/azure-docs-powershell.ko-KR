---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ec7f6f910a50f479a923451fb9b893a5cabb5301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869877"
---
# <span data-ttu-id="b14bb-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b14bb-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b14bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b14bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b14bb-103">연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="b14bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b14bb-104">SYNTAX</span></span>

### <span data-ttu-id="b14bb-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b14bb-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b14bb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b14bb-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b14bb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b14bb-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b14bb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b14bb-108">DESCRIPTION</span></span>
<span data-ttu-id="b14bb-109">New-AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 원본 및 대상에 대 한 연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-109">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="b14bb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b14bb-110">EXAMPLES</span></span>

### <span data-ttu-id="b14bb-111">예제 1: vm 및 인터넷 대상에 대 한 연결 모니터 만들기</span><span class="sxs-lookup"><span data-stu-id="b14bb-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="b14bb-112">New-AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 원본 및 대상에 대 한 연결 모니터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="b14bb-113">변수</span><span class="sxs-lookup"><span data-stu-id="b14bb-113">PARAMETERS</span></span>

### <span data-ttu-id="b14bb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b14bb-114">-AsJob</span></span>
<span data-ttu-id="b14bb-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b14bb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b14bb-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="b14bb-116">-ConfigureOnly</span></span>
<span data-ttu-id="b14bb-117">연결 모니터를 구성 하지만 시작 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="b14bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14bb-118">-DefaultProfile</span></span>
<span data-ttu-id="b14bb-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b14bb-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b14bb-120">-DestinationAddress</span></span>
<span data-ttu-id="b14bb-121">연결 모니터 대상의 Ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b14bb-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b14bb-122">-DestinationPort</span></span>
<span data-ttu-id="b14bb-123">대상 포트.</span><span class="sxs-lookup"><span data-stu-id="b14bb-123">Destination port.</span></span>

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

### <span data-ttu-id="b14bb-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="b14bb-124">-DestinationResourceId</span></span>
<span data-ttu-id="b14bb-125">연결 모니터 대상의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b14bb-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b14bb-126">-Force</span></span>
<span data-ttu-id="b14bb-127">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="b14bb-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b14bb-128">-위치</span><span class="sxs-lookup"><span data-stu-id="b14bb-128">-Location</span></span>
<span data-ttu-id="b14bb-129">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b14bb-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b14bb-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="b14bb-131">모니터링 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14bb-132">-이름</span><span class="sxs-lookup"><span data-stu-id="b14bb-132">-Name</span></span>
<span data-ttu-id="b14bb-133">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14bb-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b14bb-134">-NetworkWatcher</span></span>
<span data-ttu-id="b14bb-135">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="b14bb-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="b14bb-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b14bb-136">-NetworkWatcherName</span></span>
<span data-ttu-id="b14bb-137">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="b14bb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b14bb-138">-ResourceGroupName</span></span>
<span data-ttu-id="b14bb-139">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b14bb-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b14bb-140">-SourcePort</span></span>
<span data-ttu-id="b14bb-141">원본 포트.</span><span class="sxs-lookup"><span data-stu-id="b14bb-141">Source port.</span></span>

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

### <span data-ttu-id="b14bb-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b14bb-142">-SourceResourceId</span></span>
<span data-ttu-id="b14bb-143">연결 모니터 원본의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-143">The ID of the connection monitor source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14bb-144">태그</span><span class="sxs-lookup"><span data-stu-id="b14bb-144">-Tag</span></span>
<span data-ttu-id="b14bb-145">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b14bb-146">-확인</span><span class="sxs-lookup"><span data-stu-id="b14bb-146">-Confirm</span></span>
<span data-ttu-id="b14bb-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b14bb-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b14bb-148">-WhatIf</span></span>
<span data-ttu-id="b14bb-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b14bb-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b14bb-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14bb-151">CommonParameters</span></span>
<span data-ttu-id="b14bb-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14bb-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14bb-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b14bb-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14bb-154">입력</span><span class="sxs-lookup"><span data-stu-id="b14bb-154">INPUTS</span></span>

### <span data-ttu-id="b14bb-155">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b14bb-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="b14bb-156">출력</span><span class="sxs-lookup"><span data-stu-id="b14bb-156">OUTPUTS</span></span>

### <span data-ttu-id="b14bb-157">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="b14bb-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="b14bb-158">상속자</span><span class="sxs-lookup"><span data-stu-id="b14bb-158">NOTES</span></span>
<span data-ttu-id="b14bb-159">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="b14bb-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="b14bb-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b14bb-160">RELATED LINKS</span></span>

[<span data-ttu-id="b14bb-161">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b14bb-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b14bb-162">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b14bb-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b14bb-163">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b14bb-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b14bb-164">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b14bb-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b14bb-165">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b14bb-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b14bb-166">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b14bb-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b14bb-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b14bb-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b14bb-168">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b14bb-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b14bb-169">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b14bb-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b14bb-170">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b14bb-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b14bb-171">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b14bb-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b14bb-172">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b14bb-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b14bb-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b14bb-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b14bb-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b14bb-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b14bb-175">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b14bb-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b14bb-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b14bb-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b14bb-177">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b14bb-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b14bb-178">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b14bb-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b14bb-179">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b14bb-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b14bb-180">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b14bb-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b14bb-181">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b14bb-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b14bb-182">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b14bb-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b14bb-183">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b14bb-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b14bb-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b14bb-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b14bb-185">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b14bb-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b14bb-186">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b14bb-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b14bb-187">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b14bb-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
