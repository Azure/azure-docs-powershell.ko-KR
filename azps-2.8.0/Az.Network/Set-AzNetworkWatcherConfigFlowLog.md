---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f2e063e6870ebfe41034441b7b3134694d9a85a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871977"
---
# <span data-ttu-id="e0f51-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e0f51-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="e0f51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0f51-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f51-103">대상 리소스에 대 한 흐름 로깅을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="e0f51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0f51-104">SYNTAX</span></span>

### <span data-ttu-id="e0f51-105">SetFlowlogByResourceWithoutTA (기본값)</span><span class="sxs-lookup"><span data-stu-id="e0f51-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f51-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="e0f51-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f51-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="e0f51-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0f51-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="e0f51-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f51-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="e0f51-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0f51-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="e0f51-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f51-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="e0f51-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0f51-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="e0f51-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0f51-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="e0f51-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0f51-114">설명은</span><span class="sxs-lookup"><span data-stu-id="e0f51-114">DESCRIPTION</span></span>
<span data-ttu-id="e0f51-115">Set-AzNetworkWatcherConfigFlowLog는 대상 리소스에 대 한 흐름 로깅을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="e0f51-116">구성할 속성에는 제공 된 리소스에 대해 흐름 로깅이 설정 되어 있는지 여부, 로그를 보낼 구성 된 저장소 계정, 흐름 로깅 형식, 로그에 대 한 보존 정책이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="e0f51-117">현재 네트워크 보안 그룹은 유동 로깅에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="e0f51-118">예제의</span><span class="sxs-lookup"><span data-stu-id="e0f51-118">EXAMPLES</span></span>

### <span data-ttu-id="e0f51-119">예제 1: 지정 된 NSG에 대 한 흐름 로깅 구성</span><span class="sxs-lookup"><span data-stu-id="e0f51-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="e0f51-120">이 예제에서는 네트워크 보안 그룹에 대 한 흐름 로깅 상태를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="e0f51-121">응답에서 지정 된 NSG에 흐름 로깅 사용, 기본 형식 및 보존 정책 설정이 없음이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="e0f51-122">예제 2: 지정 된 NSG에 대 한 흐름 로깅을 구성 하 고 흐름 로깅 버전을 2로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="e0f51-123">이 예제에서는 버전 2 로그가 지정 된 네트워크 보안 그룹 (NSG)에서 흐름 로깅을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="e0f51-124">응답에서 지정 된 NSG에 흐름 로깅이 사용 하도록 설정 되 고, 형식이 설정 되 고, 구성 된 보존 정책이 없음이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="e0f51-125">영역이 지정 된 버전을 지원 하지 않는 경우 네트워크 감시자는 지역에서 지원 되는 기본 버전을 작성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="e0f51-126">예제 3: 지정 된 NSG에 대 한 흐름 로깅 및 트래픽 분석 구성</span><span class="sxs-lookup"><span data-stu-id="e0f51-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="e0f51-127">이 예제에서는 네트워크 보안 그룹에 대 한 흐름 로깅 상태 및 트래픽 분석을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="e0f51-128">응답에서 지정 된 NSG에 흐름 로깅 및 트래픽 분석 사용, 기본 형식 및 보존 정책 설정이 없음이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="e0f51-129">변수</span><span class="sxs-lookup"><span data-stu-id="e0f51-129">PARAMETERS</span></span>

### <span data-ttu-id="e0f51-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0f51-130">-AsJob</span></span>
<span data-ttu-id="e0f51-131">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e0f51-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0f51-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f51-132">-DefaultProfile</span></span>
<span data-ttu-id="e0f51-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0f51-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="e0f51-134">-EnableFlowLog</span></span>
<span data-ttu-id="e0f51-135">흐름 로깅을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-135">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="e0f51-136">-EnableRetention</span></span>
<span data-ttu-id="e0f51-137">보존을 설정/해제 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-137">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="e0f51-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="e0f51-139">보존을 설정/해제 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-139">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-140">-FormatType</span><span class="sxs-lookup"><span data-stu-id="e0f51-140">-FormatType</span></span>
<span data-ttu-id="e0f51-141">흐름 로그 형식 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-141">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="e0f51-142">-FormatVersion</span></span>
<span data-ttu-id="e0f51-143">흐름 로그 형식 버전.</span><span class="sxs-lookup"><span data-stu-id="e0f51-143">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-144">-위치</span><span class="sxs-lookup"><span data-stu-id="e0f51-144">-Location</span></span>
<span data-ttu-id="e0f51-145">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-145">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-146">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0f51-146">-NetworkWatcher</span></span>
<span data-ttu-id="e0f51-147">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="e0f51-147">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e0f51-148">-NetworkWatcherName</span></span>
<span data-ttu-id="e0f51-149">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-149">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f51-150">-ResourceGroupName</span></span>
<span data-ttu-id="e0f51-151">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-151">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-152">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="e0f51-152">-RetentionInDays</span></span>
<span data-ttu-id="e0f51-153">흐름 로그 기록을 유지할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-153">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="e0f51-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e0f51-154">-StorageAccountId</span></span>
<span data-ttu-id="e0f51-155">흐름 로그를 저장 하는 데 사용 되는 저장소 계정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-155">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="e0f51-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f51-156">-TargetResourceId</span></span>
<span data-ttu-id="e0f51-157">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-157">The target resource ID.</span></span>

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

### <span data-ttu-id="e0f51-158">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="e0f51-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="e0f51-159">TA 서비스가 흐름 분석을 수행 해야 하는 빈도를 결정 하는 간격 (분)을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-160">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="e0f51-160">-Workspace</span></span>
<span data-ttu-id="e0f51-161">트래픽 분석 데이터를 저장 하는 데 사용 되는 WS 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-161">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-162">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="e0f51-162">-WorkspaceGUID</span></span>
<span data-ttu-id="e0f51-163">트래픽 분석 데이터를 저장 하는 데 사용 되는 WS의 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="e0f51-164">-WorkspaceLocation</span></span>
<span data-ttu-id="e0f51-165">트래픽 분석 데이터를 저장 하는 데 사용 되는 WS의 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e0f51-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="e0f51-167">트래픽 분석 데이터를 저장 하는 데 사용 되는 WS의 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f51-168">-확인</span><span class="sxs-lookup"><span data-stu-id="e0f51-168">-Confirm</span></span>
<span data-ttu-id="e0f51-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0f51-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f51-170">-WhatIf</span></span>
<span data-ttu-id="e0f51-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0f51-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0f51-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f51-173">CommonParameters</span></span>
<span data-ttu-id="e0f51-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0f51-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f51-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f51-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f51-176">입력</span><span class="sxs-lookup"><span data-stu-id="e0f51-176">INPUTS</span></span>

### <span data-ttu-id="e0f51-177">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0f51-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e0f51-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e0f51-178">System.String</span></span>

### <span data-ttu-id="e0f51-179">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e0f51-179">System.Boolean</span></span>

### <span data-ttu-id="e0f51-180">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="e0f51-180">System.Int32</span></span>

### <span data-ttu-id="e0f51-181">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="e0f51-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e0f51-182">IOperationalInsightWorkspace (네트워크. 내부. 일반)</span><span class="sxs-lookup"><span data-stu-id="e0f51-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="e0f51-183">출력</span><span class="sxs-lookup"><span data-stu-id="e0f51-183">OUTPUTS</span></span>

### <span data-ttu-id="e0f51-184">Microsoft. 네트워크 모델. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="e0f51-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="e0f51-185">상속자</span><span class="sxs-lookup"><span data-stu-id="e0f51-185">NOTES</span></span>
<span data-ttu-id="e0f51-186">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 흐름, 로그, flowlog, 로깅</span><span class="sxs-lookup"><span data-stu-id="e0f51-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="e0f51-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0f51-187">RELATED LINKS</span></span>

[<span data-ttu-id="e0f51-188">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0f51-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e0f51-189">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0f51-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e0f51-190">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0f51-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e0f51-191">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e0f51-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e0f51-192">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e0f51-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e0f51-193">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e0f51-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e0f51-194">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e0f51-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e0f51-195">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0f51-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0f51-196">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e0f51-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e0f51-197">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0f51-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0f51-198">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0f51-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0f51-199">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0f51-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0f51-200">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0f51-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e0f51-201">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e0f51-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e0f51-202">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e0f51-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e0f51-203">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0f51-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0f51-204">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0f51-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0f51-205">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0f51-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0f51-206">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e0f51-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e0f51-207">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0f51-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0f51-208">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0f51-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e0f51-209">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e0f51-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e0f51-210">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e0f51-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e0f51-211">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e0f51-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e0f51-212">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e0f51-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e0f51-213">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e0f51-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="e0f51-214">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0f51-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
