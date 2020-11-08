---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213304"
---
# <span data-ttu-id="1cd48-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1cd48-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="1cd48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cd48-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd48-103">-이미지로 매개 변수를 사용 하 여 노드 형식의 특정 ndes에 대해 노드 형식 리소스 속성을 설정 하거나 이미지로 된 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="1cd48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1cd48-104">SYNTAX</span></span>

### <span data-ttu-id="1cd48-105">ByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="1cd48-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cd48-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="1cd48-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cd48-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="1cd48-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cd48-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="1cd48-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cd48-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="1cd48-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cd48-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="1cd48-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1cd48-111">설명은</span><span class="sxs-lookup"><span data-stu-id="1cd48-111">DESCRIPTION</span></span>
<span data-ttu-id="1cd48-112">-이미지로 매개 변수를 사용 하 여 노드 형식의 특정 ndes에 대해 노드 형식 리소스 속성을 설정 하거나 이미지로 된 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="1cd48-113">Reimgae 작업에서 vm을 reimaging 후 다시 사용할 수 있도록 설정 하기 전에 service fabric 노드가 사용 되지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="1cd48-114">기본 노드 형식에서 이러한 작업을 수행 하는 경우에는 모든 노드를 동시에 모두 이미지로 만들지 못할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="1cd48-115">Use-ForceReimage는 서비스 패브릭이 노드를 사용 하지 않도록 설정할 수 없지만,이로 인해 노드에서 상태 저장 작업이 실행 되는 경우 데이터가 손실 될 수 있으므로 주의 해 서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="1cd48-116">예제의</span><span class="sxs-lookup"><span data-stu-id="1cd48-116">EXAMPLES</span></span>

### <span data-ttu-id="1cd48-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="1cd48-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="1cd48-118">노드 형식의 인스턴스 수를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="1cd48-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="1cd48-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="1cd48-120">노드 형식의 배치 properites를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-120">Update placement properites of the node type.</span></span> <span data-ttu-id="1cd48-121">이렇게 하면 이전 배치 properites (있는 경우)가 덮어쓰여집니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="1cd48-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="1cd48-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="1cd48-123">노드 형식에 노드 0 및 3을 이미지로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="1cd48-124">예제 4</span><span class="sxs-lookup"><span data-stu-id="1cd48-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="1cd48-125">파이프를 사용 하 여 노드 형식의 인스턴스 수를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="1cd48-126">변수</span><span class="sxs-lookup"><span data-stu-id="1cd48-126">PARAMETERS</span></span>

### <span data-ttu-id="1cd48-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="1cd48-127">-ApplicationEndPort</span></span>
<span data-ttu-id="1cd48-128">포트 범위의 응용 프로그램 끝 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-128">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="1cd48-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="1cd48-129">-ApplicationStartPort</span></span>
<span data-ttu-id="1cd48-130">포트 범위의 응용 프로그램 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-130">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="1cd48-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cd48-131">-AsJob</span></span>
<span data-ttu-id="1cd48-132">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1cd48-133">용량</span><span class="sxs-lookup"><span data-stu-id="1cd48-133">-Capacity</span></span>
<span data-ttu-id="1cd48-134">노드 형식의 노드에 적용 된 용량 태그는 키/값 쌍으로, 클러스터 리소스 관리자는 이러한 태그를 사용 하 여 노드의 리소스 크기를 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="1cd48-135">업데이트 하면 현재 값이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-135">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="1cd48-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1cd48-136">-ClusterName</span></span>
<span data-ttu-id="1cd48-137">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-137">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1cd48-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd48-138">-DefaultProfile</span></span>
<span data-ttu-id="1cd48-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cd48-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="1cd48-140">-EphemeralEndPort</span></span>
<span data-ttu-id="1cd48-141">포트 범위의 임시 끝 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-141">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="1cd48-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="1cd48-142">-EphemeralStartPort</span></span>
<span data-ttu-id="1cd48-143">포트 범위의 임시 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-143">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="1cd48-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="1cd48-144">-ForceReimage</span></span>
<span data-ttu-id="1cd48-145">이 플래그를 사용 하면 서비스 패브릭이 노드를 사용 하지 않도록 설정할 수 없는 경우에도 강제로 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="1cd48-146">노드에서 상태 저장 작업을 실행 하는 경우 데이터 손실이 발생할 수 있으므로 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

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

### <span data-ttu-id="1cd48-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cd48-147">-InputObject</span></span>
<span data-ttu-id="1cd48-148">노드 형식 리소스</span><span class="sxs-lookup"><span data-stu-id="1cd48-148">Node type resource</span></span>

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

### <span data-ttu-id="1cd48-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="1cd48-149">-InstanceCount</span></span>
<span data-ttu-id="1cd48-150">노드 형식의 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-150">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="1cd48-151">-이름</span><span class="sxs-lookup"><span data-stu-id="1cd48-151">-Name</span></span>
<span data-ttu-id="1cd48-152">노드 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-152">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="1cd48-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="1cd48-153">-NodeName</span></span>
<span data-ttu-id="1cd48-154">작업의 노드 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-154">List of node names for the operation.</span></span>

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

### <span data-ttu-id="1cd48-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cd48-155">-PassThru</span></span>
<span data-ttu-id="1cd48-156">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="1cd48-156">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="1cd48-157">-배치 속성</span><span class="sxs-lookup"><span data-stu-id="1cd48-157">-PlacementProperty</span></span>
<span data-ttu-id="1cd48-158">노드 형식의 노드에 적용 되는 배치 태그로, 키/값 쌍으로 특정 서비스 (작업 부하)가 실행 되는 위치를 나타내는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="1cd48-159">업데이트 하면 현재 값이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-159">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="1cd48-160">-이미지로</span><span class="sxs-lookup"><span data-stu-id="1cd48-160">-Reimage</span></span>
<span data-ttu-id="1cd48-161">노드 형식에 맞게 노드를 이미지로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-161">Specify to reimage nodes on the node type.</span></span>

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

### <span data-ttu-id="1cd48-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cd48-162">-ResourceGroupName</span></span>
<span data-ttu-id="1cd48-163">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1cd48-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cd48-164">-ResourceId</span></span>
<span data-ttu-id="1cd48-165">노드 형식 리소스 id</span><span class="sxs-lookup"><span data-stu-id="1cd48-165">Node type resource id</span></span>

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

### <span data-ttu-id="1cd48-166">-확인</span><span class="sxs-lookup"><span data-stu-id="1cd48-166">-Confirm</span></span>
<span data-ttu-id="1cd48-167">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cd48-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cd48-168">-WhatIf</span></span>
<span data-ttu-id="1cd48-169">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cd48-170">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cd48-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd48-171">CommonParameters</span></span>
<span data-ttu-id="1cd48-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd48-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd48-173">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1cd48-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd48-174">입력</span><span class="sxs-lookup"><span data-stu-id="1cd48-174">INPUTS</span></span>

### <span data-ttu-id="1cd48-175">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1cd48-175">System.String</span></span>

## <span data-ttu-id="1cd48-176">출력</span><span class="sxs-lookup"><span data-stu-id="1cd48-176">OUTPUTS</span></span>

### <span data-ttu-id="1cd48-177">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1cd48-177">System.Boolean</span></span>

## <span data-ttu-id="1cd48-178">상속자</span><span class="sxs-lookup"><span data-stu-id="1cd48-178">NOTES</span></span>

## <span data-ttu-id="1cd48-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cd48-179">RELATED LINKS</span></span>
