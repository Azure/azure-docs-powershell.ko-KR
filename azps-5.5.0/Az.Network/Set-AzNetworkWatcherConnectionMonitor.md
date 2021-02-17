---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184185"
---
# <span data-ttu-id="600fd-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="600fd-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="600fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600fd-102">SYNOPSIS</span></span>
<span data-ttu-id="600fd-103">연결 모니터 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="600fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="600fd-104">SYNTAX</span></span>

### <span data-ttu-id="600fd-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="600fd-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="600fd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="600fd-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="600fd-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="600fd-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600fd-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="600fd-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600fd-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="600fd-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600fd-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="600fd-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600fd-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="600fd-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600fd-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="600fd-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600fd-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="600fd-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600fd-114">설명</span><span class="sxs-lookup"><span data-stu-id="600fd-114">DESCRIPTION</span></span>
<span data-ttu-id="600fd-115">이 Set-AzNetworkWatcherConnectionMonitor cmdlet은 연결 모니터 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="600fd-116">예제</span><span class="sxs-lookup"><span data-stu-id="600fd-116">EXAMPLES</span></span>

### <span data-ttu-id="600fd-117">예제 1: 연결 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="600fd-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="600fd-118">이 예제에서는 destinationAddress를 변경하고 태그를 추가하여 기존 연결 모니터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="600fd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="600fd-119">PARAMETERS</span></span>

### <span data-ttu-id="600fd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="600fd-120">-AsJob</span></span>
<span data-ttu-id="600fd-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="600fd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="600fd-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="600fd-122">-ConfigureOnly</span></span>
<span data-ttu-id="600fd-123">연결 모니터를 구성하지만 시작하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-123">Configure connection monitor, but do not start it</span></span>

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

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600fd-124">-DefaultProfile</span></span>
<span data-ttu-id="600fd-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="600fd-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="600fd-126">-DestinationAddress</span></span>
<span data-ttu-id="600fd-127">연결 모니터 대상(IP 또는 도메인 이름)의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="600fd-128">-DestinationPort</span></span>
<span data-ttu-id="600fd-129">연결 모니터에서 사용하는 대상 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-129">The destination port used by connection monitor.</span></span>

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

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="600fd-130">-DestinationResourceId</span></span>
<span data-ttu-id="600fd-131">연결 모니터에서 대상으로 사용되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-132">-Force</span><span class="sxs-lookup"><span data-stu-id="600fd-132">-Force</span></span>
<span data-ttu-id="600fd-133">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="600fd-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="600fd-134">-InputObject</span></span>
<span data-ttu-id="600fd-135">연결 모니터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="600fd-136">-Location</span><span class="sxs-lookup"><span data-stu-id="600fd-136">-Location</span></span>
<span data-ttu-id="600fd-137">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="600fd-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="600fd-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="600fd-139">모니터링 간격(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="600fd-140">기본값은 60초입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-140">Default value is 60 seconds.</span></span>

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

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-141">-Name</span><span class="sxs-lookup"><span data-stu-id="600fd-141">-Name</span></span>
<span data-ttu-id="600fd-142">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="600fd-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="600fd-143">-NetworkWatcher</span></span>
<span data-ttu-id="600fd-144">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="600fd-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="600fd-145">-NetworkWatcherName</span></span>
<span data-ttu-id="600fd-146">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="600fd-147">-Note</span><span class="sxs-lookup"><span data-stu-id="600fd-147">-Note</span></span>
<span data-ttu-id="600fd-148">연결 모니터와 연결된 메모입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-148">Notes associated with connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-149">-Output</span><span class="sxs-lookup"><span data-stu-id="600fd-149">-Output</span></span>
<span data-ttu-id="600fd-150">연결 모니터 출력 대상을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-150">Describes a connection monitor output destinations.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600fd-151">-ResourceGroupName</span></span>
<span data-ttu-id="600fd-152">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="600fd-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="600fd-153">-ResourceId</span></span>
<span data-ttu-id="600fd-154">ConnectionMonitor 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="600fd-155">-SourcePort</span></span>
<span data-ttu-id="600fd-156">연결 모니터에서 사용되는 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-156">The source port used by connection monitor.</span></span>

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

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="600fd-157">-SourceResourceId</span></span>
<span data-ttu-id="600fd-158">연결 모니터에서 원본으로 사용되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-158">The ID of the resource used as the source by connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="600fd-159">-Tag</span></span>
<span data-ttu-id="600fd-160">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-160">A hashtable which represents resource tags.</span></span>

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

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="600fd-161">-TestGroup</span></span>
<span data-ttu-id="600fd-162">테스트 그룹 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-162">The list of test groups.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600fd-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="600fd-163">-Confirm</span></span>
<span data-ttu-id="600fd-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600fd-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600fd-165">-WhatIf</span></span>
<span data-ttu-id="600fd-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="600fd-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600fd-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600fd-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600fd-168">CommonParameters</span></span>
<span data-ttu-id="600fd-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="600fd-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600fd-170">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="600fd-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600fd-171">입력</span><span class="sxs-lookup"><span data-stu-id="600fd-171">INPUTS</span></span>

### <span data-ttu-id="600fd-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="600fd-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="600fd-173">System.String</span><span class="sxs-lookup"><span data-stu-id="600fd-173">System.String</span></span>

### <span data-ttu-id="600fd-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="600fd-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="600fd-175">출력</span><span class="sxs-lookup"><span data-stu-id="600fd-175">OUTPUTS</span></span>

### <span data-ttu-id="600fd-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="600fd-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="600fd-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="600fd-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="600fd-178">참고 사항</span><span class="sxs-lookup"><span data-stu-id="600fd-178">NOTES</span></span>

## <span data-ttu-id="600fd-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="600fd-179">RELATED LINKS</span></span>
