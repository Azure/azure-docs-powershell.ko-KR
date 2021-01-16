---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344186"
---
# <span data-ttu-id="dbf69-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="dbf69-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="dbf69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbf69-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf69-103">흐름 로그 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-103">Updates flow log resource.</span></span>

## <span data-ttu-id="dbf69-104">구문</span><span class="sxs-lookup"><span data-stu-id="dbf69-104">SYNTAX</span></span>

### <span data-ttu-id="dbf69-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="dbf69-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf69-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dbf69-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf69-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="dbf69-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf69-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="dbf69-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf69-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dbf69-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf69-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="dbf69-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf69-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dbf69-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf69-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="dbf69-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbf69-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="dbf69-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf69-114">설명</span><span class="sxs-lookup"><span data-stu-id="dbf69-114">DESCRIPTION</span></span>
<span data-ttu-id="dbf69-115">흐름 로그 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-115">Updates flow log resource.</span></span>

## <span data-ttu-id="dbf69-116">예제</span><span class="sxs-lookup"><span data-stu-id="dbf69-116">EXAMPLES</span></span>

### <span data-ttu-id="dbf69-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="dbf69-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="dbf69-118">이름 : pstest Id : /subscriptions/bb-bbbb-bbbb-bbbb-bbbb-bb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/bbbbbb-1bbbb-bbbb-bb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/bbbbbb-bbbb-bb-bb-bb-bb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled : True RetentionPolicy : { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "버전": 2 } FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="dbf69-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="dbf69-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbf69-119">PARAMETERS</span></span>

### <span data-ttu-id="dbf69-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf69-120">-DefaultProfile</span></span>
<span data-ttu-id="dbf69-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf69-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="dbf69-122">-Enabled</span></span>
<span data-ttu-id="dbf69-123">흐름 로깅을 사용/사용하지 않도록 설정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="dbf69-124">-EnableRetention</span></span>
<span data-ttu-id="dbf69-125">보존을 사용/사용하지 않도록 설정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="dbf69-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="dbf69-127">TrafficAnalytics를 사용/사용하지 않도록 설정하는 플래그</span><span class="sxs-lookup"><span data-stu-id="dbf69-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-128">-Force</span><span class="sxs-lookup"><span data-stu-id="dbf69-128">-Force</span></span>
<span data-ttu-id="dbf69-129">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="dbf69-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="dbf69-130">-FormatType</span></span>
<span data-ttu-id="dbf69-131">흐름 로그의 파일 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-131">The file type of flow log.</span></span>
<span data-ttu-id="dbf69-132">이제 지원되는 유일한 값은 'JSON'입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="dbf69-133">-FormatVersion</span></span>
<span data-ttu-id="dbf69-134">흐름 로그의 버전(버전)입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbf69-135">-InputObject</span></span>
<span data-ttu-id="dbf69-136">흐름 lof 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-137">-Location</span><span class="sxs-lookup"><span data-stu-id="dbf69-137">-Location</span></span>
<span data-ttu-id="dbf69-138">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-138">Location of the network watcher.</span></span>

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

### <span data-ttu-id="dbf69-139">-Name</span><span class="sxs-lookup"><span data-stu-id="dbf69-139">-Name</span></span>
<span data-ttu-id="dbf69-140">흐름 로그 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbf69-141">-NetworkWatcher</span></span>
<span data-ttu-id="dbf69-142">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="dbf69-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dbf69-143">-NetworkWatcherName</span></span>
<span data-ttu-id="dbf69-144">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="dbf69-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf69-145">-ResourceGroupName</span></span>
<span data-ttu-id="dbf69-146">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-146">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dbf69-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbf69-147">-ResourceId</span></span>
<span data-ttu-id="dbf69-148">FlowLog 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="dbf69-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="dbf69-150">흐름 로그 레코드를 보존할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="dbf69-151">-StorageId</span></span>
<span data-ttu-id="dbf69-152">흐름 로그를 저장하는 데 사용되는 저장소 계정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="dbf69-153">-Tag</span></span>
<span data-ttu-id="dbf69-154">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dbf69-155">-TargetResourceId</span></span>
<span data-ttu-id="dbf69-156">흐름 로그를 적용할 네트워크 보안 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="dbf69-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="dbf69-158">TA 서비스가 흐름 분석을 얼마나 자주 해야 하는지 결정하는 분 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="dbf69-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="dbf69-160">연결된 작업 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf69-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbf69-161">-Confirm</span></span>
<span data-ttu-id="dbf69-162">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf69-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf69-163">-WhatIf</span></span>
<span data-ttu-id="dbf69-164">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dbf69-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf69-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf69-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf69-166">CommonParameters</span></span>
<span data-ttu-id="dbf69-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dbf69-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf69-168">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dbf69-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf69-169">입력</span><span class="sxs-lookup"><span data-stu-id="dbf69-169">INPUTS</span></span>

### <span data-ttu-id="dbf69-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbf69-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="dbf69-171">System.String</span><span class="sxs-lookup"><span data-stu-id="dbf69-171">System.String</span></span>

### <span data-ttu-id="dbf69-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="dbf69-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="dbf69-173">출력</span><span class="sxs-lookup"><span data-stu-id="dbf69-173">OUTPUTS</span></span>

### <span data-ttu-id="dbf69-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="dbf69-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="dbf69-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dbf69-175">NOTES</span></span>

## <span data-ttu-id="dbf69-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbf69-176">RELATED LINKS</span></span>

[<span data-ttu-id="dbf69-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbf69-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="dbf69-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbf69-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="dbf69-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbf69-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="dbf69-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dbf69-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="dbf69-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dbf69-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dbf69-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dbf69-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="dbf69-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dbf69-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dbf69-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbf69-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbf69-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dbf69-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="dbf69-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbf69-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbf69-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbf69-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbf69-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbf69-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbf69-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbf69-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="dbf69-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dbf69-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="dbf69-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="dbf69-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="dbf69-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbf69-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbf69-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbf69-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbf69-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbf69-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbf69-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="dbf69-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="dbf69-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbf69-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbf69-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbf69-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbf69-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dbf69-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="dbf69-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="dbf69-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="dbf69-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="dbf69-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="dbf69-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="dbf69-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="dbf69-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="dbf69-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="dbf69-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbf69-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="dbf69-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="dbf69-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="dbf69-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="dbf69-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="dbf69-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="dbf69-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)