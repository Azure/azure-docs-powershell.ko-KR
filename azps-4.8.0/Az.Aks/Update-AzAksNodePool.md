---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204142"
---
# <span data-ttu-id="86860-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="86860-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="86860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86860-102">SYNOPSIS</span></span>
<span data-ttu-id="86860-103">관리 되는 클러스터의 노드 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86860-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="86860-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86860-104">SYNTAX</span></span>

### <span data-ttu-id="86860-105">defaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="86860-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86860-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86860-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86860-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86860-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86860-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86860-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86860-109">설명은</span><span class="sxs-lookup"><span data-stu-id="86860-109">DESCRIPTION</span></span>
<span data-ttu-id="86860-110">관리 되는 클러스터의 노드 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86860-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="86860-111">예제의</span><span class="sxs-lookup"><span data-stu-id="86860-111">EXAMPLES</span></span>

### <span data-ttu-id="86860-112">지정 된 노드 풀에 대해 minimun count를 5로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="86860-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="86860-113">변수</span><span class="sxs-lookup"><span data-stu-id="86860-113">PARAMETERS</span></span>

### <span data-ttu-id="86860-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86860-114">-AsJob</span></span>
<span data-ttu-id="86860-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="86860-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86860-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="86860-116">-ClusterName</span></span>
<span data-ttu-id="86860-117">관리 되는 클러스터 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86860-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="86860-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="86860-118">-ClusterObject</span></span>
<span data-ttu-id="86860-119">클러스터 개체</span><span class="sxs-lookup"><span data-stu-id="86860-119">The cluster object</span></span>

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

### <span data-ttu-id="86860-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86860-120">-DefaultProfile</span></span>
<span data-ttu-id="86860-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86860-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86860-122">-EnableAutoScaling 크기 조정을</span><span class="sxs-lookup"><span data-stu-id="86860-122">-EnableAutoScaling</span></span>
<span data-ttu-id="86860-123">자동 scaler 설정 여부</span><span class="sxs-lookup"><span data-stu-id="86860-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="86860-124">-Force</span><span class="sxs-lookup"><span data-stu-id="86860-124">-Force</span></span>
<span data-ttu-id="86860-125">메시지를 표시 하지 않고 노드 풀 업데이트</span><span class="sxs-lookup"><span data-stu-id="86860-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="86860-126">-Id</span><span class="sxs-lookup"><span data-stu-id="86860-126">-Id</span></span>
<span data-ttu-id="86860-127">관리 되는 Kubernetes 클러스터의 노드 풀 Id</span><span class="sxs-lookup"><span data-stu-id="86860-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="86860-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86860-128">-InputObject</span></span>
<span data-ttu-id="86860-129">일반적으로 파이프라인을 통해 전달 되는 PSAgentPool 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="86860-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="86860-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="86860-130">-KubernetesVersion</span></span>
<span data-ttu-id="86860-131">클러스터를 만드는 데 사용할 Kubernetes의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="86860-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="86860-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="86860-132">-MaxCount</span></span>
<span data-ttu-id="86860-133">자동 크기 조정을 위한 최대 노드 수</span><span class="sxs-lookup"><span data-stu-id="86860-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="86860-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="86860-134">-MinCount</span></span>
<span data-ttu-id="86860-135">자동 크기 조정을 위한 최소 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="86860-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="86860-136">-이름</span><span class="sxs-lookup"><span data-stu-id="86860-136">-Name</span></span>
<span data-ttu-id="86860-137">노드 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86860-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="86860-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86860-138">-ResourceGroupName</span></span>
<span data-ttu-id="86860-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86860-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="86860-140">-확인</span><span class="sxs-lookup"><span data-stu-id="86860-140">-Confirm</span></span>
<span data-ttu-id="86860-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="86860-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86860-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86860-142">-WhatIf</span></span>
<span data-ttu-id="86860-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="86860-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86860-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86860-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86860-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86860-145">CommonParameters</span></span>
<span data-ttu-id="86860-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86860-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86860-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="86860-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86860-148">입력</span><span class="sxs-lookup"><span data-stu-id="86860-148">INPUTS</span></span>

### <span data-ttu-id="86860-149">Aks. PSNodePool 풀</span><span class="sxs-lookup"><span data-stu-id="86860-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="86860-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="86860-150">System.String</span></span>

## <span data-ttu-id="86860-151">출력</span><span class="sxs-lookup"><span data-stu-id="86860-151">OUTPUTS</span></span>

### <span data-ttu-id="86860-152">Aks. PSNodePool 풀</span><span class="sxs-lookup"><span data-stu-id="86860-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="86860-153">상속자</span><span class="sxs-lookup"><span data-stu-id="86860-153">NOTES</span></span>

## <span data-ttu-id="86860-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86860-154">RELATED LINKS</span></span>
