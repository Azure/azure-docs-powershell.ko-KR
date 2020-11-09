---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309221"
---
# <span data-ttu-id="289dd-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="289dd-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="289dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="289dd-102">SYNOPSIS</span></span>
<span data-ttu-id="289dd-103">연결 모니터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="289dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="289dd-104">SYNTAX</span></span>

### <span data-ttu-id="289dd-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="289dd-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="289dd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="289dd-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="289dd-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="289dd-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="289dd-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="289dd-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="289dd-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="289dd-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="289dd-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="289dd-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="289dd-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="289dd-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="289dd-112">설명은</span><span class="sxs-lookup"><span data-stu-id="289dd-112">DESCRIPTION</span></span>
<span data-ttu-id="289dd-113">New-AzNetworkWatcherConnectionMonitor cmdlet은 지정 된 원본 및 대상 (SingleSourcedestination connection monitor) 또는 테스트 그룹 집합 (MultiEndpointConnectionMonitor)에 대 한 연결 모니터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="289dd-114">예제의</span><span class="sxs-lookup"><span data-stu-id="289dd-114">EXAMPLES</span></span>

### <span data-ttu-id="289dd-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="289dd-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="289dd-116">Name: cm Id:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/공급자/NetworkWatcher_centraluseuap Microsoft/connectionMonitors/t1 Etag: W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState: 성공 원본: {"ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000/providers/resourceGroups/RgCentralUSEUAP/공급자/Microsoft. 컴퓨트/virtualMachines/vm "," Port ": 0} 대상: {" 주소 ":" bing.com "," Port ": 80} MonitoringIntervalInSeconds: 60 자동 시작: 실제 시작: 1/12/2018 7:13:11 PM MonitoringStatus: 실행 위치: centraluseuap/connectionMonitors 태그: {}</span><span class="sxs-lookup"><span data-stu-id="289dd-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="289dd-117">변수</span><span class="sxs-lookup"><span data-stu-id="289dd-117">PARAMETERS</span></span>

### <span data-ttu-id="289dd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="289dd-118">-AsJob</span></span>
<span data-ttu-id="289dd-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="289dd-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="289dd-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="289dd-120">-ConfigureOnly</span></span>
<span data-ttu-id="289dd-121">연결 모니터를 구성 하지만 시작 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-121">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="289dd-122">-ConnectionMonitor</span></span>
<span data-ttu-id="289dd-123">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="289dd-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289dd-124">-DefaultProfile</span></span>
<span data-ttu-id="289dd-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="289dd-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="289dd-126">-DestinationAddress</span></span>
<span data-ttu-id="289dd-127">연결 모니터 대상 (IP 또는 도메인 이름)의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="289dd-128">-DestinationPort</span></span>
<span data-ttu-id="289dd-129">연결 모니터에 사용 되는 대상 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="289dd-130">-DestinationResourceId</span></span>
<span data-ttu-id="289dd-131">연결 모니터에서 대상으로 사용 되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-132">-Force</span><span class="sxs-lookup"><span data-stu-id="289dd-132">-Force</span></span>
<span data-ttu-id="289dd-133">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="289dd-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="289dd-134">-위치</span><span class="sxs-lookup"><span data-stu-id="289dd-134">-Location</span></span>
<span data-ttu-id="289dd-135">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-135">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="289dd-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="289dd-137">모니터링 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="289dd-138">기본값은 60 초입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-138">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-139">-이름</span><span class="sxs-lookup"><span data-stu-id="289dd-139">-Name</span></span>
<span data-ttu-id="289dd-140">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-140">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="289dd-141">-NetworkWatcher</span></span>
<span data-ttu-id="289dd-142">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="289dd-142">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="289dd-143">-NetworkWatcherName</span></span>
<span data-ttu-id="289dd-144">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-144">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-145">-메모</span><span class="sxs-lookup"><span data-stu-id="289dd-145">-Note</span></span>
<span data-ttu-id="289dd-146">연결 모니터와 연결 된 노트입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-146">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-147">-출력</span><span class="sxs-lookup"><span data-stu-id="289dd-147">-Output</span></span>
<span data-ttu-id="289dd-148">연결 모니터 출력 대상에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-148">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="289dd-149">-ResourceGroupName</span></span>
<span data-ttu-id="289dd-150">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-150">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="289dd-151">-SourcePort</span></span>
<span data-ttu-id="289dd-152">연결 모니터에 사용 되는 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-152">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="289dd-153">-SourceResourceId</span></span>
<span data-ttu-id="289dd-154">연결 모니터에서 원본으로 사용 하는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-154">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-155">태그</span><span class="sxs-lookup"><span data-stu-id="289dd-155">-Tag</span></span>
<span data-ttu-id="289dd-156">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-156">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="289dd-157">-TestGroup</span></span>
<span data-ttu-id="289dd-158">테스트 그룹의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-158">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-159">-확인</span><span class="sxs-lookup"><span data-stu-id="289dd-159">-Confirm</span></span>
<span data-ttu-id="289dd-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="289dd-161">-WhatIf</span></span>
<span data-ttu-id="289dd-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="289dd-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289dd-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289dd-164">CommonParameters</span></span>
<span data-ttu-id="289dd-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="289dd-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289dd-166">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="289dd-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289dd-167">입력</span><span class="sxs-lookup"><span data-stu-id="289dd-167">INPUTS</span></span>

### <span data-ttu-id="289dd-168">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="289dd-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="289dd-169">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="289dd-169">System.String</span></span>

### <span data-ttu-id="289dd-170">System.webserver. List ' 1 [[PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft. e. e l t. i = 2.2.2.0, Culture = 중립, PublicKeyToken = null]] 목록</span><span class="sxs-lookup"><span data-stu-id="289dd-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="289dd-171">System.webserver. List ' 1 [[PSNetworkWatcherConnectionMonitorOutputObject, Microsoft. e. e l t. i = 2.2.2.0, Culture = 중립, PublicKeyToken = null]] 목록</span><span class="sxs-lookup"><span data-stu-id="289dd-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="289dd-172">출력</span><span class="sxs-lookup"><span data-stu-id="289dd-172">OUTPUTS</span></span>

### <span data-ttu-id="289dd-173">PSConnectionMonitorResultV1에 대 한.</span><span class="sxs-lookup"><span data-stu-id="289dd-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="289dd-174">PSConnectionMonitorResultV2에 대 한.</span><span class="sxs-lookup"><span data-stu-id="289dd-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="289dd-175">상속자</span><span class="sxs-lookup"><span data-stu-id="289dd-175">NOTES</span></span>

## <span data-ttu-id="289dd-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="289dd-176">RELATED LINKS</span></span>
