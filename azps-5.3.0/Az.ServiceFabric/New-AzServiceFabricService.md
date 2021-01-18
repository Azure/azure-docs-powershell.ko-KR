---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 930d86e457bef446d282db95d4289913bdcf10b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494769"
---
# <span data-ttu-id="235b7-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="235b7-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="235b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="235b7-102">SYNOPSIS</span></span>
<span data-ttu-id="235b7-103">지정된 애플리케이션 및 클러스터에서 새 Service Fabric 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="235b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="235b7-104">SYNTAX</span></span>

### <span data-ttu-id="235b7-105">Stateless-Singleton(기본값)</span><span class="sxs-lookup"><span data-stu-id="235b7-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="235b7-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="235b7-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="235b7-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="235b7-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235b7-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="235b7-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235b7-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="235b7-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="235b7-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="235b7-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="235b7-111">설명</span><span class="sxs-lookup"><span data-stu-id="235b7-111">DESCRIPTION</span></span>
<span data-ttu-id="235b7-112">이 cmdlet을 사용하면 지정된 애플리케이션에서 상태 비장 또는 상태 비장 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="235b7-113">서비스는 애플리케이션 매니페스트에서 종료해야 합니다. 형식은 매니페스트의 형식과 동일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="235b7-114">애플리케이션 이름은 서비스 이름의 prefix입니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="235b7-115">예제</span><span class="sxs-lookup"><span data-stu-id="235b7-115">EXAMPLES</span></span>

### <span data-ttu-id="235b7-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="235b7-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="235b7-117">이 예제에서는 인스턴스 수 -1(모든 노드)를 사용하여 새 상태 비어 있는 서비스 "testApp~testService1"을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="235b7-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="235b7-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="235b7-119">이 예제에서는 5개 노드를 대상으로 하는 새 상태 관리 서비스 "testApp~testService2"를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="235b7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="235b7-120">PARAMETERS</span></span>

### <span data-ttu-id="235b7-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="235b7-121">-ApplicationName</span></span>
<span data-ttu-id="235b7-122">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="235b7-123">-ClusterName</span></span>
<span data-ttu-id="235b7-124">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="235b7-125">-DefaultMoveCost</span></span>
<span data-ttu-id="235b7-126">이동에 대한 기본 비용을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="235b7-127">비용이 높을수록 클러스터 균형을 조정하려고 할 때 Cluster Resource Manager가 복제본을 이동할 가능성이 줄어 니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="235b7-128">-DefaultProfile</span></span>
<span data-ttu-id="235b7-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="235b7-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="235b7-130">-InstanceCount</span></span>
<span data-ttu-id="235b7-131">서비스에 대한 인스턴스 수 지정</span><span class="sxs-lookup"><span data-stu-id="235b7-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="235b7-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="235b7-133">서비스에 대한 최소 복제본 집합 크기 지정</span><span class="sxs-lookup"><span data-stu-id="235b7-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-134">-Name</span><span class="sxs-lookup"><span data-stu-id="235b7-134">-Name</span></span>
<span data-ttu-id="235b7-135">서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="235b7-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="235b7-137">서비스가 명명된 파티션 구성표를 사용 중임</span><span class="sxs-lookup"><span data-stu-id="235b7-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="235b7-138">이 모델을 사용하는 서비스에는 일반적으로 바인딩된 집합 내에서 버킷할 수 있는 데이터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="235b7-139">명명된 파티션 키로 사용되는 데이터 필드의 몇 가지 일반적인 예로는 지역, 우편 번호, 고객 그룹 또는 기타 비즈니스 경계가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="235b7-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="235b7-141">서비스가 싱글톤 파티션 구성표를 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="235b7-142">싱글톤 파티션은 일반적으로 서비스에 추가 라우팅이 필요하지 않은 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="235b7-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="235b7-144">서비스가 UniformInt64 파티션 구성표를 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="235b7-145">즉, 각 파티션은 int64 키 범위를 소유합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="235b7-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="235b7-147">서비스의 쿼럼 손실 대기 기간 지정</span><span class="sxs-lookup"><span data-stu-id="235b7-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="235b7-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="235b7-149">서비스에 대한 복제본 다시 시작 대기 기간 지정</span><span class="sxs-lookup"><span data-stu-id="235b7-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="235b7-150">-ResourceGroupName</span></span>
<span data-ttu-id="235b7-151">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-151">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="235b7-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="235b7-153">서비스에 대한 대기 복제본 기간 지정</span><span class="sxs-lookup"><span data-stu-id="235b7-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="235b7-154">-Stateful</span></span>
<span data-ttu-id="235b7-155">상태 비우기 서비스에 사용</span><span class="sxs-lookup"><span data-stu-id="235b7-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-156">-Stateless</span><span class="sxs-lookup"><span data-stu-id="235b7-156">-Stateless</span></span>
<span data-ttu-id="235b7-157">상태 비어 있는 서비스에 사용</span><span class="sxs-lookup"><span data-stu-id="235b7-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="235b7-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="235b7-159">서비스에 대한 대상 복제본 집합 크기 지정</span><span class="sxs-lookup"><span data-stu-id="235b7-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-160">-Type</span><span class="sxs-lookup"><span data-stu-id="235b7-160">-Type</span></span>
<span data-ttu-id="235b7-161">애플리케이션 매니페스트에 존재해야 하는 애플리케이션의 서비스 유형 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="235b7-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="235b7-162">-Confirm</span></span>
<span data-ttu-id="235b7-163">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="235b7-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="235b7-164">-WhatIf</span></span>
<span data-ttu-id="235b7-165">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="235b7-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="235b7-166">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="235b7-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="235b7-167">CommonParameters</span></span>
<span data-ttu-id="235b7-168">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="235b7-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="235b7-169">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="235b7-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="235b7-170">입력</span><span class="sxs-lookup"><span data-stu-id="235b7-170">INPUTS</span></span>

### <span data-ttu-id="235b7-171">System.String</span><span class="sxs-lookup"><span data-stu-id="235b7-171">System.String</span></span>

## <span data-ttu-id="235b7-172">출력</span><span class="sxs-lookup"><span data-stu-id="235b7-172">OUTPUTS</span></span>

### <span data-ttu-id="235b7-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="235b7-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="235b7-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="235b7-174">NOTES</span></span>

## <span data-ttu-id="235b7-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="235b7-175">RELATED LINKS</span></span>
