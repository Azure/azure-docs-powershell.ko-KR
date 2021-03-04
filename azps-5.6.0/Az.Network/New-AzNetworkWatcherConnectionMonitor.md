---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 18db8d01bd9c6c54b1fdf3957f25e12848e309ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958539"
---
# <span data-ttu-id="b8125-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8125-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b8125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8125-102">SYNOPSIS</span></span>
<span data-ttu-id="b8125-103">연결 모니터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="b8125-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8125-104">SYNTAX</span></span>

### <span data-ttu-id="b8125-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b8125-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8125-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b8125-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8125-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="b8125-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8125-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="b8125-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8125-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b8125-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8125-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="b8125-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8125-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="b8125-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8125-112">설명</span><span class="sxs-lookup"><span data-stu-id="b8125-112">DESCRIPTION</span></span>
<span data-ttu-id="b8125-113">New-AzNetworkWatcherConnectionMonitor cmdlet은 지정된 원본 및 대상(SingleSourcedestination 연결 모니터) 또는 테스트 그룹 집합(MultiEndpointConnectionMonitor)에 대한 연결 모니터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="b8125-114">예제</span><span class="sxs-lookup"><span data-stu-id="b8125-114">EXAMPLES</span></span>

### <span data-ttu-id="b8125-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8125-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="b8125-116">이름 : cm Id : /subscriptions/0000000-0000-0000-0000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag : W/"e86b28cf-b907-0074475-a8b7-34d310367694" ProvisioningState : 성공한 원본 : { "ResourceId": "/subscriptions/00000-0000-00000-00000-000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft . Compute/virtualMachines/vm", "Port": 0 } 대상 : { "address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 1/12/13:11 PM MonitoringStatus : Running Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : {}</span><span class="sxs-lookup"><span data-stu-id="b8125-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="b8125-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b8125-117">PARAMETERS</span></span>

### <span data-ttu-id="b8125-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8125-118">-AsJob</span></span>
<span data-ttu-id="b8125-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b8125-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8125-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="b8125-120">-ConfigureOnly</span></span>
<span data-ttu-id="b8125-121">연결 모니터를 구성하지만 시작하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="b8125-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8125-122">-ConnectionMonitor</span></span>
<span data-ttu-id="b8125-123">연결 모니터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="b8125-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8125-124">-DefaultProfile</span></span>
<span data-ttu-id="b8125-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8125-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b8125-126">-DestinationAddress</span></span>
<span data-ttu-id="b8125-127">연결 모니터 대상(IP 또는 도메인 이름)의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="b8125-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b8125-128">-DestinationPort</span></span>
<span data-ttu-id="b8125-129">연결 모니터에서 사용하는 대상 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="b8125-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="b8125-130">-DestinationResourceId</span></span>
<span data-ttu-id="b8125-131">연결 모니터에서 대상으로 사용되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="b8125-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b8125-132">-Force</span></span>
<span data-ttu-id="b8125-133">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b8125-134">-Location</span><span class="sxs-lookup"><span data-stu-id="b8125-134">-Location</span></span>
<span data-ttu-id="b8125-135">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b8125-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b8125-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="b8125-137">모니터링 간격(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="b8125-138">기본값은 60초입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="b8125-139">-Name</span><span class="sxs-lookup"><span data-stu-id="b8125-139">-Name</span></span>
<span data-ttu-id="b8125-140">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="b8125-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8125-141">-NetworkWatcher</span></span>
<span data-ttu-id="b8125-142">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="b8125-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b8125-143">-NetworkWatcherName</span></span>
<span data-ttu-id="b8125-144">네트워크 감시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="b8125-145">-Note</span><span class="sxs-lookup"><span data-stu-id="b8125-145">-Note</span></span>
<span data-ttu-id="b8125-146">연결 모니터와 연결된 노트입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="b8125-147">-Output</span><span class="sxs-lookup"><span data-stu-id="b8125-147">-Output</span></span>
<span data-ttu-id="b8125-148">연결 모니터 출력 대상을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="b8125-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8125-149">-ResourceGroupName</span></span>
<span data-ttu-id="b8125-150">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b8125-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b8125-151">-SourcePort</span></span>
<span data-ttu-id="b8125-152">연결 모니터에서 사용되는 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="b8125-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b8125-153">-SourceResourceId</span></span>
<span data-ttu-id="b8125-154">연결 모니터를 사용하여 원본으로 사용되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="b8125-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8125-155">-Tag</span></span>
<span data-ttu-id="b8125-156">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b8125-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="b8125-157">-TestGroup</span></span>
<span data-ttu-id="b8125-158">테스트 그룹 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-158">The list of test groups.</span></span>

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

### <span data-ttu-id="b8125-159">-확인</span><span class="sxs-lookup"><span data-stu-id="b8125-159">-Confirm</span></span>
<span data-ttu-id="b8125-160">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8125-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8125-161">-WhatIf</span></span>
<span data-ttu-id="b8125-162">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8125-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8125-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8125-164">CommonParameters</span></span>
<span data-ttu-id="b8125-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8125-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8125-166">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8125-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8125-167">입력</span><span class="sxs-lookup"><span data-stu-id="b8125-167">INPUTS</span></span>

### <span data-ttu-id="b8125-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8125-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b8125-169">System.String</span><span class="sxs-lookup"><span data-stu-id="b8125-169">System.String</span></span>

### <span data-ttu-id="b8125-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b8125-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b8125-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b8125-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b8125-172">출력</span><span class="sxs-lookup"><span data-stu-id="b8125-172">OUTPUTS</span></span>

### <span data-ttu-id="b8125-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="b8125-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="b8125-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="b8125-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="b8125-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8125-175">NOTES</span></span>

## <span data-ttu-id="b8125-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8125-176">RELATED LINKS</span></span>
