---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344181"
---
# <span data-ttu-id="ed139-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ed139-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ed139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed139-102">SYNOPSIS</span></span>
<span data-ttu-id="ed139-103">연결 모니터 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="ed139-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed139-104">SYNTAX</span></span>

### <span data-ttu-id="ed139-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ed139-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed139-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ed139-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed139-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="ed139-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed139-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="ed139-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed139-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ed139-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed139-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="ed139-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed139-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed139-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed139-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="ed139-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed139-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ed139-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed139-114">설명</span><span class="sxs-lookup"><span data-stu-id="ed139-114">DESCRIPTION</span></span>
<span data-ttu-id="ed139-115">이 Set-AzNetworkWatcherConnectionMonitor cmdlet은 연결 모니터 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="ed139-116">예제</span><span class="sxs-lookup"><span data-stu-id="ed139-116">EXAMPLES</span></span>

### <span data-ttu-id="ed139-117">예제 1: 연결 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="ed139-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="ed139-118">이 예제에서는 destinationAddress를 변경하고 태그를 추가하여 기존 연결 모니터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="ed139-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed139-119">PARAMETERS</span></span>

### <span data-ttu-id="ed139-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed139-120">-AsJob</span></span>
<span data-ttu-id="ed139-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ed139-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed139-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="ed139-122">-ConfigureOnly</span></span>
<span data-ttu-id="ed139-123">연결 모니터를 구성하지만 시작하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="ed139-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed139-124">-DefaultProfile</span></span>
<span data-ttu-id="ed139-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed139-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ed139-126">-DestinationAddress</span></span>
<span data-ttu-id="ed139-127">연결 모니터 대상(IP 또는 도메인 이름)의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="ed139-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ed139-128">-DestinationPort</span></span>
<span data-ttu-id="ed139-129">연결 모니터에서 사용하는 대상 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="ed139-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="ed139-130">-DestinationResourceId</span></span>
<span data-ttu-id="ed139-131">연결 모니터에서 대상으로 사용되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="ed139-132">-Force</span><span class="sxs-lookup"><span data-stu-id="ed139-132">-Force</span></span>
<span data-ttu-id="ed139-133">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ed139-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed139-134">-InputObject</span></span>
<span data-ttu-id="ed139-135">연결 모니터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="ed139-136">-Location</span><span class="sxs-lookup"><span data-stu-id="ed139-136">-Location</span></span>
<span data-ttu-id="ed139-137">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ed139-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ed139-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="ed139-139">모니터링 간격(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="ed139-140">기본값은 60초입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="ed139-141">-Name</span><span class="sxs-lookup"><span data-stu-id="ed139-141">-Name</span></span>
<span data-ttu-id="ed139-142">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="ed139-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed139-143">-NetworkWatcher</span></span>
<span data-ttu-id="ed139-144">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="ed139-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ed139-145">-NetworkWatcherName</span></span>
<span data-ttu-id="ed139-146">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="ed139-147">-Note</span><span class="sxs-lookup"><span data-stu-id="ed139-147">-Note</span></span>
<span data-ttu-id="ed139-148">연결 모니터와 연결된 메모입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="ed139-149">-Output</span><span class="sxs-lookup"><span data-stu-id="ed139-149">-Output</span></span>
<span data-ttu-id="ed139-150">연결 모니터 출력 대상을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="ed139-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed139-151">-ResourceGroupName</span></span>
<span data-ttu-id="ed139-152">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ed139-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed139-153">-ResourceId</span></span>
<span data-ttu-id="ed139-154">ConnectionMonitor 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="ed139-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="ed139-155">-SourcePort</span></span>
<span data-ttu-id="ed139-156">연결 모니터에서 사용되는 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="ed139-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ed139-157">-SourceResourceId</span></span>
<span data-ttu-id="ed139-158">연결 모니터에서 원본으로 사용되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="ed139-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed139-159">-Tag</span></span>
<span data-ttu-id="ed139-160">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ed139-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="ed139-161">-TestGroup</span></span>
<span data-ttu-id="ed139-162">테스트 그룹 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-162">The list of test groups.</span></span>

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

### <span data-ttu-id="ed139-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed139-163">-Confirm</span></span>
<span data-ttu-id="ed139-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed139-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed139-165">-WhatIf</span></span>
<span data-ttu-id="ed139-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ed139-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed139-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed139-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed139-168">CommonParameters</span></span>
<span data-ttu-id="ed139-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed139-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed139-170">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ed139-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed139-171">입력</span><span class="sxs-lookup"><span data-stu-id="ed139-171">INPUTS</span></span>

### <span data-ttu-id="ed139-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ed139-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ed139-173">System.String</span><span class="sxs-lookup"><span data-stu-id="ed139-173">System.String</span></span>

### <span data-ttu-id="ed139-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ed139-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ed139-175">출력</span><span class="sxs-lookup"><span data-stu-id="ed139-175">OUTPUTS</span></span>

### <span data-ttu-id="ed139-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="ed139-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="ed139-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="ed139-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="ed139-178">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed139-178">NOTES</span></span>

## <span data-ttu-id="ed139-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed139-179">RELATED LINKS</span></span>