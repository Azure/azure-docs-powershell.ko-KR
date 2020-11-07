---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 44f81008b0693a4ff14a80a818e9d2514dfe0ebf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704166"
---
# <span data-ttu-id="ff7dc-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff7dc-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ff7dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7dc-103">연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff7dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff7dc-104">SYNTAX</span></span>

### <span data-ttu-id="ff7dc-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff7dc-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff7dc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ff7dc-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff7dc-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ff7dc-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7dc-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff7dc-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7dc-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ff7dc-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff7dc-110">설명은</span><span class="sxs-lookup"><span data-stu-id="ff7dc-110">DESCRIPTION</span></span>
<span data-ttu-id="ff7dc-111">Set-AzureRmNetworkWatcherConnectionMonitor cmdlet은 지정 된 연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="ff7dc-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ff7dc-112">EXAMPLES</span></span>

### <span data-ttu-id="ff7dc-113">예제 1: 연결 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="ff7dc-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="ff7dc-114">이 예제에서는 destinationAddress를 변경 하 고 태그를 추가 하 여 기존 연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="ff7dc-115">변수</span><span class="sxs-lookup"><span data-stu-id="ff7dc-115">PARAMETERS</span></span>

### <span data-ttu-id="ff7dc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff7dc-116">-AsJob</span></span>
<span data-ttu-id="ff7dc-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ff7dc-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-118">-확인</span><span class="sxs-lookup"><span data-stu-id="ff7dc-118">-Confirm</span></span>
<span data-ttu-id="ff7dc-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7dc-120">-DefaultProfile</span></span>
<span data-ttu-id="ff7dc-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ff7dc-122">-DestinationAddress</span></span>
<span data-ttu-id="ff7dc-123">연결 모니터 대상의 Ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-123">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ff7dc-124">-DestinationPort</span></span>
<span data-ttu-id="ff7dc-125">대상 포트.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-125">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="ff7dc-126">-DestinationResourceId</span></span>
<span data-ttu-id="ff7dc-127">연결 모니터 대상의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-127">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff7dc-128">-InputObject</span></span>
<span data-ttu-id="ff7dc-129">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="ff7dc-129">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-130">-위치</span><span class="sxs-lookup"><span data-stu-id="ff7dc-130">-Location</span></span>
<span data-ttu-id="ff7dc-131">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ff7dc-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ff7dc-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="ff7dc-133">모니터링 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-133">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-134">-이름</span><span class="sxs-lookup"><span data-stu-id="ff7dc-134">-Name</span></span>
<span data-ttu-id="ff7dc-135">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff7dc-136">-NetworkWatcher</span></span>
<span data-ttu-id="ff7dc-137">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="ff7dc-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ff7dc-138">-NetworkWatcherName</span></span>
<span data-ttu-id="ff7dc-139">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="ff7dc-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff7dc-140">-ResourceGroupName</span></span>
<span data-ttu-id="ff7dc-141">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ff7dc-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff7dc-142">-ResourceId</span></span>
<span data-ttu-id="ff7dc-143">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-143">Resource ID.</span></span>

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

### <span data-ttu-id="ff7dc-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="ff7dc-144">-SourcePort</span></span>
<span data-ttu-id="ff7dc-145">원본 포트.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-145">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ff7dc-146">-SourceResourceId</span></span>
<span data-ttu-id="ff7dc-147">연결 모니터 원본의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-147">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-148">태그</span><span class="sxs-lookup"><span data-stu-id="ff7dc-148">-Tag</span></span>
<span data-ttu-id="ff7dc-149">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff7dc-150">-WhatIf</span></span>
<span data-ttu-id="ff7dc-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff7dc-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7dc-153">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="ff7dc-153">-ConfigureOnly</span></span>
<span data-ttu-id="ff7dc-154">연결 모니터를 구성 하지만 시작 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-154">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="ff7dc-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7dc-155">CommonParameters</span></span>
<span data-ttu-id="ff7dc-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ff7dc-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff7dc-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7dc-158">입력</span><span class="sxs-lookup"><span data-stu-id="ff7dc-158">INPUTS</span></span>

### <span data-ttu-id="ff7dc-159">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff7dc-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ff7dc-160">Microsoft. Azure. PSConnectionMonitorResult.</span><span class="sxs-lookup"><span data-stu-id="ff7dc-160">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ff7dc-161">출력</span><span class="sxs-lookup"><span data-stu-id="ff7dc-161">OUTPUTS</span></span>

### <span data-ttu-id="ff7dc-162">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ff7dc-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ff7dc-163">상속자</span><span class="sxs-lookup"><span data-stu-id="ff7dc-163">NOTES</span></span>
<span data-ttu-id="ff7dc-164">키워드: azure, azurerm, arm, 리소스, 연결, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 모니터</span><span class="sxs-lookup"><span data-stu-id="ff7dc-164">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="ff7dc-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff7dc-165">RELATED LINKS</span></span>

[<span data-ttu-id="ff7dc-166">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff7dc-166">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ff7dc-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff7dc-167">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ff7dc-168">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ff7dc-168">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ff7dc-169">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ff7dc-169">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="ff7dc-170">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ff7dc-170">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="ff7dc-171">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ff7dc-171">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="ff7dc-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ff7dc-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="ff7dc-173">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ff7dc-173">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ff7dc-174">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ff7dc-174">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="ff7dc-175">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ff7dc-175">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ff7dc-176">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ff7dc-176">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ff7dc-177">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ff7dc-177">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ff7dc-178">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff7dc-178">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ff7dc-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ff7dc-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="ff7dc-180">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff7dc-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ff7dc-181">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff7dc-181">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ff7dc-182">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff7dc-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ff7dc-183">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ff7dc-183">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
