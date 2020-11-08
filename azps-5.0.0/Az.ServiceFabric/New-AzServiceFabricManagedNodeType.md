---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216537"
---
# <span data-ttu-id="11739-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="11739-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="11739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11739-102">SYNOPSIS</span></span>
<span data-ttu-id="11739-103">새 노드 형식 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11739-103">Create new node type resource.</span></span>

## <span data-ttu-id="11739-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11739-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11739-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11739-105">DESCRIPTION</span></span>
<span data-ttu-id="11739-106">특정 클러스터에 대 한 새 노드 형식 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11739-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="11739-107">예제의</span><span class="sxs-lookup"><span data-stu-id="11739-107">EXAMPLES</span></span>

### <span data-ttu-id="11739-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="11739-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="11739-109">노드가 3 개 있는 기본 노드 유형을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11739-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="11739-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="11739-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="11739-111">노드 5 개를 사용 하 여 기본 노드 유형을 만들고 배치 속성, 용량, 응용 프로그램 및 임시 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="11739-112">변수</span><span class="sxs-lookup"><span data-stu-id="11739-112">PARAMETERS</span></span>

### <span data-ttu-id="11739-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="11739-113">-ApplicationEndPort</span></span>
<span data-ttu-id="11739-114">포트 범위의 응용 프로그램 끝 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="11739-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="11739-115">-ApplicationStartPort</span></span>
<span data-ttu-id="11739-116">포트 범위의 응용 프로그램 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="11739-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11739-117">-AsJob</span></span>
<span data-ttu-id="11739-118">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="11739-119">용량</span><span class="sxs-lookup"><span data-stu-id="11739-119">-Capacity</span></span>
<span data-ttu-id="11739-120">노드 형식의 노드에 적용 된 용량 태그는 키/값 쌍으로, 클러스터 리소스 관리자는 이러한 태그를 사용 하 여 노드의 리소스 크기를 파악 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="11739-121">업데이트 하면 현재 값이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11739-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="11739-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11739-122">-ClusterName</span></span>
<span data-ttu-id="11739-123">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="11739-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11739-124">-DefaultProfile</span></span>
<span data-ttu-id="11739-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11739-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="11739-126">-DiskSize</span></span>
<span data-ttu-id="11739-127">GBs의 노드 형식에서 각 vm에 대 한 디스크 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="11739-128">기본 100.</span><span class="sxs-lookup"><span data-stu-id="11739-128">Default 100.</span></span>

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

### <span data-ttu-id="11739-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="11739-129">-EphemeralEndPort</span></span>
<span data-ttu-id="11739-130">포트 범위의 임시 끝 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="11739-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="11739-131">-EphemeralStartPort</span></span>
<span data-ttu-id="11739-132">포트 범위의 임시 시작 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="11739-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="11739-133">-InstanceCount</span></span>
<span data-ttu-id="11739-134">노드 형식의 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-134">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="11739-135">-이름</span><span class="sxs-lookup"><span data-stu-id="11739-135">-Name</span></span>
<span data-ttu-id="11739-136">노드 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="11739-137">-배치 속성</span><span class="sxs-lookup"><span data-stu-id="11739-137">-PlacementProperty</span></span>
<span data-ttu-id="11739-138">노드 형식의 노드에 적용 되는 배치 태그로, 키/값 쌍으로 특정 서비스 (작업 부하)가 실행 되는 위치를 나타내는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11739-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="11739-139">업데이트 하면 현재 값이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11739-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="11739-140">-기본</span><span class="sxs-lookup"><span data-stu-id="11739-140">-Primary</span></span>
<span data-ttu-id="11739-141">노드 형식이 기본 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="11739-142">이 노드 형식에서는 시스템 서비스를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-142">On this node type will run system services.</span></span>
<span data-ttu-id="11739-143">하나의 노드 유형을 기본으로 표시 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="11739-144">기본 노드 유형을 삭제 하거나 기존 클러스터에 대해 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="11739-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="11739-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11739-145">-ResourceGroupName</span></span>
<span data-ttu-id="11739-146">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="11739-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="11739-147">-VmImageOffer</span></span>
<span data-ttu-id="11739-148">Azure 가상 컴퓨터 마켓플레이스 이미지의 제안 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="11739-149">Default: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="11739-149">Default: WindowsServer.</span></span>

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

### <span data-ttu-id="11739-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="11739-150">-VmImagePublisher</span></span>
<span data-ttu-id="11739-151">Azure 가상 컴퓨터 마켓플레이스 이미지의 게시자입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="11739-152">기본값: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="11739-152">Default: MicrosoftWindowsServer.</span></span>

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

### <span data-ttu-id="11739-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="11739-153">-VmImageSku</span></span>
<span data-ttu-id="11739-154">Azure 가상 컴퓨터 마켓플레이스 이미지의 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="11739-155">기본값: 2019-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="11739-155">Default: 2019-Datacenter.</span></span>

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

### <span data-ttu-id="11739-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="11739-156">-VmImageVersion</span></span>
<span data-ttu-id="11739-157">Azure Virtual Machines 마켓플레이스 이미지의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="11739-158">기본값: 최근.</span><span class="sxs-lookup"><span data-stu-id="11739-158">Default: latest.</span></span>

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

### <span data-ttu-id="11739-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="11739-159">-VmSize</span></span>
<span data-ttu-id="11739-160">풀의 가상 컴퓨터 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="11739-161">풀의 모든 가상 머신은 같은 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="11739-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="11739-162">기본값: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="11739-162">Default: Standard_D2.</span></span>

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

### <span data-ttu-id="11739-163">-확인</span><span class="sxs-lookup"><span data-stu-id="11739-163">-Confirm</span></span>
<span data-ttu-id="11739-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11739-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11739-165">-WhatIf</span></span>
<span data-ttu-id="11739-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11739-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11739-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11739-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11739-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11739-168">CommonParameters</span></span>
<span data-ttu-id="11739-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11739-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11739-170">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11739-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11739-171">입력</span><span class="sxs-lookup"><span data-stu-id="11739-171">INPUTS</span></span>

### <span data-ttu-id="11739-172">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11739-172">System.String</span></span>

## <span data-ttu-id="11739-173">출력</span><span class="sxs-lookup"><span data-stu-id="11739-173">OUTPUTS</span></span>

### <span data-ttu-id="11739-174">ServiceFabric. a i m.</span><span class="sxs-lookup"><span data-stu-id="11739-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="11739-175">상속자</span><span class="sxs-lookup"><span data-stu-id="11739-175">NOTES</span></span>

## <span data-ttu-id="11739-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11739-176">RELATED LINKS</span></span>
