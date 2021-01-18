---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 6d4dca8cdaa9e80fd1417fd65a9200eb5e3ecf7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496483"
---
# <span data-ttu-id="271d2-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="271d2-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="271d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="271d2-102">SYNOPSIS</span></span>
<span data-ttu-id="271d2-103">대상 리소스에 대한 흐름 로깅을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="271d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="271d2-104">SYNTAX</span></span>

### <span data-ttu-id="271d2-105">SetFlowlogByResourceWithoutTA(기본값)</span><span class="sxs-lookup"><span data-stu-id="271d2-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271d2-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="271d2-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271d2-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="271d2-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="271d2-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="271d2-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271d2-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="271d2-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="271d2-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="271d2-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271d2-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="271d2-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="271d2-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="271d2-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="271d2-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="271d2-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="271d2-114">설명</span><span class="sxs-lookup"><span data-stu-id="271d2-114">DESCRIPTION</span></span>
<span data-ttu-id="271d2-115">이 Set-AzNetworkWatcherConfigFlowLog 리소스에 대한 흐름 로깅을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="271d2-116">구성할 속성에는 제공된 리소스에 대해 흐름 로깅을 사용할 수 있는지 여부, 로그를 보낼 구성된 저장소 계정, 흐름 로깅 형식 및 로그에 대한 보존 정책이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="271d2-117">현재 네트워크 보안 그룹은 흐름 로깅에 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="271d2-118">예제</span><span class="sxs-lookup"><span data-stu-id="271d2-118">EXAMPLES</span></span>

### <span data-ttu-id="271d2-119">예제 1: 지정된 NSG에 대한 흐름 로깅 구성</span><span class="sxs-lookup"><span data-stu-id="271d2-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="271d2-120">이 예제에서는 네트워크 보안 그룹에 대한 흐름 로깅 상태를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="271d2-121">응답에서 지정된 NSG에 흐름 로깅, 기본 형식 및 보존 정책 집합이 없는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="271d2-122">예제 2: 지정된 NSG에 대한 흐름 로깅을 구성하고 흐름 로깅 버전을 2로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="271d2-123">이 예제에서는 버전 2 로그가 지정된 NSG(네트워크 보안 그룹)에서 흐름 로깅을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="271d2-124">응답에서 지정된 NSG에 흐름 로깅이 사용하도록 설정되어 있으며, 형식이 설정되어 있으며, 보존 정책이 구성되지 않은 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="271d2-125">지역이 지정한 버전을 지원하지 않는 경우 Network Watcher는 해당 지역에 지원되는 기본 버전을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="271d2-126">예제 3: 지정된 NSG에 대한 흐름 로깅 및 트래픽 분석 구성</span><span class="sxs-lookup"><span data-stu-id="271d2-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="271d2-127">이 예제에서는 네트워크 보안 그룹에 대한 흐름 로깅 상태 및 트래픽 분석을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="271d2-128">응답에서 지정된 NSG에 흐름 로깅 및 트래픽 분석이 사용하도록 설정되어 있으며 기본 형식 및 보존 정책 집합이 없는 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="271d2-129">예제 4: 흐름 로깅 및 트래픽 분석이 구성된 지정된 NSG에 대한 트래픽 분석 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="271d2-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

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
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="271d2-130">이 예제에서는 앞에서 구성한 흐름 로깅 및 트래픽 분석이 있는 네트워크 보안 그룹에 대한 트래픽 분석을 사용하지 않도록 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="271d2-131">응답에서 지정된 NSG가 흐름 로깅을 사용하도록 설정했지만 트래픽 분석을 사용하지 않도록 설정한 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="271d2-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="271d2-132">PARAMETERS</span></span>

### <span data-ttu-id="271d2-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="271d2-133">-AsJob</span></span>
<span data-ttu-id="271d2-134">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="271d2-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="271d2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271d2-135">-DefaultProfile</span></span>
<span data-ttu-id="271d2-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="271d2-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="271d2-137">-EnableFlowLog</span></span>
<span data-ttu-id="271d2-138">흐름 로깅을 사용/사용하지 않도록 설정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="271d2-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="271d2-139">-EnableRetention</span></span>
<span data-ttu-id="271d2-140">보존을 사용/사용하지 않도록 설정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="271d2-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="271d2-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="271d2-142">보존을 사용/사용하지 않도록 설정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="271d2-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="271d2-143">-FormatType</span></span>
<span data-ttu-id="271d2-144">흐름 로그 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-144">Type of flow log format.</span></span>

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

### <span data-ttu-id="271d2-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="271d2-145">-FormatVersion</span></span>
<span data-ttu-id="271d2-146">흐름 로그 형식의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-146">Version of flow log format.</span></span>

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

### <span data-ttu-id="271d2-147">-Location</span><span class="sxs-lookup"><span data-stu-id="271d2-147">-Location</span></span>
<span data-ttu-id="271d2-148">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="271d2-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="271d2-149">-NetworkWatcher</span></span>
<span data-ttu-id="271d2-150">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="271d2-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="271d2-151">-NetworkWatcherName</span></span>
<span data-ttu-id="271d2-152">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="271d2-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="271d2-153">-ResourceGroupName</span></span>
<span data-ttu-id="271d2-154">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="271d2-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="271d2-155">-RetentionInDays</span></span>
<span data-ttu-id="271d2-156">흐름 로그 레코드를 보존할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="271d2-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="271d2-157">-StorageAccountId</span></span>
<span data-ttu-id="271d2-158">흐름 로그를 저장하는 데 사용되는 저장소 계정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="271d2-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="271d2-159">-TargetResourceId</span></span>
<span data-ttu-id="271d2-160">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-160">The target resource ID.</span></span>

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

### <span data-ttu-id="271d2-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="271d2-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="271d2-162">TA 서비스가 흐름 분석을 얼마나 자주 해야 하는지 결정하는 간격(분)을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span> <span data-ttu-id="271d2-163">지원되는 값은 10분 및 60분입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-163">Supported values are 10 and 60 minutes.</span></span>

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

### <span data-ttu-id="271d2-164">-Workspace</span><span class="sxs-lookup"><span data-stu-id="271d2-164">-Workspace</span></span>
<span data-ttu-id="271d2-165">트래픽 분석 데이터를 저장하는 데 사용되는 WS 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-165">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="271d2-166">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="271d2-166">-WorkspaceGUID</span></span>
<span data-ttu-id="271d2-167">트래픽 분석 데이터를 저장하는 데 사용되는 WS의 GUID입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-167">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="271d2-168">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="271d2-168">-WorkspaceLocation</span></span>
<span data-ttu-id="271d2-169">트래픽 분석 데이터를 저장하는 데 사용되는 WS의 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-169">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="271d2-170">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="271d2-170">-WorkspaceResourceId</span></span>
<span data-ttu-id="271d2-171">트래픽 분석 데이터를 저장하는 데 사용되는 WS의 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-171">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="271d2-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="271d2-172">-Confirm</span></span>
<span data-ttu-id="271d2-173">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="271d2-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="271d2-174">-WhatIf</span></span>
<span data-ttu-id="271d2-175">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="271d2-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="271d2-176">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="271d2-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271d2-177">CommonParameters</span></span>
<span data-ttu-id="271d2-178">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="271d2-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271d2-179">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="271d2-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271d2-180">입력</span><span class="sxs-lookup"><span data-stu-id="271d2-180">INPUTS</span></span>

### <span data-ttu-id="271d2-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="271d2-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="271d2-182">System.String</span><span class="sxs-lookup"><span data-stu-id="271d2-182">System.String</span></span>

### <span data-ttu-id="271d2-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="271d2-183">System.Boolean</span></span>

### <span data-ttu-id="271d2-184">System.Int32</span><span class="sxs-lookup"><span data-stu-id="271d2-184">System.Int32</span></span>

### <span data-ttu-id="271d2-185">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="271d2-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="271d2-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="271d2-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="271d2-187">출력</span><span class="sxs-lookup"><span data-stu-id="271d2-187">OUTPUTS</span></span>

### <span data-ttu-id="271d2-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="271d2-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="271d2-189">참고 사항</span><span class="sxs-lookup"><span data-stu-id="271d2-189">NOTES</span></span>
<span data-ttu-id="271d2-190">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 감시자, 흐름, 로그, 흐름 로그, 로깅</span><span class="sxs-lookup"><span data-stu-id="271d2-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="271d2-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="271d2-191">RELATED LINKS</span></span>

[<span data-ttu-id="271d2-192">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="271d2-192">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="271d2-193">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="271d2-193">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="271d2-194">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="271d2-194">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="271d2-195">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="271d2-195">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="271d2-196">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="271d2-196">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="271d2-197">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="271d2-197">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="271d2-198">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="271d2-198">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="271d2-199">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="271d2-199">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="271d2-200">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="271d2-200">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="271d2-201">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="271d2-201">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="271d2-202">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="271d2-202">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="271d2-203">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="271d2-203">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="271d2-204">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="271d2-204">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="271d2-205">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="271d2-205">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="271d2-206">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="271d2-206">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="271d2-207">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="271d2-207">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="271d2-208">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="271d2-208">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="271d2-209">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="271d2-209">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="271d2-210">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="271d2-210">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="271d2-211">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="271d2-211">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="271d2-212">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="271d2-212">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="271d2-213">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="271d2-213">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="271d2-214">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="271d2-214">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="271d2-215">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="271d2-215">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="271d2-216">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="271d2-216">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="271d2-217">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="271d2-217">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="271d2-218">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="271d2-218">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
