---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: 6f16664eac63ab2bb543b2d032679d979f3c2122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010059"
---
# <span data-ttu-id="5c1eb-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="5c1eb-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="5c1eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1eb-103">관리되는 클러스터에서 노드 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="5c1eb-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c1eb-104">SYNTAX</span></span>

### <span data-ttu-id="5c1eb-105">defaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c1eb-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1eb-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c1eb-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1eb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c1eb-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1eb-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c1eb-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c1eb-109">설명</span><span class="sxs-lookup"><span data-stu-id="5c1eb-109">DESCRIPTION</span></span>
<span data-ttu-id="5c1eb-110">관리되는 클러스터에서 노드 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="5c1eb-111">예제</span><span class="sxs-lookup"><span data-stu-id="5c1eb-111">EXAMPLES</span></span>

### <span data-ttu-id="5c1eb-112">지정된 노드 풀의 미니문 수를 5로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="5c1eb-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c1eb-113">PARAMETERS</span></span>

### <span data-ttu-id="5c1eb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c1eb-114">-AsJob</span></span>
<span data-ttu-id="5c1eb-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5c1eb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c1eb-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5c1eb-116">-ClusterName</span></span>
<span data-ttu-id="5c1eb-117">관리되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="5c1eb-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="5c1eb-118">-ClusterObject</span></span>
<span data-ttu-id="5c1eb-119">클러스터 개체</span><span class="sxs-lookup"><span data-stu-id="5c1eb-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1eb-120">-DefaultProfile</span></span>
<span data-ttu-id="5c1eb-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c1eb-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="5c1eb-122">-EnableAutoScaling</span></span>
<span data-ttu-id="5c1eb-123">자동 크기 조정기 사용 여부</span><span class="sxs-lookup"><span data-stu-id="5c1eb-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="5c1eb-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5c1eb-124">-Force</span></span>
<span data-ttu-id="5c1eb-125">프롬프트 없이 노드 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="5c1eb-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="5c1eb-126">-Id</span><span class="sxs-lookup"><span data-stu-id="5c1eb-126">-Id</span></span>
<span data-ttu-id="5c1eb-127">관리되는 Kubernetes 클러스터의 노드 풀 ID</span><span class="sxs-lookup"><span data-stu-id="5c1eb-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1eb-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c1eb-128">-InputObject</span></span>
<span data-ttu-id="5c1eb-129">일반적으로 파이프라인을 통해 전달되는 PSAgentPool 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c1eb-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="5c1eb-130">-KubernetesVersion</span></span>
<span data-ttu-id="5c1eb-131">클러스터를 만드는 데 사용할 Kubernetes 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="5c1eb-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="5c1eb-132">-MaxCount</span></span>
<span data-ttu-id="5c1eb-133">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="5c1eb-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="5c1eb-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="5c1eb-134">-MinCount</span></span>
<span data-ttu-id="5c1eb-135">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="5c1eb-136">-Name</span><span class="sxs-lookup"><span data-stu-id="5c1eb-136">-Name</span></span>
<span data-ttu-id="5c1eb-137">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1eb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1eb-138">-ResourceGroupName</span></span>
<span data-ttu-id="5c1eb-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c1eb-140">-확인</span><span class="sxs-lookup"><span data-stu-id="5c1eb-140">-Confirm</span></span>
<span data-ttu-id="5c1eb-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1eb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1eb-142">-WhatIf</span></span>
<span data-ttu-id="5c1eb-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c1eb-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1eb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1eb-145">CommonParameters</span></span>
<span data-ttu-id="5c1eb-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1eb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1eb-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c1eb-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1eb-148">입력</span><span class="sxs-lookup"><span data-stu-id="5c1eb-148">INPUTS</span></span>

### <span data-ttu-id="5c1eb-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="5c1eb-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="5c1eb-150">System.String</span><span class="sxs-lookup"><span data-stu-id="5c1eb-150">System.String</span></span>

## <span data-ttu-id="5c1eb-151">출력</span><span class="sxs-lookup"><span data-stu-id="5c1eb-151">OUTPUTS</span></span>

### <span data-ttu-id="5c1eb-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="5c1eb-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="5c1eb-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c1eb-153">NOTES</span></span>

## <span data-ttu-id="5c1eb-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c1eb-154">RELATED LINKS</span></span>
