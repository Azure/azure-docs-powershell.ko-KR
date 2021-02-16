---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206685"
---
# <span data-ttu-id="8f7ca-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="8f7ca-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="8f7ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7ca-103">연결 모니터 V2 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="8f7ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="8f7ca-104">SYNTAX</span></span>

### <span data-ttu-id="8f7ca-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8f7ca-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7ca-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8f7ca-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f7ca-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8f7ca-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7ca-108">설명</span><span class="sxs-lookup"><span data-stu-id="8f7ca-108">DESCRIPTION</span></span>
<span data-ttu-id="8f7ca-109">New-AzNetworkWatcherConnectionMonitorObject cmdlet은 연결 모니터 V2 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="8f7ca-110">예제</span><span class="sxs-lookup"><span data-stu-id="8f7ca-110">EXAMPLES</span></span>

### <span data-ttu-id="8f7ca-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8f7ca-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="8f7ca-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="8f7ca-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="8f7ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f7ca-113">PARAMETERS</span></span>

### <span data-ttu-id="8f7ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7ca-114">-DefaultProfile</span></span>
<span data-ttu-id="8f7ca-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f7ca-116">-Location</span><span class="sxs-lookup"><span data-stu-id="8f7ca-116">-Location</span></span>
<span data-ttu-id="8f7ca-117">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8f7ca-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8f7ca-118">-Name</span></span>
<span data-ttu-id="8f7ca-119">연결 모니터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-119">The connection monitor name.</span></span>

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

### <span data-ttu-id="8f7ca-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8f7ca-120">-NetworkWatcher</span></span>
<span data-ttu-id="8f7ca-121">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7ca-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8f7ca-122">-NetworkWatcherName</span></span>
<span data-ttu-id="8f7ca-123">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="8f7ca-124">-Note</span><span class="sxs-lookup"><span data-stu-id="8f7ca-124">-Note</span></span>
<span data-ttu-id="8f7ca-125">연결 모니터와 연결된 메모입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="8f7ca-126">-Output</span><span class="sxs-lookup"><span data-stu-id="8f7ca-126">-Output</span></span>
<span data-ttu-id="8f7ca-127">연결 모니터 출력 대상을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-127">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f7ca-129">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8f7ca-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f7ca-130">-Tag</span></span>
<span data-ttu-id="8f7ca-131">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-131">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8f7ca-132">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="8f7ca-132">-TestGroup</span></span>
<span data-ttu-id="8f7ca-133">테스트 그룹 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-133">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7ca-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f7ca-134">-Confirm</span></span>
<span data-ttu-id="8f7ca-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7ca-136">-WhatIf</span></span>
<span data-ttu-id="8f7ca-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8f7ca-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7ca-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7ca-139">CommonParameters</span></span>
<span data-ttu-id="8f7ca-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7ca-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8f7ca-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7ca-142">입력</span><span class="sxs-lookup"><span data-stu-id="8f7ca-142">INPUTS</span></span>

### <span data-ttu-id="8f7ca-143">없음</span><span class="sxs-lookup"><span data-stu-id="8f7ca-143">None</span></span>

## <span data-ttu-id="8f7ca-144">출력</span><span class="sxs-lookup"><span data-stu-id="8f7ca-144">OUTPUTS</span></span>

### <span data-ttu-id="8f7ca-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="8f7ca-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="8f7ca-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8f7ca-146">NOTES</span></span>

## <span data-ttu-id="8f7ca-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f7ca-147">RELATED LINKS</span></span>
