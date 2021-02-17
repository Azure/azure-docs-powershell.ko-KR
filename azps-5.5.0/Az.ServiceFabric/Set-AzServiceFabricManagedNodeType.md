---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191140"
---
# <span data-ttu-id="11578-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="11578-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="11578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11578-102">SYNOPSIS</span></span>
<span data-ttu-id="11578-103">-Reimage 매개 변수를 사용하여 노드 형식 리소스 속성을 설정하거나 노드 형식의 특정 ndes에서 다시IMAGE 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="11578-104">구문</span><span class="sxs-lookup"><span data-stu-id="11578-104">SYNTAX</span></span>

### <span data-ttu-id="11578-105">ByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="11578-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11578-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="11578-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11578-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="11578-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11578-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="11578-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11578-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="11578-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11578-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="11578-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11578-111">설명</span><span class="sxs-lookup"><span data-stu-id="11578-111">DESCRIPTION</span></span>
<span data-ttu-id="11578-112">-Reimage 매개 변수를 사용하여 노드 형식 리소스 속성을 설정하거나 노드 형식의 특정 ndes에서 다시IMAGE 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="11578-113">재이미징 작업 시 서비스 패브릭 노드는 vm을 다시미징하기 전에 비활성화되어 다시 돌아오면 다시 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="11578-114">주 노드 유형에서 이 작업을 수행하면 모든 노드를 동시에 다시IMAGE하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11578-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="11578-115">서비스 패브릭이 노드를 비활성화할 수 없지만 상태 저장 워크로드가 노드에서 실행되는 경우 데이터 손실이 발생할 수 있는 경우에도 -ForceReimage를 사용하여 작업을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="11578-116">예제</span><span class="sxs-lookup"><span data-stu-id="11578-116">EXAMPLES</span></span>

### <span data-ttu-id="11578-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="11578-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="11578-118">노드 유형의 인스턴스 수를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="11578-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="11578-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="11578-120">노드 유형의 배치 적절한 위치를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-120">Update placement properites of the node type.</span></span> <span data-ttu-id="11578-121">이렇게 하면 이전 배치 적절한 위치(있는 경우)를 덮어옵니다.</span><span class="sxs-lookup"><span data-stu-id="11578-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="11578-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="11578-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="11578-123">노드 형식에서 노드 0과 3을 다시IMAGE합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="11578-124">예제 4</span><span class="sxs-lookup"><span data-stu-id="11578-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="11578-125">파이핑을 통해 노드 유형의 인스턴스 수를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="11578-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11578-126">PARAMETERS</span></span>

### <span data-ttu-id="11578-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="11578-127">-ApplicationEndPort</span></span>
<span data-ttu-id="11578-128">포트 범위의 애플리케이션 끝 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="11578-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="11578-129">-ApplicationStartPort</span></span>
<span data-ttu-id="11578-130">포트 범위의 애플리케이션 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="11578-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11578-131">-AsJob</span></span>
<span data-ttu-id="11578-132">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="11578-133">-Capacity</span><span class="sxs-lookup"><span data-stu-id="11578-133">-Capacity</span></span>
<span data-ttu-id="11578-134">노드 형식의 노드에 적용된 용량 태그는 키/값 쌍으로, 클러스터 리소스 관리자는 이러한 태그를 사용하여 노드에 있는 리소스의 양을 이해합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="11578-135">이를 업데이트하면 현재 값이 다시 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="11578-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11578-136">-ClusterName</span></span>
<span data-ttu-id="11578-137">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11578-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11578-138">-DefaultProfile</span></span>
<span data-ttu-id="11578-139">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11578-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11578-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="11578-140">-EphemeralEndPort</span></span>
<span data-ttu-id="11578-141">포트 범위의 사용 후 사용 후 종료 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="11578-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="11578-142">-EphemeralStartPort</span></span>
<span data-ttu-id="11578-143">포트 범위의 사용 후 사용 후 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="11578-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="11578-144">-ForceReimage</span></span>
<span data-ttu-id="11578-145">서비스 패브릭이 노드를 사용하지 않도록 설정할 수 없는 경우에도 이 플래그를 사용하여 제거를 강제합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="11578-146">상태 저장 워크로드가 노드에서 실행되는 경우 데이터 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11578-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11578-147">-InputObject</span></span>
<span data-ttu-id="11578-148">노드 유형 리소스</span><span class="sxs-lookup"><span data-stu-id="11578-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11578-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="11578-149">-InstanceCount</span></span>
<span data-ttu-id="11578-150">노드 형식의 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="11578-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-151">-Name</span><span class="sxs-lookup"><span data-stu-id="11578-151">-Name</span></span>
<span data-ttu-id="11578-152">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11578-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="11578-153">-NodeName</span></span>
<span data-ttu-id="11578-154">작업에 대한 노드 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="11578-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11578-155">-PassThru</span></span>
<span data-ttu-id="11578-156">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="11578-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="11578-157">-PlacementProperty</span></span>
<span data-ttu-id="11578-158">노드 형식의 노드에 키/값 쌍으로 적용된 배치 태그는 특정 서비스(워크로드)를 실행할 위치를 나타내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11578-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="11578-159">이를 업데이트하면 현재 값이 다시 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="11578-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-160">-Image</span><span class="sxs-lookup"><span data-stu-id="11578-160">-Reimage</span></span>
<span data-ttu-id="11578-161">노드 형식에서 노드를 다시 이식할지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11578-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11578-162">-ResourceGroupName</span></span>
<span data-ttu-id="11578-163">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11578-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11578-164">-ResourceId</span></span>
<span data-ttu-id="11578-165">노드 유형 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="11578-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11578-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11578-166">-Confirm</span></span>
<span data-ttu-id="11578-167">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="11578-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11578-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11578-168">-WhatIf</span></span>
<span data-ttu-id="11578-169">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="11578-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11578-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11578-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11578-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11578-171">CommonParameters</span></span>
<span data-ttu-id="11578-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11578-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11578-173">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11578-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11578-174">입력</span><span class="sxs-lookup"><span data-stu-id="11578-174">INPUTS</span></span>

### <span data-ttu-id="11578-175">System.String</span><span class="sxs-lookup"><span data-stu-id="11578-175">System.String</span></span>

## <span data-ttu-id="11578-176">출력</span><span class="sxs-lookup"><span data-stu-id="11578-176">OUTPUTS</span></span>

### <span data-ttu-id="11578-177">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11578-177">System.Boolean</span></span>

## <span data-ttu-id="11578-178">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11578-178">NOTES</span></span>

## <span data-ttu-id="11578-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11578-179">RELATED LINKS</span></span>
