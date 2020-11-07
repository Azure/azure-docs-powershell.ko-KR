---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872190"
---
# <span data-ttu-id="b2510-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2510-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b2510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2510-102">SYNOPSIS</span></span>
<span data-ttu-id="b2510-103">연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-103">Update a connection monitor.</span></span>

## <span data-ttu-id="b2510-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2510-104">SYNTAX</span></span>

### <span data-ttu-id="b2510-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2510-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2510-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b2510-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2510-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b2510-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2510-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2510-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2510-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b2510-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2510-110">설명은</span><span class="sxs-lookup"><span data-stu-id="b2510-110">DESCRIPTION</span></span>
<span data-ttu-id="b2510-111">Set-AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="b2510-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b2510-112">EXAMPLES</span></span>

### <span data-ttu-id="b2510-113">예제 1: 연결 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="b2510-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="b2510-114">이 예제에서는 destinationAddress를 변경 하 고 태그를 추가 하 여 기존 연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="b2510-115">변수</span><span class="sxs-lookup"><span data-stu-id="b2510-115">PARAMETERS</span></span>

### <span data-ttu-id="b2510-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2510-116">-AsJob</span></span>
<span data-ttu-id="b2510-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b2510-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2510-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="b2510-118">-ConfigureOnly</span></span>
<span data-ttu-id="b2510-119">연결 모니터를 구성 하지만 시작 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="b2510-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2510-120">-DefaultProfile</span></span>
<span data-ttu-id="b2510-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2510-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b2510-122">-DestinationAddress</span></span>
<span data-ttu-id="b2510-123">연결 모니터 대상의 Ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b2510-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b2510-124">-DestinationPort</span></span>
<span data-ttu-id="b2510-125">대상 포트.</span><span class="sxs-lookup"><span data-stu-id="b2510-125">Destination port.</span></span>

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

### <span data-ttu-id="b2510-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="b2510-126">-DestinationResourceId</span></span>
<span data-ttu-id="b2510-127">연결 모니터 대상의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b2510-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2510-128">-InputObject</span></span>
<span data-ttu-id="b2510-129">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="b2510-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="b2510-130">-위치</span><span class="sxs-lookup"><span data-stu-id="b2510-130">-Location</span></span>
<span data-ttu-id="b2510-131">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b2510-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b2510-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="b2510-133">모니터링 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="b2510-134">-이름</span><span class="sxs-lookup"><span data-stu-id="b2510-134">-Name</span></span>
<span data-ttu-id="b2510-135">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="b2510-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2510-136">-NetworkWatcher</span></span>
<span data-ttu-id="b2510-137">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="b2510-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="b2510-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b2510-138">-NetworkWatcherName</span></span>
<span data-ttu-id="b2510-139">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="b2510-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2510-140">-ResourceGroupName</span></span>
<span data-ttu-id="b2510-141">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b2510-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2510-142">-ResourceId</span></span>
<span data-ttu-id="b2510-143">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-143">Resource ID.</span></span>

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

### <span data-ttu-id="b2510-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b2510-144">-SourcePort</span></span>
<span data-ttu-id="b2510-145">원본 포트.</span><span class="sxs-lookup"><span data-stu-id="b2510-145">Source port.</span></span>

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

### <span data-ttu-id="b2510-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b2510-146">-SourceResourceId</span></span>
<span data-ttu-id="b2510-147">연결 모니터 원본의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="b2510-148">태그</span><span class="sxs-lookup"><span data-stu-id="b2510-148">-Tag</span></span>
<span data-ttu-id="b2510-149">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b2510-150">-확인</span><span class="sxs-lookup"><span data-stu-id="b2510-150">-Confirm</span></span>
<span data-ttu-id="b2510-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2510-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2510-152">-WhatIf</span></span>
<span data-ttu-id="b2510-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2510-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2510-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2510-155">CommonParameters</span></span>
<span data-ttu-id="b2510-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2510-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2510-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2510-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2510-158">입력</span><span class="sxs-lookup"><span data-stu-id="b2510-158">INPUTS</span></span>

### <span data-ttu-id="b2510-159">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2510-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b2510-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b2510-160">System.String</span></span>

### <span data-ttu-id="b2510-161">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="b2510-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="b2510-162">출력</span><span class="sxs-lookup"><span data-stu-id="b2510-162">OUTPUTS</span></span>

### <span data-ttu-id="b2510-163">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="b2510-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="b2510-164">상속자</span><span class="sxs-lookup"><span data-stu-id="b2510-164">NOTES</span></span>
<span data-ttu-id="b2510-165">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="b2510-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="b2510-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2510-166">RELATED LINKS</span></span>

[<span data-ttu-id="b2510-167">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2510-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b2510-168">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2510-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b2510-169">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b2510-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b2510-170">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b2510-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b2510-171">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b2510-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b2510-172">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b2510-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b2510-173">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b2510-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b2510-174">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2510-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2510-175">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b2510-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b2510-176">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2510-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2510-177">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2510-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2510-178">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2510-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2510-179">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2510-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2510-180">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b2510-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b2510-181">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2510-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2510-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2510-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2510-183">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2510-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2510-184">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2510-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2510-185">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2510-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b2510-186">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b2510-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b2510-187">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b2510-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b2510-188">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b2510-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b2510-189">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b2510-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b2510-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b2510-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b2510-191">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b2510-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b2510-192">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b2510-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b2510-193">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b2510-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
