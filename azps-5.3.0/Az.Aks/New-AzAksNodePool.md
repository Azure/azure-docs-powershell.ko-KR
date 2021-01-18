---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492674"
---
# <span data-ttu-id="fa235-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="fa235-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="fa235-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa235-102">SYNOPSIS</span></span>
<span data-ttu-id="fa235-103">지정된 클러스터에서 새 노드 풀을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="fa235-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa235-104">SYNTAX</span></span>

### <span data-ttu-id="fa235-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa235-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa235-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa235-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa235-107">설명</span><span class="sxs-lookup"><span data-stu-id="fa235-107">DESCRIPTION</span></span>
<span data-ttu-id="fa235-108">지정된 클러스터에서 새 노드 풀을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="fa235-109">예제</span><span class="sxs-lookup"><span data-stu-id="fa235-109">EXAMPLES</span></span>

### <span data-ttu-id="fa235-110">기본 매개 변수를 사용하여 노드 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="fa235-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="fa235-111">AKS에서 Windows Server 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="fa235-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="fa235-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa235-112">PARAMETERS</span></span>

### <span data-ttu-id="fa235-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fa235-113">-ClusterName</span></span>
<span data-ttu-id="fa235-114">관리되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="fa235-115">-ClusterObject</span></span>
<span data-ttu-id="fa235-116">노드 풀을 만들 클러스터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-117">-Count</span><span class="sxs-lookup"><span data-stu-id="fa235-117">-Count</span></span>
<span data-ttu-id="fa235-118">노드 풀에 대한 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="fa235-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa235-119">-DefaultProfile</span></span>
<span data-ttu-id="fa235-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa235-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="fa235-121">-EnableAutoScaling</span></span>
<span data-ttu-id="fa235-122">자동 크기 조정기 사용 여부</span><span class="sxs-lookup"><span data-stu-id="fa235-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="fa235-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fa235-123">-Force</span></span>
<span data-ttu-id="fa235-124">노드 풀이 이미 있는 경우에도 노드 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="fa235-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="fa235-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="fa235-125">-KubernetesVersion</span></span>
<span data-ttu-id="fa235-126">클러스터를 만드는 데 사용할 Kubernetes 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-126">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fa235-127">-MaxCount</span></span>
<span data-ttu-id="fa235-128">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="fa235-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="fa235-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="fa235-129">-MaxPodCount</span></span>
<span data-ttu-id="fa235-130">노드에서 실행할 수 있는 최대 Pod 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="fa235-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="fa235-131">-MinCount</span></span>
<span data-ttu-id="fa235-132">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="fa235-133">-Name</span><span class="sxs-lookup"><span data-stu-id="fa235-133">-Name</span></span>
<span data-ttu-id="fa235-134">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-134">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="fa235-135">-OsDiskSize</span></span>
<span data-ttu-id="fa235-136">노드 풀에 대한 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="fa235-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="fa235-137">-OsType</span></span>
<span data-ttu-id="fa235-138">os 유형을 지정하는 데 사용할 OsType입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="fa235-139">Linux 및 Windows에서 선택</span><span class="sxs-lookup"><span data-stu-id="fa235-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="fa235-140">Linux의 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-140">Default to Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa235-141">-ResourceGroupName</span></span>
<span data-ttu-id="fa235-142">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fa235-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="fa235-144">우선 순위가 낮은 가상 머신 확장 집합에 대한 지우기 정책을 지정하는 데 사용할 ScaleSetEvictionPolicy입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="fa235-145">기본값은 삭제입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-145">Default to Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="fa235-146">-ScaleSetPriority</span></span>
<span data-ttu-id="fa235-147">가상 머신 확장 집합 우선 순위를 지정하는 데 사용할 ScaleSetPriority입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="fa235-148">기본값은 일반입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-148">Default to regular.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="fa235-149">-VmSetType</span></span>
<span data-ttu-id="fa235-150">노드 풀의 형식을 나타 내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-150">Represents types of an node pool.</span></span>
<span data-ttu-id="fa235-151">가능한 값은 'VirtualMachineScaleSets', 'AvailabilitySet'입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="fa235-152">-VmSize</span></span>
<span data-ttu-id="fa235-153">Virtual Machine의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="fa235-154">기본값은 Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="fa235-154">Default value is Standard_D2_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="fa235-155">-VnetSubnetID</span></span>
<span data-ttu-id="fa235-156">VNet SubnetID는 VNet의 서브넷 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa235-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa235-157">-Confirm</span></span>
<span data-ttu-id="fa235-158">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa235-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa235-159">-WhatIf</span></span>
<span data-ttu-id="fa235-160">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fa235-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa235-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa235-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa235-162">CommonParameters</span></span>
<span data-ttu-id="fa235-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa235-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa235-164">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fa235-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa235-165">입력</span><span class="sxs-lookup"><span data-stu-id="fa235-165">INPUTS</span></span>

### <span data-ttu-id="fa235-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fa235-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="fa235-167">출력</span><span class="sxs-lookup"><span data-stu-id="fa235-167">OUTPUTS</span></span>

### <span data-ttu-id="fa235-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="fa235-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="fa235-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa235-169">NOTES</span></span>

## <span data-ttu-id="fa235-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa235-170">RELATED LINKS</span></span>
