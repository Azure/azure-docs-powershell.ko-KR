---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 1fe3cb8227751553ac748fb99cf08baa044a6f0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214366"
---
# <span data-ttu-id="07c34-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="07c34-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="07c34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07c34-102">SYNOPSIS</span></span>
<span data-ttu-id="07c34-103">지정 된 네트워크 보안 그룹에 대 한 흐름 로그 리소스를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="07c34-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07c34-104">SYNTAX</span></span>

### <span data-ttu-id="07c34-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="07c34-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c34-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="07c34-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c34-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="07c34-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c34-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="07c34-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c34-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="07c34-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c34-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="07c34-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07c34-111">설명은</span><span class="sxs-lookup"><span data-stu-id="07c34-111">DESCRIPTION</span></span>
<span data-ttu-id="07c34-112">New-AzNetworkWatcherFlowLog 명령은 지정 된 네트워크 보안 그룹에 대 한 흐름 로그 리소스를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="07c34-113">예제의</span><span class="sxs-lookup"><span data-stu-id="07c34-113">EXAMPLES</span></span>

### <span data-ttu-id="07c34-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="07c34-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="07c34-115">이름: pstest Id:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid t e m/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag: W/ProvisioningState: 성공 위치: e us TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft./networkSecurityGroups StorageId: MyNSG s/Microsoft. Storage/Storageid/MySTorage 활성화 됨: 실제 보존 정책: {"일": true} 형식: {"Type": "JSON", "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": True, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "": "workspaceResourceId oups//subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr/", "FlowLogsV2Demo": 60}}</span><span class="sxs-lookup"><span data-stu-id="07c34-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="07c34-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="07c34-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="07c34-117">TrafficAnalytics가 구성 된 flowLog 리소스를 사용 하지 않도록 설정 하려면 TrafficAnalytics도 사용 하지 않도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="07c34-118">예제 2와 같이 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="07c34-119">이름: pstest Id:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid? t e m/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: 성공 위치: e<c13> us TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft. 네트워크/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. 저장소/Storageid/MySTorage 사용: False 보존 정책: 0, "사용": False} 형식: {"Type": "JSON", "Version": 1} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": False, "trafficAnalyticsInterval": 60}}</span><span class="sxs-lookup"><span data-stu-id="07c34-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="07c34-120">변수</span><span class="sxs-lookup"><span data-stu-id="07c34-120">PARAMETERS</span></span>

### <span data-ttu-id="07c34-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c34-121">-DefaultProfile</span></span>
<span data-ttu-id="07c34-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07c34-123">-사용</span><span class="sxs-lookup"><span data-stu-id="07c34-123">-Enabled</span></span>
<span data-ttu-id="07c34-124">흐름 로깅을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-124">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="07c34-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="07c34-125">-EnableRetention</span></span>
<span data-ttu-id="07c34-126">보존을 설정/해제 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-126">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="07c34-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="07c34-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="07c34-128">TrafficAnalytics를 사용 하거나 사용 하지 않도록 설정 하는 플래그</span><span class="sxs-lookup"><span data-stu-id="07c34-128">Flag to enable/disable TrafficAnalytics</span></span>

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

### <span data-ttu-id="07c34-129">-Force</span><span class="sxs-lookup"><span data-stu-id="07c34-129">-Force</span></span>
<span data-ttu-id="07c34-130">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="07c34-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="07c34-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="07c34-131">-FormatType</span></span>
<span data-ttu-id="07c34-132">흐름 로그의 파일 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-132">The file type of flow log.</span></span>
<span data-ttu-id="07c34-133">현재 ' JSON ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-133">The only supported value now is 'JSON'.</span></span>

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

### <span data-ttu-id="07c34-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="07c34-134">-FormatVersion</span></span>
<span data-ttu-id="07c34-135">흐름 로그의 버전 (개정)입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-135">The version (revision) of the flow log.</span></span>

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

### <span data-ttu-id="07c34-136">-위치</span><span class="sxs-lookup"><span data-stu-id="07c34-136">-Location</span></span>
<span data-ttu-id="07c34-137">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="07c34-138">-이름</span><span class="sxs-lookup"><span data-stu-id="07c34-138">-Name</span></span>
<span data-ttu-id="07c34-139">흐름 로그 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-139">The flow log name.</span></span>

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

### <span data-ttu-id="07c34-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07c34-140">-NetworkWatcher</span></span>
<span data-ttu-id="07c34-141">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="07c34-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="07c34-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="07c34-142">-NetworkWatcherName</span></span>
<span data-ttu-id="07c34-143">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="07c34-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07c34-144">-ResourceGroupName</span></span>
<span data-ttu-id="07c34-145">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="07c34-146">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="07c34-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="07c34-147">흐름 로그 기록을 유지할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-147">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="07c34-148">-StorageId</span><span class="sxs-lookup"><span data-stu-id="07c34-148">-StorageId</span></span>
<span data-ttu-id="07c34-149">흐름 로그를 저장 하는 데 사용 되는 저장소 계정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-149">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="07c34-150">태그</span><span class="sxs-lookup"><span data-stu-id="07c34-150">-Tag</span></span>
<span data-ttu-id="07c34-151">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-151">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="07c34-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="07c34-152">-TargetResourceId</span></span>
<span data-ttu-id="07c34-153">흐름 로그가 적용 되는 네트워크 보안 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-153">ID of network security group to which flow log will be applied.</span></span>

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

### <span data-ttu-id="07c34-154">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="07c34-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="07c34-155">TA 서비스에서 분석을 수행 하는 빈도를 결정 하는 간격 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="07c34-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="07c34-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="07c34-157">첨부 된 작업 영역의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-157">Resource Id of the attached workspace.</span></span>

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

### <span data-ttu-id="07c34-158">-확인</span><span class="sxs-lookup"><span data-stu-id="07c34-158">-Confirm</span></span>
<span data-ttu-id="07c34-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07c34-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07c34-160">-WhatIf</span></span>
<span data-ttu-id="07c34-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07c34-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07c34-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c34-163">CommonParameters</span></span>
<span data-ttu-id="07c34-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07c34-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c34-165">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07c34-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c34-166">입력</span><span class="sxs-lookup"><span data-stu-id="07c34-166">INPUTS</span></span>

### <span data-ttu-id="07c34-167">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07c34-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="07c34-168">출력</span><span class="sxs-lookup"><span data-stu-id="07c34-168">OUTPUTS</span></span>

### <span data-ttu-id="07c34-169">Microsoft. 네트워크 모델. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="07c34-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="07c34-170">상속자</span><span class="sxs-lookup"><span data-stu-id="07c34-170">NOTES</span></span>

## <span data-ttu-id="07c34-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07c34-171">RELATED LINKS</span></span>

[<span data-ttu-id="07c34-172">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07c34-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="07c34-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07c34-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="07c34-174">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07c34-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="07c34-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="07c34-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="07c34-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="07c34-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="07c34-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="07c34-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="07c34-178">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="07c34-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="07c34-179">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07c34-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07c34-180">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="07c34-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="07c34-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07c34-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07c34-182">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07c34-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07c34-183">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07c34-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07c34-184">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="07c34-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="07c34-185">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="07c34-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="07c34-186">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="07c34-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="07c34-187">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07c34-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07c34-188">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07c34-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07c34-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07c34-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07c34-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="07c34-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="07c34-191">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07c34-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07c34-192">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07c34-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07c34-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="07c34-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="07c34-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="07c34-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="07c34-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="07c34-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="07c34-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="07c34-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="07c34-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="07c34-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="07c34-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07c34-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="07c34-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="07c34-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="07c34-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="07c34-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="07c34-201">제거-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="07c34-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
