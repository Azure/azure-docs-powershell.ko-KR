---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: 779561ee3ff0a0b687104bd828890c314612f100
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307877"
---
# <span data-ttu-id="d0f36-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d0f36-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="d0f36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f36-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f36-103">서비스 패브릭 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-103">Update a service fabric application.</span></span> <span data-ttu-id="d0f36-104">이렇게 하면 응용 프로그램 매개 변수를 업데이트 하 고 응용 프로그램 업그레이드를 트리거할 응용 프로그램 유형 버전을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="d0f36-105">구문과</span><span class="sxs-lookup"><span data-stu-id="d0f36-105">SYNTAX</span></span>

### <span data-ttu-id="d0f36-106">ByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0f36-106">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="d0f36-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f36-107">ByResourceId</span></span>
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

### <span data-ttu-id="d0f36-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0f36-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f36-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d0f36-109">DESCRIPTION</span></span>
<span data-ttu-id="d0f36-110">이 cmdlet을 사용 하 여 응용 프로그램 매개 변수를 업데이트 하 고 응용 프로그램 유형 버전을 업그레이드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="d0f36-111">매개 변수를 업데이트 하면 새 형식 버전을 사용 하는 경우에만 ARM의 모델을 변경할 수 있으며,이 명령은 응용 프로그램 업그레이드를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="d0f36-112">지정 된 유형 버전은 **New-AzServiceFabricApplicationTypeVersion** 를 사용 하 여 클러스터에 이미 생성 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="d0f36-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d0f36-113">EXAMPLES</span></span>

### <span data-ttu-id="d0f36-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0f36-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="d0f36-115">이 예제에서는 응용 프로그램 업그레이드를 시작 하 여 type 버전을 **New-AzServiceFabricApplicationTypeVersion** 를 사용 하 여 만든 "v2"로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="d0f36-116">사용 된 응용 프로그램 매개 변수는 응용 프로그램 매니페스트에서 정의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="d0f36-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="d0f36-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="d0f36-118">이 예제에서는 응용 프로그램에 대 한 최소 및 최대 노드 제한 수를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="d0f36-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="d0f36-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="d0f36-120">이 예제에서는 응용 프로그램 업그레이드를 시작 하 여 형식 버전을 "v2"로 업데이트 하 고 현재 업그레이드에서 적용 되는 일부 업그레이드 정책 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="d0f36-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="d0f36-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="d0f36-122">이 예제에서는 응용 프로그램 매개 변수를 업데이트 하지만 이러한 변경 내용은 응용 프로그램에 대 한 다음 버전 업그레이드 까지만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="d0f36-123">변수</span><span class="sxs-lookup"><span data-stu-id="d0f36-123">PARAMETERS</span></span>

### <span data-ttu-id="d0f36-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="d0f36-124">-ApplicationParameter</span></span>
<span data-ttu-id="d0f36-125">응용 프로그램 매개 변수를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="d0f36-126">이러한 매개 변수는 응용 프로그램 매니페스트에 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-126">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="d0f36-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d0f36-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="d0f36-128">응용 프로그램 종류 버전 지정</span><span class="sxs-lookup"><span data-stu-id="d0f36-128">Specify the application type version</span></span>

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

### <span data-ttu-id="d0f36-129">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d0f36-129">-ClusterName</span></span>
<span data-ttu-id="d0f36-130">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d0f36-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="d0f36-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="d0f36-132">상태 평가 중에 경고 상태 이벤트를 오류 이벤트로 처리할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="d0f36-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f36-133">-DefaultProfile</span></span>
<span data-ttu-id="d0f36-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f36-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="d0f36-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="d0f36-136">모니터링 되는 업그레이드에 사용할 기본 서비스 종류에 대 한 상태 정책에서 허용 하는 서비스 당 최대 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d0f36-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="d0f36-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="d0f36-138">모니터링 되는 업그레이드에 사용할 기본 서비스 형식에 대 한 상태 정책에서 허용 하는 서비스 당 총 \ \ \ 번째 복제본의 최대 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d0f36-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="d0f36-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="d0f36-140">모니터링 되는 업그레이드에 사용할 기본 서비스 종류에 대 한 상태 정책에서 허용 하는 서비스의 최대 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d0f36-141">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="d0f36-141">-FailureAction</span></span>
<span data-ttu-id="d0f36-142">모니터링 되는 업그레이드가 실패할 경우 수행할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="d0f36-143">이 매개 변수에 허용 되는 값은 롤백 또는 수동입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="d0f36-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="d0f36-144">-ForceRestart</span></span>
<span data-ttu-id="d0f36-145">업그레이드가 구성 전용 변경 인 경우에도 서비스 호스트가 다시 시작 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="d0f36-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d0f36-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="d0f36-147">이전 상태 검사에 실패 한 경우 서비스 패브릭에서 상태 검사를 다시 시도 하는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="d0f36-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="d0f36-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="d0f36-149">다음 업그레이드 도메인으로 이동 하거나 업그레이드를 완료 하기 전에 응용 프로그램이 안정적인 지 확인 하기 위해 서비스 패브릭에서 대기 하는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="d0f36-150">이 대기 시간으로 상태 검사를 수행한 후에는 체력의 감지 되지 않은 변경을 방지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="d0f36-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="d0f36-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="d0f36-152">업그레이드 도메인에서 업그레이드를 완료 한 후 초기 상태 검사를 수행 하기 전에 서비스 패브릭에서 대기 하는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="d0f36-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0f36-153">-InputObject</span></span>
<span data-ttu-id="d0f36-154">응용 프로그램 리소스.</span><span class="sxs-lookup"><span data-stu-id="d0f36-154">The application resource.</span></span>

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

### <span data-ttu-id="d0f36-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="d0f36-155">-MaximumNodeCount</span></span>
<span data-ttu-id="d0f36-156">응용 프로그램을 배치할 최대 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-156">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="d0f36-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="d0f36-157">-MinimumNodeCount</span></span>
<span data-ttu-id="d0f36-158">서비스 패브릭에서이 응용 프로그램에 대 한 용량을 예약할 최소 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="d0f36-159">-이름</span><span class="sxs-lookup"><span data-stu-id="d0f36-159">-Name</span></span>
<span data-ttu-id="d0f36-160">응용 프로그램 이름 지정</span><span class="sxs-lookup"><span data-stu-id="d0f36-160">Specify the name of the application</span></span>

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

### <span data-ttu-id="d0f36-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f36-161">-ResourceGroupName</span></span>
<span data-ttu-id="d0f36-162">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-162">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d0f36-163">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f36-163">-ResourceId</span></span>
<span data-ttu-id="d0f36-164">응용 프로그램의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-164">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="d0f36-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="d0f36-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="d0f36-166">@ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"} 형식의 해시 테이블로 여러 서비스 유형에 사용할 상태 정책의 맵을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="d0f36-167">예: @ {"ServiceTypeName01" = "5, 10, 5"; "ServiceTypeName02" = "5, 5, 5"}</span><span class="sxs-lookup"><span data-stu-id="d0f36-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="d0f36-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="d0f36-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="d0f36-169">클러스터의 응용 프로그램 상태 상태에 오류가 발생 하기 전에 상태를 표시 하는 클러스터의 노드에 배포 된 응용 프로그램 인스턴스의 최대 백분율을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="d0f36-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d0f36-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="d0f36-171">서비스 패브릭에서 단일 업그레이드 도메인을 업그레이드 하는 데 걸리는 최대 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="d0f36-172">이 기간이 지난 후에는 업그레이드가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-172">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="d0f36-173">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d0f36-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="d0f36-174">서비스 패브릭이 업그레이드를 진행 하기 전에 안전 하지 않은 상태에서 서비스가 안전한 상태로 다시 구성 될 때까지 서비스가 대기 하는 최대 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="d0f36-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d0f36-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="d0f36-176">서비스 패브릭에서 전체 업그레이드에 대해 걸리는 최대 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="d0f36-177">이 기간이 지난 후에는 업그레이드가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-177">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="d0f36-178">-확인</span><span class="sxs-lookup"><span data-stu-id="d0f36-178">-Confirm</span></span>
<span data-ttu-id="d0f36-179">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f36-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f36-180">-WhatIf</span></span>
<span data-ttu-id="d0f36-181">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f36-182">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f36-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f36-183">CommonParameters</span></span>
<span data-ttu-id="d0f36-184">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0f36-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f36-185">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0f36-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f36-186">입력</span><span class="sxs-lookup"><span data-stu-id="d0f36-186">INPUTS</span></span>

### <span data-ttu-id="d0f36-187">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0f36-187">System.String</span></span>

### <span data-ttu-id="d0f36-188">ServiceFabric 응용 프로그램의 경우</span><span class="sxs-lookup"><span data-stu-id="d0f36-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d0f36-189">출력</span><span class="sxs-lookup"><span data-stu-id="d0f36-189">OUTPUTS</span></span>

### <span data-ttu-id="d0f36-190">ServiceFabric 응용 프로그램의 경우</span><span class="sxs-lookup"><span data-stu-id="d0f36-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d0f36-191">상속자</span><span class="sxs-lookup"><span data-stu-id="d0f36-191">NOTES</span></span>

## <span data-ttu-id="d0f36-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0f36-192">RELATED LINKS</span></span>
