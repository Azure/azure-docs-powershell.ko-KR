---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192636"
---
# <span data-ttu-id="32935-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="32935-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="32935-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32935-102">SYNOPSIS</span></span>
<span data-ttu-id="32935-103">관리되는 클러스터에서 노드 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32935-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="32935-104">구문</span><span class="sxs-lookup"><span data-stu-id="32935-104">SYNTAX</span></span>

### <span data-ttu-id="32935-105">defaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="32935-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32935-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32935-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32935-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32935-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32935-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32935-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32935-109">설명</span><span class="sxs-lookup"><span data-stu-id="32935-109">DESCRIPTION</span></span>
<span data-ttu-id="32935-110">관리되는 클러스터에서 노드 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32935-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="32935-111">예제</span><span class="sxs-lookup"><span data-stu-id="32935-111">EXAMPLES</span></span>

### <span data-ttu-id="32935-112">지정된 노드 풀에 대한 미니문 수를 5로 변경</span><span class="sxs-lookup"><span data-stu-id="32935-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="32935-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32935-113">PARAMETERS</span></span>

### <span data-ttu-id="32935-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32935-114">-AsJob</span></span>
<span data-ttu-id="32935-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="32935-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32935-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="32935-116">-ClusterName</span></span>
<span data-ttu-id="32935-117">관리되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32935-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="32935-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="32935-118">-ClusterObject</span></span>
<span data-ttu-id="32935-119">클러스터 개체</span><span class="sxs-lookup"><span data-stu-id="32935-119">The cluster object</span></span>

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

### <span data-ttu-id="32935-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32935-120">-DefaultProfile</span></span>
<span data-ttu-id="32935-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32935-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32935-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="32935-122">-EnableAutoScaling</span></span>
<span data-ttu-id="32935-123">자동 크기 조정기 사용 여부</span><span class="sxs-lookup"><span data-stu-id="32935-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="32935-124">-Force</span><span class="sxs-lookup"><span data-stu-id="32935-124">-Force</span></span>
<span data-ttu-id="32935-125">프롬프트 없이 노드 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="32935-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="32935-126">-Id</span><span class="sxs-lookup"><span data-stu-id="32935-126">-Id</span></span>
<span data-ttu-id="32935-127">관리되는 Kubernetes 클러스터의 노드 풀 ID</span><span class="sxs-lookup"><span data-stu-id="32935-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="32935-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32935-128">-InputObject</span></span>
<span data-ttu-id="32935-129">일반적으로 파이프라인을 통해 전달되는 PSAgentPool 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="32935-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="32935-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="32935-130">-KubernetesVersion</span></span>
<span data-ttu-id="32935-131">클러스터를 만드는 데 사용할 Kubernetes 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="32935-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="32935-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="32935-132">-MaxCount</span></span>
<span data-ttu-id="32935-133">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="32935-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="32935-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="32935-134">-MinCount</span></span>
<span data-ttu-id="32935-135">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="32935-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="32935-136">-Name</span><span class="sxs-lookup"><span data-stu-id="32935-136">-Name</span></span>
<span data-ttu-id="32935-137">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32935-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="32935-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32935-138">-ResourceGroupName</span></span>
<span data-ttu-id="32935-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32935-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="32935-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32935-140">-Confirm</span></span>
<span data-ttu-id="32935-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32935-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32935-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32935-142">-WhatIf</span></span>
<span data-ttu-id="32935-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="32935-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32935-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32935-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32935-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32935-145">CommonParameters</span></span>
<span data-ttu-id="32935-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32935-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32935-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32935-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32935-148">입력</span><span class="sxs-lookup"><span data-stu-id="32935-148">INPUTS</span></span>

### <span data-ttu-id="32935-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="32935-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="32935-150">System.String</span><span class="sxs-lookup"><span data-stu-id="32935-150">System.String</span></span>

## <span data-ttu-id="32935-151">출력</span><span class="sxs-lookup"><span data-stu-id="32935-151">OUTPUTS</span></span>

### <span data-ttu-id="32935-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="32935-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="32935-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32935-153">NOTES</span></span>

## <span data-ttu-id="32935-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32935-154">RELATED LINKS</span></span>
