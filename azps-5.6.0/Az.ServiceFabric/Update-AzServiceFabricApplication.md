---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: febf0ecb24be1b419353142805c9f91e0c771de5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955616"
---
# <span data-ttu-id="b5be3-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="b5be3-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="b5be3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5be3-102">SYNOPSIS</span></span>
<span data-ttu-id="b5be3-103">서비스 패브릭 애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-103">Update a service fabric application.</span></span> <span data-ttu-id="b5be3-104">이렇게 하면 애플리케이션 매개 변수를 업데이트하고/또는 애플리케이션 업그레이드를 트리거하는 애플리케이션 형식 버전을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="b5be3-105">배포된 애플리케이션만 ARM 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="b5be3-106">구문</span><span class="sxs-lookup"><span data-stu-id="b5be3-106">SYNTAX</span></span>

### <span data-ttu-id="b5be3-107">ByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="b5be3-107">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5be3-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5be3-108">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5be3-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5be3-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5be3-110">설명</span><span class="sxs-lookup"><span data-stu-id="b5be3-110">DESCRIPTION</span></span>
<span data-ttu-id="b5be3-111">이 cmdlet은 애플리케이션 매개 변수를 업데이트하고 애플리케이션 유형 버전을 업그레이드하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="b5be3-112">매개 변수를 업데이트하면 새 ARM 버전이 사용될 때만 명령이 애플리케이션 업그레이드를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="b5be3-113">지정된 형식 버전은 **New-AzServiceFabricApplicationTypeVersion** 을 사용하여 클러스터에 이미 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="b5be3-114">예제</span><span class="sxs-lookup"><span data-stu-id="b5be3-114">EXAMPLES</span></span>

### <span data-ttu-id="b5be3-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5be3-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="b5be3-116">이 예제에서는 **New-AzServiceFabricApplicationTypeVersion으로** 만든 형식 버전을 "v2"로 업데이트하기 위해 애플리케이션 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="b5be3-117">사용된 애플리케이션 매개 변수는 애플리케이션 매니페스트에 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="b5be3-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="b5be3-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="b5be3-119">이 예제에서는 애플리케이션에 대한 최소 및 최대 노드 제한을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="b5be3-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="b5be3-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="b5be3-121">이 예제에서는 형식 버전을 "v2"로 업데이트하기 위해 애플리케이션 업그레이드를 시작하고 현재 업그레이드에서 적용될 일부 업그레이드 정책 매개 변수도 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="b5be3-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="b5be3-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="b5be3-123">이 예제에서는 애플리케이션 매개 변수를 업데이트하지만 이러한 변경 내용은 다음 버전이 애플리케이션으로 업그레이드될 때까지만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="b5be3-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b5be3-124">PARAMETERS</span></span>

### <span data-ttu-id="b5be3-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="b5be3-125">-ApplicationParameter</span></span>
<span data-ttu-id="b5be3-126">애플리케이션 매개 변수를 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="b5be3-127">이러한 매개 변수는 애플리케이션 매니페스트에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-127">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="b5be3-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="b5be3-129">애플리케이션 유형 버전 지정</span><span class="sxs-lookup"><span data-stu-id="b5be3-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b5be3-130">-ClusterName</span></span>
<span data-ttu-id="b5be3-131">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-131">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="b5be3-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="b5be3-133">상태 평가 중에 경고 상태 이벤트를 오류 이벤트로 취급할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5be3-134">-DefaultProfile</span></span>
<span data-ttu-id="b5be3-135">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5be3-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="b5be3-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="b5be3-137">모니터링된 업그레이드에 사용할 기본 서비스 유형에 대해 상태 정책에서 허용하는 서비스당 비보정 파티션의 최대 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="b5be3-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="b5be3-139">모니터링된 업그레이드에 사용할 기본 서비스 유형에 대해 상태 정책에서 허용하는 서비스당 비보정 복제본의 최대 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="b5be3-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="b5be3-141">모니터링된 업그레이드에 사용할 기본 서비스 유형에 대해 상태 정책에서 허용하는 비보정 서비스의 최대 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="b5be3-142">-FailureAction</span></span>
<span data-ttu-id="b5be3-143">모니터링된 업그레이드가 실패하는 경우 취할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="b5be3-144">이 매개 변수에 대해 허용되는 값은 롤백 또는 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="b5be3-145">-ForceRestart</span></span>
<span data-ttu-id="b5be3-146">업그레이드가 구성 전용 변경인 경우에도 서비스 호스트가 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="b5be3-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="b5be3-148">이전 상태 검사가 실패하면 Service Fabric이 상태 검사를 다시 검색하는 기간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="b5be3-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="b5be3-150">서비스 패브릭이 다음 업그레이드 도메인으로 이동하거나 업그레이드를 완료하기 전에 애플리케이션이 안정되어 있는지 확인하기 위해 서비스 패브릭이 대기하는 기간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="b5be3-151">이 대기 기간은 상태 확인이 수행된 직후에 확인되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="b5be3-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="b5be3-153">업그레이드 도메인에서 업그레이드를 완료한 후 Service Fabric이 초기 상태 검사를 수행하기 전에 대기하는 기간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5be3-154">-InputObject</span></span>
<span data-ttu-id="b5be3-155">애플리케이션 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-155">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="b5be3-156">-MaximumNodeCount</span></span>
<span data-ttu-id="b5be3-157">애플리케이션을 두는 최대 노드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-157">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="b5be3-158">-MinimumNodeCount</span></span>
<span data-ttu-id="b5be3-159">Service Fabric이 이 애플리케이션에 대한 용량을 예약할 노드의 최소 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-160">-Name</span><span class="sxs-lookup"><span data-stu-id="b5be3-160">-Name</span></span>
<span data-ttu-id="b5be3-161">애플리케이션 이름 지정</span><span class="sxs-lookup"><span data-stu-id="b5be3-161">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5be3-162">-ResourceGroupName</span></span>
<span data-ttu-id="b5be3-163">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5be3-164">-ResourceId</span></span>
<span data-ttu-id="b5be3-165">애플리케이션의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-165">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="b5be3-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="b5be3-167">다른 서비스 형식에 사용할 상태 정책 맵을 다음 형식으로 해시 테이블로 지정합니다. @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}}</span><span class="sxs-lookup"><span data-stu-id="b5be3-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="b5be3-168">예: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="b5be3-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="b5be3-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="b5be3-170">클러스터의 애플리케이션 상태 상태가 오류가 발생하기 전에 클러스터의 노드에 배포된 애플리케이션 인스턴스의 최대 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="b5be3-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="b5be3-172">Service Fabric이 단일 업그레이드 도메인을 업그레이드하는 데 걸리는 최대 시간을 초로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="b5be3-173">이 기간이 지난 후 업그레이드가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-173">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="b5be3-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="b5be3-175">Service Fabric이 업그레이드를 진행하기 전에 서비스 패브릭이 안전한 상태로 다시 구성할 때까지 기다리는 최대 시간을 지정합니다. 아직 안전 상태가 아닌 경우.</span><span class="sxs-lookup"><span data-stu-id="b5be3-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="b5be3-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="b5be3-177">Service Fabric이 전체 업그레이드에 소요되는 최대 시간을 초로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="b5be3-178">이 기간이 지난 후 업그레이드가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-178">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be3-179">-확인</span><span class="sxs-lookup"><span data-stu-id="b5be3-179">-Confirm</span></span>
<span data-ttu-id="b5be3-180">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5be3-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5be3-181">-WhatIf</span></span>
<span data-ttu-id="b5be3-182">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5be3-183">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5be3-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5be3-184">CommonParameters</span></span>
<span data-ttu-id="b5be3-185">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5be3-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5be3-186">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5be3-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5be3-187">입력</span><span class="sxs-lookup"><span data-stu-id="b5be3-187">INPUTS</span></span>

### <span data-ttu-id="b5be3-188">System.String</span><span class="sxs-lookup"><span data-stu-id="b5be3-188">System.String</span></span>

### <span data-ttu-id="b5be3-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="b5be3-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="b5be3-190">출력</span><span class="sxs-lookup"><span data-stu-id="b5be3-190">OUTPUTS</span></span>

### <span data-ttu-id="b5be3-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="b5be3-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="b5be3-192">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b5be3-192">NOTES</span></span>

## <span data-ttu-id="b5be3-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5be3-193">RELATED LINKS</span></span>
