---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043098"
---
# <span data-ttu-id="7c679-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7c679-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="7c679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c679-102">SYNOPSIS</span></span>
<span data-ttu-id="7c679-103">연결 모니터 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="7c679-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c679-104">SYNTAX</span></span>

### <span data-ttu-id="7c679-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c679-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c679-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7c679-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c679-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="7c679-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c679-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="7c679-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c679-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7c679-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c679-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="7c679-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c679-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c679-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c679-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="7c679-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c679-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c679-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c679-114">설명은</span><span class="sxs-lookup"><span data-stu-id="7c679-114">DESCRIPTION</span></span>
<span data-ttu-id="7c679-115">Set-AzNetworkWatcherConnectionMonitor cmdlet은 연결 모니터 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="7c679-116">예제의</span><span class="sxs-lookup"><span data-stu-id="7c679-116">EXAMPLES</span></span>

### <span data-ttu-id="7c679-117">예제 1: 연결 모니터 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c679-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="7c679-118">이 예제에서는 destinationAddress를 변경 하 고 태그를 추가 하 여 기존 연결 모니터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="7c679-119">변수</span><span class="sxs-lookup"><span data-stu-id="7c679-119">PARAMETERS</span></span>

### <span data-ttu-id="7c679-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c679-120">-AsJob</span></span>
<span data-ttu-id="7c679-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c679-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c679-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="7c679-122">-ConfigureOnly</span></span>
<span data-ttu-id="7c679-123">연결 모니터를 구성 하지만 시작 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="7c679-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c679-124">-DefaultProfile</span></span>
<span data-ttu-id="7c679-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c679-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7c679-126">-DestinationAddress</span></span>
<span data-ttu-id="7c679-127">연결 모니터 대상 (IP 또는 도메인 이름)의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="7c679-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7c679-128">-DestinationPort</span></span>
<span data-ttu-id="7c679-129">연결 모니터에 사용 되는 대상 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="7c679-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="7c679-130">-DestinationResourceId</span></span>
<span data-ttu-id="7c679-131">연결 모니터에서 대상으로 사용 되는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="7c679-132">-Force</span><span class="sxs-lookup"><span data-stu-id="7c679-132">-Force</span></span>
<span data-ttu-id="7c679-133">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="7c679-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7c679-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c679-134">-InputObject</span></span>
<span data-ttu-id="7c679-135">연결 모니터 개체</span><span class="sxs-lookup"><span data-stu-id="7c679-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="7c679-136">-위치</span><span class="sxs-lookup"><span data-stu-id="7c679-136">-Location</span></span>
<span data-ttu-id="7c679-137">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7c679-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7c679-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="7c679-139">모니터링 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="7c679-140">기본값은 60 초입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="7c679-141">-이름</span><span class="sxs-lookup"><span data-stu-id="7c679-141">-Name</span></span>
<span data-ttu-id="7c679-142">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="7c679-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7c679-143">-NetworkWatcher</span></span>
<span data-ttu-id="7c679-144">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="7c679-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="7c679-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7c679-145">-NetworkWatcherName</span></span>
<span data-ttu-id="7c679-146">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="7c679-147">-메모</span><span class="sxs-lookup"><span data-stu-id="7c679-147">-Note</span></span>
<span data-ttu-id="7c679-148">연결 모니터와 연결 된 노트입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="7c679-149">-출력</span><span class="sxs-lookup"><span data-stu-id="7c679-149">-Output</span></span>
<span data-ttu-id="7c679-150">연결 모니터 출력 대상에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="7c679-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c679-151">-ResourceGroupName</span></span>
<span data-ttu-id="7c679-152">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7c679-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c679-153">-ResourceId</span></span>
<span data-ttu-id="7c679-154">ConnectionMonitor 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="7c679-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="7c679-155">-SourcePort</span></span>
<span data-ttu-id="7c679-156">연결 모니터에 사용 되는 원본 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="7c679-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7c679-157">-SourceResourceId</span></span>
<span data-ttu-id="7c679-158">연결 모니터에서 원본으로 사용 하는 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="7c679-159">태그</span><span class="sxs-lookup"><span data-stu-id="7c679-159">-Tag</span></span>
<span data-ttu-id="7c679-160">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7c679-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="7c679-161">-TestGroup</span></span>
<span data-ttu-id="7c679-162">테스트 그룹의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-162">The list of test groups.</span></span>

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

### <span data-ttu-id="7c679-163">-확인</span><span class="sxs-lookup"><span data-stu-id="7c679-163">-Confirm</span></span>
<span data-ttu-id="7c679-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c679-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c679-165">-WhatIf</span></span>
<span data-ttu-id="7c679-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c679-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c679-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c679-168">CommonParameters</span></span>
<span data-ttu-id="7c679-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c679-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c679-170">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c679-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c679-171">입력</span><span class="sxs-lookup"><span data-stu-id="7c679-171">INPUTS</span></span>

### <span data-ttu-id="7c679-172">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7c679-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7c679-173">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c679-173">System.String</span></span>

### <span data-ttu-id="7c679-174">Microsoft. 네트워크 모델. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="7c679-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="7c679-175">출력</span><span class="sxs-lookup"><span data-stu-id="7c679-175">OUTPUTS</span></span>

### <span data-ttu-id="7c679-176">PSConnectionMonitorResultV1에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7c679-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="7c679-177">PSConnectionMonitorResultV2에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7c679-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="7c679-178">상속자</span><span class="sxs-lookup"><span data-stu-id="7c679-178">NOTES</span></span>

## <span data-ttu-id="7c679-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c679-179">RELATED LINKS</span></span>
