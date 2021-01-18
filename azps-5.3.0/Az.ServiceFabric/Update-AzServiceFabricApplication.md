---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494737"
---
# <span data-ttu-id="f83df-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f83df-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="f83df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f83df-102">SYNOPSIS</span></span>
<span data-ttu-id="f83df-103">Service Fabric 애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-103">Update a service fabric application.</span></span> <span data-ttu-id="f83df-104">이렇게 하면 애플리케이션 매개 변수를 업데이트하고/또는 애플리케이션 업그레이드를 트리거하는 애플리케이션 유형 버전을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="f83df-105">배포된 ARM 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="f83df-106">구문</span><span class="sxs-lookup"><span data-stu-id="f83df-106">SYNTAX</span></span>

### <span data-ttu-id="f83df-107">ByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="f83df-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="f83df-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f83df-108">ByResourceId</span></span>
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

### <span data-ttu-id="f83df-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f83df-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f83df-110">설명</span><span class="sxs-lookup"><span data-stu-id="f83df-110">DESCRIPTION</span></span>
<span data-ttu-id="f83df-111">이 cmdlet을 사용하여 애플리케이션 매개 변수를 업데이트하고 애플리케이션 유형 버전을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="f83df-112">매개 변수를 업데이트하면 새 형식 버전이 사용되는 ARM 모델만 변경됩니다. 명령은 애플리케이션 업그레이드를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="f83df-113">지정된 형식 버전은 **New-AzServiceFabricApplicationTypeVersion을** 사용하여 클러스터에 이미 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="f83df-114">예제</span><span class="sxs-lookup"><span data-stu-id="f83df-114">EXAMPLES</span></span>

### <span data-ttu-id="f83df-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="f83df-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="f83df-116">이 예제에서는 **New-AzServiceFabricApplicationTypeVersion으로** 만든 형식 버전을 "v2"로 업데이트하는 애플리케이션 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="f83df-117">사용되는 애플리케이션 매개 변수는 애플리케이션 매니페스트에 정의해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="f83df-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="f83df-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="f83df-119">이 예제에서는 애플리케이션에 대한 최소 및 최대 노드 수 제한을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="f83df-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="f83df-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="f83df-121">이 예제에서는 유형 버전을 "v2"로 업데이트하는 애플리케이션 업그레이드를 시작하고 현재 업그레이드에서 적용될 일부 업그레이드 정책 매개 변수도 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="f83df-122">예제 4</span><span class="sxs-lookup"><span data-stu-id="f83df-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="f83df-123">이 예제에서는 애플리케이션 매개 변수를 업데이트하지만 이러한 변경 내용은 다음 버전이 애플리케이션으로 업그레이드될 때까지만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="f83df-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f83df-124">PARAMETERS</span></span>

### <span data-ttu-id="f83df-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="f83df-125">-ApplicationParameter</span></span>
<span data-ttu-id="f83df-126">애플리케이션 매개 변수를 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="f83df-127">이러한 매개 변수는 애플리케이션 매니페스트에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="f83df-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f83df-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="f83df-129">애플리케이션 유형 버전 지정</span><span class="sxs-lookup"><span data-stu-id="f83df-129">Specify the application type version</span></span>

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

### <span data-ttu-id="f83df-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f83df-130">-ClusterName</span></span>
<span data-ttu-id="f83df-131">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f83df-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="f83df-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="f83df-133">상태 평가 중에 경고 상태 이벤트를 오류 이벤트로 취급할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="f83df-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83df-134">-DefaultProfile</span></span>
<span data-ttu-id="f83df-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f83df-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="f83df-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="f83df-137">모니터링된 업그레이드에 사용할 기본 서비스 유형에 대한 상태 정책에서 허용하는 서비스당 미지정 파티션의 최대 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="f83df-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="f83df-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="f83df-139">모니터링되는 업그레이드에 사용할 기본 서비스 유형에 대한 상태 정책에서 허용하는 서비스당 미지정 복제본의 최대 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="f83df-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="f83df-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="f83df-141">모니터링된 업그레이드에 사용할 기본 서비스 유형에 대한 상태 정책에서 허용하는 비보안 서비스의 최대 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="f83df-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="f83df-142">-FailureAction</span></span>
<span data-ttu-id="f83df-143">모니터링되는 업그레이드가 실패하는 경우 취할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="f83df-144">이 매개 변수에 허용되는 값은 Rollback 또는 Manual입니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="f83df-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="f83df-145">-ForceRestart</span></span>
<span data-ttu-id="f83df-146">업그레이드가 구성 전용 변경인 경우에도 서비스 호스트가 다시 시작된다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="f83df-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="f83df-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="f83df-148">이전 상태 검사가 실패하면 Service Fabric이 상태 검사를 다시 검색하는 기간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="f83df-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="f83df-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="f83df-150">Service Fabric이 다음 업그레이드 도메인으로 이동하거나 업그레이드를 완료하기 전에 애플리케이션이 안정적인지 확인하기 위해 대기하는 기간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="f83df-151">이 대기 기간은 상태 검사가 수행된 직후에 확인되지 않도록 상태 변경을 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="f83df-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="f83df-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="f83df-153">Service Fabric이 업그레이드 도메인에서 업그레이드를 완료한 후 초기 상태 검사를 수행하기 전에 대기하는 기간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="f83df-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f83df-154">-InputObject</span></span>
<span data-ttu-id="f83df-155">애플리케이션 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-155">The application resource.</span></span>

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

### <span data-ttu-id="f83df-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="f83df-156">-MaximumNodeCount</span></span>
<span data-ttu-id="f83df-157">애플리케이션을 두는 노드의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="f83df-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="f83df-158">-MinimumNodeCount</span></span>
<span data-ttu-id="f83df-159">Service Fabric이 이 애플리케이션에 대한 용량을 예약하는 노드의 최소 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="f83df-160">-Name</span><span class="sxs-lookup"><span data-stu-id="f83df-160">-Name</span></span>
<span data-ttu-id="f83df-161">애플리케이션의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="f83df-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="f83df-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83df-162">-ResourceGroupName</span></span>
<span data-ttu-id="f83df-163">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f83df-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f83df-164">-ResourceId</span></span>
<span data-ttu-id="f83df-165">애플리케이션의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="f83df-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="f83df-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="f83df-167">다양한 서비스 유형에 사용할 상태 정책 맵을 @"ServiceTypeName" @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}}으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="f83df-168">예: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="f83df-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="f83df-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="f83df-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="f83df-170">클러스터의 애플리케이션 상태 오류가 발생하기 전에 클러스터의 노드에 배포된 애플리케이션 인스턴스의 최대 백분율을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="f83df-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="f83df-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="f83df-172">Service Fabric이 단일 업그레이드 도메인을 업그레이드하는 데 걸리는 최대 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="f83df-173">이 기간 후에 업그레이드가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="f83df-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="f83df-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="f83df-175">Service Fabric이 업그레이드를 진행하기 전에 서비스 패브릭이 안전한 상태로 재구성할 때까지 대기하는 최대 시간을 지정합니다(안전 상태가 아닌 경우).</span><span class="sxs-lookup"><span data-stu-id="f83df-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="f83df-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="f83df-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="f83df-177">Service Fabric이 전체 업그레이드에 걸리는 최대 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="f83df-178">이 기간 후에 업그레이드가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="f83df-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f83df-179">-Confirm</span></span>
<span data-ttu-id="f83df-180">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f83df-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83df-181">-WhatIf</span></span>
<span data-ttu-id="f83df-182">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f83df-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f83df-183">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f83df-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83df-184">CommonParameters</span></span>
<span data-ttu-id="f83df-185">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f83df-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83df-186">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f83df-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83df-187">입력</span><span class="sxs-lookup"><span data-stu-id="f83df-187">INPUTS</span></span>

### <span data-ttu-id="f83df-188">System.String</span><span class="sxs-lookup"><span data-stu-id="f83df-188">System.String</span></span>

### <span data-ttu-id="f83df-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="f83df-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="f83df-190">출력</span><span class="sxs-lookup"><span data-stu-id="f83df-190">OUTPUTS</span></span>

### <span data-ttu-id="f83df-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="f83df-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="f83df-192">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f83df-192">NOTES</span></span>

## <span data-ttu-id="f83df-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f83df-193">RELATED LINKS</span></span>
