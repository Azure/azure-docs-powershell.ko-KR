---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348854"
---
# <span data-ttu-id="6b621-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="6b621-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="6b621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b621-102">SYNOPSIS</span></span>
<span data-ttu-id="6b621-103">관리되는 클러스터에서 노드 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="6b621-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b621-104">SYNTAX</span></span>

### <span data-ttu-id="6b621-105">defaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6b621-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b621-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b621-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b621-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b621-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b621-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b621-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b621-109">설명</span><span class="sxs-lookup"><span data-stu-id="6b621-109">DESCRIPTION</span></span>
<span data-ttu-id="6b621-110">관리되는 클러스터에서 노드 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="6b621-111">예제</span><span class="sxs-lookup"><span data-stu-id="6b621-111">EXAMPLES</span></span>

### <span data-ttu-id="6b621-112">지정된 노드 풀에 대한 미니문 수를 5로 변경</span><span class="sxs-lookup"><span data-stu-id="6b621-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="6b621-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b621-113">PARAMETERS</span></span>

### <span data-ttu-id="6b621-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b621-114">-AsJob</span></span>
<span data-ttu-id="6b621-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6b621-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b621-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6b621-116">-ClusterName</span></span>
<span data-ttu-id="6b621-117">관리되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="6b621-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="6b621-118">-ClusterObject</span></span>
<span data-ttu-id="6b621-119">클러스터 개체</span><span class="sxs-lookup"><span data-stu-id="6b621-119">The cluster object</span></span>

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

### <span data-ttu-id="6b621-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b621-120">-DefaultProfile</span></span>
<span data-ttu-id="6b621-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b621-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="6b621-122">-EnableAutoScaling</span></span>
<span data-ttu-id="6b621-123">자동 크기 조정기 사용 여부</span><span class="sxs-lookup"><span data-stu-id="6b621-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="6b621-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6b621-124">-Force</span></span>
<span data-ttu-id="6b621-125">프롬프트 없이 노드 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="6b621-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="6b621-126">-Id</span><span class="sxs-lookup"><span data-stu-id="6b621-126">-Id</span></span>
<span data-ttu-id="6b621-127">관리되는 Kubernetes 클러스터의 노드 풀 ID</span><span class="sxs-lookup"><span data-stu-id="6b621-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6b621-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b621-128">-InputObject</span></span>
<span data-ttu-id="6b621-129">일반적으로 파이프라인을 통해 전달되는 PSAgentPool 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6b621-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="6b621-130">-KubernetesVersion</span></span>
<span data-ttu-id="6b621-131">클러스터를 만드는 데 사용할 Kubernetes 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="6b621-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6b621-132">-MaxCount</span></span>
<span data-ttu-id="6b621-133">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="6b621-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="6b621-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="6b621-134">-MinCount</span></span>
<span data-ttu-id="6b621-135">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="6b621-136">-Name</span><span class="sxs-lookup"><span data-stu-id="6b621-136">-Name</span></span>
<span data-ttu-id="6b621-137">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="6b621-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b621-138">-ResourceGroupName</span></span>
<span data-ttu-id="6b621-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b621-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b621-140">-Confirm</span></span>
<span data-ttu-id="6b621-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b621-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b621-142">-WhatIf</span></span>
<span data-ttu-id="6b621-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6b621-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b621-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b621-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b621-145">CommonParameters</span></span>
<span data-ttu-id="6b621-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b621-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b621-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6b621-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b621-148">입력</span><span class="sxs-lookup"><span data-stu-id="6b621-148">INPUTS</span></span>

### <span data-ttu-id="6b621-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="6b621-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="6b621-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6b621-150">System.String</span></span>

## <span data-ttu-id="6b621-151">출력</span><span class="sxs-lookup"><span data-stu-id="6b621-151">OUTPUTS</span></span>

### <span data-ttu-id="6b621-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="6b621-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="6b621-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b621-153">NOTES</span></span>

## <span data-ttu-id="6b621-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b621-154">RELATED LINKS</span></span>
