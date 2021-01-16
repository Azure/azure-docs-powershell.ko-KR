---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368656"
---
# <span data-ttu-id="2205a-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2205a-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="2205a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2205a-102">SYNOPSIS</span></span>
<span data-ttu-id="2205a-103">새 노드 유형 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-103">Create new node type resource.</span></span>

## <span data-ttu-id="2205a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2205a-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2205a-105">설명</span><span class="sxs-lookup"><span data-stu-id="2205a-105">DESCRIPTION</span></span>
<span data-ttu-id="2205a-106">특정 클러스터에 대한 새 노드 유형 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="2205a-107">예제</span><span class="sxs-lookup"><span data-stu-id="2205a-107">EXAMPLES</span></span>

### <span data-ttu-id="2205a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2205a-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="2205a-109">3개 노드가 있는 주 노드 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="2205a-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="2205a-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="2205a-111">5개 노드가 있는 주 노드 유형을 만들고 배치 속성, 용량, 애플리케이션 및 사용 후 제거 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="2205a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2205a-112">PARAMETERS</span></span>

### <span data-ttu-id="2205a-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="2205a-113">-ApplicationEndPort</span></span>
<span data-ttu-id="2205a-114">포트 범위의 애플리케이션 끝 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-114">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="2205a-115">-ApplicationStartPort</span></span>
<span data-ttu-id="2205a-116">포트 범위의 애플리케이션 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-116">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2205a-117">-AsJob</span></span>
<span data-ttu-id="2205a-118">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2205a-119">-Capacity</span><span class="sxs-lookup"><span data-stu-id="2205a-119">-Capacity</span></span>
<span data-ttu-id="2205a-120">노드 형식의 노드에 적용된 용량 태그는 키/값 쌍으로, 클러스터 리소스 관리자는 이러한 태그를 사용하여 노드에 있는 리소스의 양을 이해합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="2205a-121">이를 업데이트하면 현재 값이 다시 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-121">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2205a-122">-ClusterName</span></span>
<span data-ttu-id="2205a-123">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2205a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2205a-124">-DefaultProfile</span></span>
<span data-ttu-id="2205a-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2205a-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="2205a-126">-DiskSize</span></span>
<span data-ttu-id="2205a-127">노드 형식의 각 VM에 대한 디스크 크기(BS)입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="2205a-128">기본값은 100입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-128">Default 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="2205a-129">-EphemeralEndPort</span></span>
<span data-ttu-id="2205a-130">포트 범위의 사용 후 사용 후 종료 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-130">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="2205a-131">-EphemeralStartPort</span></span>
<span data-ttu-id="2205a-132">포트 범위의 사용 후 사용 후 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-132">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="2205a-133">-InstanceCount</span></span>
<span data-ttu-id="2205a-134">노드 형식의 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-135">-Name</span><span class="sxs-lookup"><span data-stu-id="2205a-135">-Name</span></span>
<span data-ttu-id="2205a-136">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="2205a-137">-PlacementProperty</span></span>
<span data-ttu-id="2205a-138">노드 형식의 노드에 키/값 쌍으로 적용된 배치 태그는 특정 서비스(워크로드)를 실행할 위치를 나타내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="2205a-139">이를 업데이트하면 현재 값이 다시 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-139">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-140">-Primary</span><span class="sxs-lookup"><span data-stu-id="2205a-140">-Primary</span></span>
<span data-ttu-id="2205a-141">노드 형식이 기본 유형인지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="2205a-142">이 노드 유형에서 시스템 서비스를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-142">On this node type will run system services.</span></span>
<span data-ttu-id="2205a-143">하나의 노드 유형만 주 노드로 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="2205a-144">기존 클러스터에 대해 주 노드 유형을 삭제하거나 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="2205a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2205a-145">-ResourceGroupName</span></span>
<span data-ttu-id="2205a-146">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2205a-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="2205a-147">-VmImageOffer</span></span>
<span data-ttu-id="2205a-148">Azure Virtual Machines Marketplace 이미지의 제품 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="2205a-149">기본값: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="2205a-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2205a-150">-VmImagePublisher</span></span>
<span data-ttu-id="2205a-151">Azure Virtual Machines Marketplace 이미지의 게시자입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="2205a-152">기본값: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="2205a-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="2205a-153">-VmImageSku</span></span>
<span data-ttu-id="2205a-154">Azure Virtual Machines Marketplace 이미지의 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="2205a-155">기본값: 2019-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="2205a-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="2205a-156">-VmImageVersion</span></span>
<span data-ttu-id="2205a-157">Azure Virtual Machines Marketplace 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="2205a-158">기본값: latest.</span><span class="sxs-lookup"><span data-stu-id="2205a-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="2205a-159">-VmSize</span></span>
<span data-ttu-id="2205a-160">풀에 있는 가상 머신의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="2205a-161">풀의 모든 가상 머신은 동일한 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="2205a-162">기본값: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="2205a-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2205a-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2205a-163">-Confirm</span></span>
<span data-ttu-id="2205a-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2205a-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2205a-165">-WhatIf</span></span>
<span data-ttu-id="2205a-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2205a-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2205a-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2205a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2205a-168">CommonParameters</span></span>
<span data-ttu-id="2205a-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2205a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2205a-170">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2205a-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2205a-171">입력</span><span class="sxs-lookup"><span data-stu-id="2205a-171">INPUTS</span></span>

### <span data-ttu-id="2205a-172">System.String</span><span class="sxs-lookup"><span data-stu-id="2205a-172">System.String</span></span>

## <span data-ttu-id="2205a-173">출력</span><span class="sxs-lookup"><span data-stu-id="2205a-173">OUTPUTS</span></span>

### <span data-ttu-id="2205a-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2205a-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="2205a-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2205a-175">NOTES</span></span>

## <span data-ttu-id="2205a-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2205a-176">RELATED LINKS</span></span>