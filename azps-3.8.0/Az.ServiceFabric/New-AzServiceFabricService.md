---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: c4a082847c8d86271d7ded5d03f9c7c27c00501b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041721"
---
# <span data-ttu-id="ee352-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ee352-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="ee352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee352-102">SYNOPSIS</span></span>
<span data-ttu-id="ee352-103">지정 된 응용 프로그램 및 클러스터 아래에 새 service fabric 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="ee352-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee352-104">SYNTAX</span></span>

### <span data-ttu-id="ee352-105">Stateless-Singleton (기본값)</span><span class="sxs-lookup"><span data-stu-id="ee352-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee352-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="ee352-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee352-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="ee352-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee352-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="ee352-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee352-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="ee352-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee352-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="ee352-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee352-111">설명은</span><span class="sxs-lookup"><span data-stu-id="ee352-111">DESCRIPTION</span></span>
<span data-ttu-id="ee352-112">이 cmdlet은 지정 된 응용 프로그램에서 상태 비저장 또는 상태 저장 서비스를 만들 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="ee352-113">서비스는 응용 프로그램 매니페스트에서 종료 되어야 하며, 형식이 매니페스트의 형식과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="ee352-114">응용 프로그램 이름은 서비스 이름의 접두사 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="ee352-115">예제의</span><span class="sxs-lookup"><span data-stu-id="ee352-115">EXAMPLES</span></span>

### <span data-ttu-id="ee352-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee352-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="ee352-117">이 예제에서는 인스턴스 개수-1을 사용 하 여 ' testApp ~ testService1 "새 상태 비저장 서비스를 만듭니다 (모든 노드에서).</span><span class="sxs-lookup"><span data-stu-id="ee352-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="ee352-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="ee352-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="ee352-119">이 예제에서는 5 개 노드를 대상으로 하는 새 스테이트 풀 서비스 "testApp ~ testService2"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="ee352-120">변수</span><span class="sxs-lookup"><span data-stu-id="ee352-120">PARAMETERS</span></span>

### <span data-ttu-id="ee352-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="ee352-121">-ApplicationName</span></span>
<span data-ttu-id="ee352-122">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="ee352-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ee352-123">-ClusterName</span></span>
<span data-ttu-id="ee352-124">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ee352-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="ee352-125">-DefaultMoveCost</span></span>
<span data-ttu-id="ee352-126">이동에 대 한 기본 비용을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="ee352-127">비용을 더 높이면 클러스터의 균형을 유지 하려고 할 때 클러스터 리소스 관리자가 복제본을 이동 하 게 될 가능성을 줄일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

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

### <span data-ttu-id="ee352-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee352-128">-DefaultProfile</span></span>
<span data-ttu-id="ee352-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee352-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="ee352-130">-InstanceCount</span></span>
<span data-ttu-id="ee352-131">서비스의 인스턴스 수 지정</span><span class="sxs-lookup"><span data-stu-id="ee352-131">Specify the instance count for the service</span></span>

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

### <span data-ttu-id="ee352-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="ee352-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="ee352-133">서비스의 최소 복제 세트 크기 지정</span><span class="sxs-lookup"><span data-stu-id="ee352-133">Specify the min replica set size for the service</span></span>

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

### <span data-ttu-id="ee352-134">-이름</span><span class="sxs-lookup"><span data-stu-id="ee352-134">-Name</span></span>
<span data-ttu-id="ee352-135">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-135">Specify the name of the service.</span></span>

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

### <span data-ttu-id="ee352-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="ee352-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="ee352-137">서비스가 명명 된 파티션 구성표를 사용 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="ee352-138">일반적으로이 모델을 사용 하는 서비스는 경계 집합 내에서 bucketed 수 있는 데이터를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="ee352-139">명명 된 파티션 키로 사용 되는 데이터 필드의 몇 가지 일반적인 예는 지역, 우편 번호, 고객 그룹 또는 기타 비즈니스 경계입니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

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

### <span data-ttu-id="ee352-140">-파티션 구성표에 있음</span><span class="sxs-lookup"><span data-stu-id="ee352-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="ee352-141">서비스가 singleton 파티션 구성표를 사용 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="ee352-142">단일 파티션은 서비스에 추가 라우팅이 필요 하지 않은 경우 일반적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

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

### <span data-ttu-id="ee352-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="ee352-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="ee352-144">서비스가 UniformInt64 파티션 구성표를 사용 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="ee352-145">즉, 각 파티션은 여러 int64 키를 소유 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-145">This means that each partition owns a range of int64 keys.</span></span>

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

### <span data-ttu-id="ee352-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="ee352-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="ee352-147">서비스에 대 한 쿼럼 손실 대기 시간 지정</span><span class="sxs-lookup"><span data-stu-id="ee352-147">Specify the quorum loss wait duration for the service</span></span>

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

### <span data-ttu-id="ee352-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="ee352-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="ee352-149">서비스에 대 한 복제본 다시 시작 대기 시간 지정</span><span class="sxs-lookup"><span data-stu-id="ee352-149">Specify the replica restart wait duration for the service</span></span>

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

### <span data-ttu-id="ee352-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee352-150">-ResourceGroupName</span></span>
<span data-ttu-id="ee352-151">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ee352-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="ee352-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="ee352-153">서비스에 대해 복제본으로 대기 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-153">Specify the stand by replica duration for the service</span></span>

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

### <span data-ttu-id="ee352-154">-스테이트 풀</span><span class="sxs-lookup"><span data-stu-id="ee352-154">-Stateful</span></span>
<span data-ttu-id="ee352-155">스테이트 풀 서비스에 사용</span><span class="sxs-lookup"><span data-stu-id="ee352-155">Use for stateful service</span></span>

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

### <span data-ttu-id="ee352-156">-상태 비저장</span><span class="sxs-lookup"><span data-stu-id="ee352-156">-Stateless</span></span>
<span data-ttu-id="ee352-157">상태 비저장 서비스에 사용</span><span class="sxs-lookup"><span data-stu-id="ee352-157">Use for stateless service</span></span>

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

### <span data-ttu-id="ee352-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="ee352-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="ee352-159">서비스에 대 한 대상 복제본 집합 크기 지정</span><span class="sxs-lookup"><span data-stu-id="ee352-159">Specify the target replica set size for the service</span></span>

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

### <span data-ttu-id="ee352-160">-Type</span><span class="sxs-lookup"><span data-stu-id="ee352-160">-Type</span></span>
<span data-ttu-id="ee352-161">응용 프로그램 매니페스트에 있어야 하는 응용 프로그램의 서비스 종류 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

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

### <span data-ttu-id="ee352-162">-확인</span><span class="sxs-lookup"><span data-stu-id="ee352-162">-Confirm</span></span>
<span data-ttu-id="ee352-163">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee352-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee352-164">-WhatIf</span></span>
<span data-ttu-id="ee352-165">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee352-166">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee352-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee352-167">CommonParameters</span></span>
<span data-ttu-id="ee352-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee352-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee352-169">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee352-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee352-170">입력</span><span class="sxs-lookup"><span data-stu-id="ee352-170">INPUTS</span></span>

### <span data-ttu-id="ee352-171">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee352-171">System.String</span></span>

## <span data-ttu-id="ee352-172">출력</span><span class="sxs-lookup"><span data-stu-id="ee352-172">OUTPUTS</span></span>

### <span data-ttu-id="ee352-173">ServiceFabric. a i m. PSService</span><span class="sxs-lookup"><span data-stu-id="ee352-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="ee352-174">상속자</span><span class="sxs-lookup"><span data-stu-id="ee352-174">NOTES</span></span>

## <span data-ttu-id="ee352-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee352-175">RELATED LINKS</span></span>
