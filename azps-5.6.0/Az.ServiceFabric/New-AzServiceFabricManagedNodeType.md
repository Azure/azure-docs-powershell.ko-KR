---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 065885f4ae8f6d2ac51cb87cb0e697f4f22245f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995890"
---
# <span data-ttu-id="cc82f-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="cc82f-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="cc82f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc82f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc82f-103">새 노드 형식 리소스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-103">Create new node type resource.</span></span>

## <span data-ttu-id="cc82f-104">구문</span><span class="sxs-lookup"><span data-stu-id="cc82f-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc82f-105">설명</span><span class="sxs-lookup"><span data-stu-id="cc82f-105">DESCRIPTION</span></span>
<span data-ttu-id="cc82f-106">특정 클러스터에 대한 새 노드 형식 리소스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="cc82f-107">예제</span><span class="sxs-lookup"><span data-stu-id="cc82f-107">EXAMPLES</span></span>

### <span data-ttu-id="cc82f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc82f-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="cc82f-109">3개 노드를 사용하여 기본 노드 유형을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="cc82f-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="cc82f-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="cc82f-111">5개 노드를 사용하여 기본 노드 유형을 만들고 배치 속성, 용량, 애플리케이션 및 에메랄 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="cc82f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cc82f-112">PARAMETERS</span></span>

### <span data-ttu-id="cc82f-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="cc82f-113">-ApplicationEndPort</span></span>
<span data-ttu-id="cc82f-114">범위의 포트의 애플리케이션 엔드 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="cc82f-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="cc82f-115">-ApplicationStartPort</span></span>
<span data-ttu-id="cc82f-116">다양한 포트의 애플리케이션 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="cc82f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc82f-117">-AsJob</span></span>
<span data-ttu-id="cc82f-118">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cc82f-119">-Capacity</span><span class="sxs-lookup"><span data-stu-id="cc82f-119">-Capacity</span></span>
<span data-ttu-id="cc82f-120">노드 형식의 노드에 키/값 쌍으로 적용된 용량 태그는 클러스터 리소스 관리자가 이러한 태그를 사용하여 노드의 리소스 양을 이해합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="cc82f-121">이 업데이트를 업데이트하면 현재 값이 다시 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="cc82f-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cc82f-122">-ClusterName</span></span>
<span data-ttu-id="cc82f-123">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cc82f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc82f-124">-DefaultProfile</span></span>
<span data-ttu-id="cc82f-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc82f-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="cc82f-126">-DiskSize</span></span>
<span data-ttu-id="cc82f-127">GB의 노드 형식의 각 vm에 대한 디스크 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="cc82f-128">기본값 100입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-128">Default 100.</span></span>

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

### <span data-ttu-id="cc82f-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="cc82f-129">-EphemeralEndPort</span></span>
<span data-ttu-id="cc82f-130">범위의 포트의 에메랄 엔드 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="cc82f-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="cc82f-131">-EphemeralStartPort</span></span>
<span data-ttu-id="cc82f-132">범위의 포트의 에메리트 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="cc82f-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="cc82f-133">-InstanceCount</span></span>
<span data-ttu-id="cc82f-134">노드 형식의 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-134">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="cc82f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cc82f-135">-Name</span></span>
<span data-ttu-id="cc82f-136">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="cc82f-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="cc82f-137">-PlacementProperty</span></span>
<span data-ttu-id="cc82f-138">노드 형식의 노드에 키/값 쌍으로 적용된 배치 태그는 특정 서비스(워크로드)를 실행해야 하는 위치를 나타내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="cc82f-139">이 업데이트를 업데이트하면 현재 값이 다시 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="cc82f-140">-Primary</span><span class="sxs-lookup"><span data-stu-id="cc82f-140">-Primary</span></span>
<span data-ttu-id="cc82f-141">노드 형식이 기본인지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="cc82f-142">이 노드 형식에서 시스템 서비스를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-142">On this node type will run system services.</span></span>
<span data-ttu-id="cc82f-143">하나의 노드 유형만 기본으로 표시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="cc82f-144">기본 노드 형식은 기존 클러스터에 대해 삭제하거나 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="cc82f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc82f-145">-ResourceGroupName</span></span>
<span data-ttu-id="cc82f-146">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="cc82f-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="cc82f-147">-VmImageOffer</span></span>
<span data-ttu-id="cc82f-148">Azure Virtual Machines Marketplace 이미지의 제품 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="cc82f-149">기본값: WindowsServer입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-149">Default: WindowsServer.</span></span>

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

### <span data-ttu-id="cc82f-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="cc82f-150">-VmImagePublisher</span></span>
<span data-ttu-id="cc82f-151">Azure Virtual Machines Marketplace 이미지의 게시자입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="cc82f-152">기본값: MicrosoftWindowsServer입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-152">Default: MicrosoftWindowsServer.</span></span>

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

### <span data-ttu-id="cc82f-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="cc82f-153">-VmImageSku</span></span>
<span data-ttu-id="cc82f-154">Azure Virtual Machines Marketplace 이미지의 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="cc82f-155">기본값: 2019-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="cc82f-155">Default: 2019-Datacenter.</span></span>

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

### <span data-ttu-id="cc82f-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="cc82f-156">-VmImageVersion</span></span>
<span data-ttu-id="cc82f-157">Azure Virtual Machines Marketplace 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="cc82f-158">기본값: 최신입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-158">Default: latest.</span></span>

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

### <span data-ttu-id="cc82f-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="cc82f-159">-VmSize</span></span>
<span data-ttu-id="cc82f-160">풀의 가상 머신의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="cc82f-161">풀의 모든 가상 머신은 크기가 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="cc82f-162">기본값: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="cc82f-162">Default: Standard_D2.</span></span>

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

### <span data-ttu-id="cc82f-163">-확인</span><span class="sxs-lookup"><span data-stu-id="cc82f-163">-Confirm</span></span>
<span data-ttu-id="cc82f-164">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc82f-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc82f-165">-WhatIf</span></span>
<span data-ttu-id="cc82f-166">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc82f-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc82f-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc82f-168">CommonParameters</span></span>
<span data-ttu-id="cc82f-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cc82f-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc82f-170">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc82f-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc82f-171">입력</span><span class="sxs-lookup"><span data-stu-id="cc82f-171">INPUTS</span></span>

### <span data-ttu-id="cc82f-172">System.String</span><span class="sxs-lookup"><span data-stu-id="cc82f-172">System.String</span></span>

## <span data-ttu-id="cc82f-173">출력</span><span class="sxs-lookup"><span data-stu-id="cc82f-173">OUTPUTS</span></span>

### <span data-ttu-id="cc82f-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="cc82f-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="cc82f-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cc82f-175">NOTES</span></span>

## <span data-ttu-id="cc82f-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc82f-176">RELATED LINKS</span></span>
