---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204148"
---
# <span data-ttu-id="4fa60-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="4fa60-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="4fa60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fa60-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa60-103">지정 된 클러스터에서 새 노드 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="4fa60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fa60-104">SYNTAX</span></span>

### <span data-ttu-id="4fa60-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fa60-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fa60-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fa60-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fa60-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4fa60-107">DESCRIPTION</span></span>
<span data-ttu-id="4fa60-108">지정 된 클러스터에서 새 노드 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="4fa60-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4fa60-109">EXAMPLES</span></span>

### <span data-ttu-id="4fa60-110">기본 매개 변수를 사용 하 여 노드 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="4fa60-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="4fa60-111">AKS에서 Windows Server 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="4fa60-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="4fa60-112">변수</span><span class="sxs-lookup"><span data-stu-id="4fa60-112">PARAMETERS</span></span>

### <span data-ttu-id="4fa60-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4fa60-113">-ClusterName</span></span>
<span data-ttu-id="4fa60-114">관리 되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="4fa60-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="4fa60-115">-ClusterObject</span></span>
<span data-ttu-id="4fa60-116">노드 풀을 만들 클러스터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="4fa60-117">-카운트</span><span class="sxs-lookup"><span data-stu-id="4fa60-117">-Count</span></span>
<span data-ttu-id="4fa60-118">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="4fa60-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa60-119">-DefaultProfile</span></span>
<span data-ttu-id="4fa60-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fa60-121">-EnableAutoScaling 크기 조정을</span><span class="sxs-lookup"><span data-stu-id="4fa60-121">-EnableAutoScaling</span></span>
<span data-ttu-id="4fa60-122">자동 scaler 설정 여부</span><span class="sxs-lookup"><span data-stu-id="4fa60-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="4fa60-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4fa60-123">-Force</span></span>
<span data-ttu-id="4fa60-124">노드 풀이 이미 있는 경우에도이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="4fa60-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="4fa60-125">-KubernetesVersion</span></span>
<span data-ttu-id="4fa60-126">클러스터를 만드는 데 사용할 Kubernetes의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="4fa60-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4fa60-127">-MaxCount</span></span>
<span data-ttu-id="4fa60-128">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="4fa60-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="4fa60-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="4fa60-129">-MaxPodCount</span></span>
<span data-ttu-id="4fa60-130">노드에서 실행할 수 있는 최대 pods 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="4fa60-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="4fa60-131">-MinCount</span></span>
<span data-ttu-id="4fa60-132">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="4fa60-133">-이름</span><span class="sxs-lookup"><span data-stu-id="4fa60-133">-Name</span></span>
<span data-ttu-id="4fa60-134">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="4fa60-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="4fa60-135">-OsDiskSize</span></span>
<span data-ttu-id="4fa60-136">노드 풀의 기본 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="4fa60-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="4fa60-137">-OsType</span></span>
<span data-ttu-id="4fa60-138">Os 종류를 지정 하는 데 사용 되는 OsType.</span><span class="sxs-lookup"><span data-stu-id="4fa60-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="4fa60-139">Linux 및 Windows에서 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="4fa60-140">Linux를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-140">Default to Linux.</span></span>

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

### <span data-ttu-id="4fa60-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa60-141">-ResourceGroupName</span></span>
<span data-ttu-id="4fa60-142">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="4fa60-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="4fa60-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="4fa60-144">낮은 우선 순위의 가상 머신 확장 집합에 대 한 제거 정책을 지정 하는 데 사용 되는 ScaleSetEvictionPolicy.</span><span class="sxs-lookup"><span data-stu-id="4fa60-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="4fa60-145">기본적으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-145">Default to Delete.</span></span>

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

### <span data-ttu-id="4fa60-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="4fa60-146">-ScaleSetPriority</span></span>
<span data-ttu-id="4fa60-147">가상 컴퓨터 크기 집합 우선 순위를 지정 하는 데 사용 되는 ScaleSetPriority.</span><span class="sxs-lookup"><span data-stu-id="4fa60-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="4fa60-148">기본값을 일반으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-148">Default to regular.</span></span>

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

### <span data-ttu-id="4fa60-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="4fa60-149">-VmSetType</span></span>
<span data-ttu-id="4fa60-150">노드 풀의 유형을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-150">Represents types of an node pool.</span></span>
<span data-ttu-id="4fa60-151">사용할 수 있는 값은 다음과 같습니다. ' VirtualMachineScaleSets ', ' AvailabilitySet '</span><span class="sxs-lookup"><span data-stu-id="4fa60-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="4fa60-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="4fa60-152">-VmSize</span></span>
<span data-ttu-id="4fa60-153">가상 컴퓨터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="4fa60-154">기본값은 Standard_D2_v2입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="4fa60-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="4fa60-155">-VnetSubnetID</span></span>
<span data-ttu-id="4fa60-156">VNet SubnetID VNet의 서브넷 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="4fa60-157">-확인</span><span class="sxs-lookup"><span data-stu-id="4fa60-157">-Confirm</span></span>
<span data-ttu-id="4fa60-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fa60-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fa60-159">-WhatIf</span></span>
<span data-ttu-id="4fa60-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fa60-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fa60-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa60-162">CommonParameters</span></span>
<span data-ttu-id="4fa60-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa60-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa60-164">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4fa60-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa60-165">입력</span><span class="sxs-lookup"><span data-stu-id="4fa60-165">INPUTS</span></span>

### <span data-ttu-id="4fa60-166">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="4fa60-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="4fa60-167">출력</span><span class="sxs-lookup"><span data-stu-id="4fa60-167">OUTPUTS</span></span>

### <span data-ttu-id="4fa60-168">Aks. PSNodePool 풀</span><span class="sxs-lookup"><span data-stu-id="4fa60-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="4fa60-169">상속자</span><span class="sxs-lookup"><span data-stu-id="4fa60-169">NOTES</span></span>

## <span data-ttu-id="4fa60-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fa60-170">RELATED LINKS</span></span>
