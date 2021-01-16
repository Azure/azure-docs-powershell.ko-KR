---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 1fe3cb8227751553ac748fb99cf08baa044a6f0d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491012"
---
# <span data-ttu-id="e3b7d-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="e3b7d-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="e3b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b7d-103">지정된 네트워크 보안 그룹에 대한 흐름 로그 리소스를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="e3b7d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3b7d-104">SYNTAX</span></span>

### <span data-ttu-id="e3b7d-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e3b7d-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b7d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e3b7d-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b7d-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="e3b7d-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b7d-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="e3b7d-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b7d-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e3b7d-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b7d-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="e3b7d-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b7d-111">설명</span><span class="sxs-lookup"><span data-stu-id="e3b7d-111">DESCRIPTION</span></span>
<span data-ttu-id="e3b7d-112">New-AzNetworkWatcherFlowLog 명령은 지정된 네트워크 보안 그룹에 대한 흐름 로그 리소스를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="e3b7d-113">예제</span><span class="sxs-lookup"><span data-stu-id="e3b7d-113">EXAMPLES</span></span>

### <span data-ttu-id="e3b7d-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3b7d-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="e3b7d-115">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="e3b7d-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="e3b7d-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3b7d-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="e3b7d-117">TrafficAnalytics가 구성된 flowLog 리소스를 사용하지 않도록 설정하려는 경우 TrafficAnalytics도 사용하지 않도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="e3b7d-118">예제 2와 같이 수행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="e3b7d-119">이름 : pstest Id : /subscriptions/bb-bbbb-bbbb-bbbb-bbbb-bb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-8 31f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : False RetentionPolicy : { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="e3b7d-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="e3b7d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3b7d-120">PARAMETERS</span></span>

### <span data-ttu-id="e3b7d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b7d-121">-DefaultProfile</span></span>
<span data-ttu-id="e3b7d-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e3b7d-123">-Enabled</span></span>
<span data-ttu-id="e3b7d-124">흐름 로깅을 사용/사용하지 않도록 설정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-124">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="e3b7d-125">-EnableRetention</span></span>
<span data-ttu-id="e3b7d-126">보존을 사용/사용하지 않도록 설정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-126">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="e3b7d-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="e3b7d-128">TrafficAnalytics를 사용/사용하지 않도록 설정하는 플래그</span><span class="sxs-lookup"><span data-stu-id="e3b7d-128">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e3b7d-129">-Force</span></span>
<span data-ttu-id="e3b7d-130">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e3b7d-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="e3b7d-131">-FormatType</span></span>
<span data-ttu-id="e3b7d-132">흐름 로그의 파일 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-132">The file type of flow log.</span></span>
<span data-ttu-id="e3b7d-133">이제 지원되는 유일한 값은 'JSON'입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-133">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="e3b7d-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="e3b7d-134">-FormatVersion</span></span>
<span data-ttu-id="e3b7d-135">흐름 로그의 버전(버전)입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-135">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="e3b7d-136">-Location</span><span class="sxs-lookup"><span data-stu-id="e3b7d-136">-Location</span></span>
<span data-ttu-id="e3b7d-137">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-137">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-138">-Name</span><span class="sxs-lookup"><span data-stu-id="e3b7d-138">-Name</span></span>
<span data-ttu-id="e3b7d-139">흐름 로그 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-139">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3b7d-140">-NetworkWatcher</span></span>
<span data-ttu-id="e3b7d-141">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-141">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e3b7d-142">-NetworkWatcherName</span></span>
<span data-ttu-id="e3b7d-143">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-143">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b7d-144">-ResourceGroupName</span></span>
<span data-ttu-id="e3b7d-145">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-145">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="e3b7d-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="e3b7d-147">흐름 로그 레코드를 보존할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-147">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="e3b7d-148">-StorageId</span><span class="sxs-lookup"><span data-stu-id="e3b7d-148">-StorageId</span></span>
<span data-ttu-id="e3b7d-149">흐름 로그를 저장하는 데 사용되는 저장소 계정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-149">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3b7d-150">-Tag</span></span>
<span data-ttu-id="e3b7d-151">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-151">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e3b7d-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e3b7d-152">-TargetResourceId</span></span>
<span data-ttu-id="e3b7d-153">흐름 로그를 적용할 네트워크 보안 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-153">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="e3b7d-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="e3b7d-155">TA 서비스가 흐름 분석을 얼마나 자주 해야 하는지 결정하는 분 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="e3b7d-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="e3b7d-157">연결된 작업 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-157">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3b7d-158">-Confirm</span></span>
<span data-ttu-id="e3b7d-159">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b7d-160">-WhatIf</span></span>
<span data-ttu-id="e3b7d-161">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3b7d-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b7d-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b7d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b7d-163">CommonParameters</span></span>
<span data-ttu-id="e3b7d-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b7d-165">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3b7d-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b7d-166">입력</span><span class="sxs-lookup"><span data-stu-id="e3b7d-166">INPUTS</span></span>

### <span data-ttu-id="e3b7d-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3b7d-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="e3b7d-168">출력</span><span class="sxs-lookup"><span data-stu-id="e3b7d-168">OUTPUTS</span></span>

### <span data-ttu-id="e3b7d-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="e3b7d-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="e3b7d-170">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3b7d-170">NOTES</span></span>

## <span data-ttu-id="e3b7d-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3b7d-171">RELATED LINKS</span></span>

[<span data-ttu-id="e3b7d-172">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3b7d-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e3b7d-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3b7d-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e3b7d-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3b7d-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e3b7d-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e3b7d-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e3b7d-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e3b7d-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e3b7d-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e3b7d-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e3b7d-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e3b7d-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e3b7d-179">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3b7d-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3b7d-180">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e3b7d-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e3b7d-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3b7d-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3b7d-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3b7d-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3b7d-183">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3b7d-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3b7d-184">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3b7d-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e3b7d-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e3b7d-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e3b7d-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e3b7d-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e3b7d-187">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3b7d-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3b7d-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3b7d-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3b7d-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3b7d-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3b7d-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e3b7d-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e3b7d-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3b7d-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3b7d-192">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3b7d-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e3b7d-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e3b7d-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e3b7d-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e3b7d-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e3b7d-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e3b7d-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e3b7d-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e3b7d-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e3b7d-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e3b7d-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e3b7d-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3b7d-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="e3b7d-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="e3b7d-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="e3b7d-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="e3b7d-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="e3b7d-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="e3b7d-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
