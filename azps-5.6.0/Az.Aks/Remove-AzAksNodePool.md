---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 27de96fccf2c420bd15e4a7522fecc16fd3032fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993104"
---
# <span data-ttu-id="6d216-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="6d216-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="6d216-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d216-102">SYNOPSIS</span></span>
<span data-ttu-id="6d216-103">관리되는 클러스터에서 노드 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="6d216-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d216-104">SYNTAX</span></span>

### <span data-ttu-id="6d216-105">GroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6d216-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d216-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d216-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d216-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d216-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d216-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d216-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d216-109">설명</span><span class="sxs-lookup"><span data-stu-id="6d216-109">DESCRIPTION</span></span>
<span data-ttu-id="6d216-110">관리되는 클러스터에서 노드 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="6d216-111">예제</span><span class="sxs-lookup"><span data-stu-id="6d216-111">EXAMPLES</span></span>

### <span data-ttu-id="6d216-112">지정된 노드 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="6d216-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="6d216-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6d216-113">PARAMETERS</span></span>

### <span data-ttu-id="6d216-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d216-114">-AsJob</span></span>
<span data-ttu-id="6d216-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6d216-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d216-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6d216-116">-ClusterName</span></span>
<span data-ttu-id="6d216-117">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="6d216-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d216-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="6d216-118">-ClusterObject</span></span>
<span data-ttu-id="6d216-119">클러스터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-119">The cluster object.</span></span>

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

### <span data-ttu-id="6d216-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d216-120">-DefaultProfile</span></span>
<span data-ttu-id="6d216-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d216-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6d216-122">-Force</span></span>
<span data-ttu-id="6d216-123">프롬프트 없이 노드 풀 제거</span><span class="sxs-lookup"><span data-stu-id="6d216-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="6d216-124">-Id</span><span class="sxs-lookup"><span data-stu-id="6d216-124">-Id</span></span>
<span data-ttu-id="6d216-125">관리되는 Kubernetes 클러스터의 노드 풀 ID</span><span class="sxs-lookup"><span data-stu-id="6d216-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d216-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d216-126">-InputObject</span></span>
<span data-ttu-id="6d216-127">일반적으로 파이프라인을 통해 전달되는 PSAgentPool 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="6d216-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6d216-128">-Name</span></span>
<span data-ttu-id="6d216-129">노드 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="6d216-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d216-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d216-130">-PassThru</span></span>
<span data-ttu-id="6d216-131">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="6d216-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6d216-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d216-132">-ResourceGroupName</span></span>
<span data-ttu-id="6d216-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6d216-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d216-134">-확인</span><span class="sxs-lookup"><span data-stu-id="6d216-134">-Confirm</span></span>
<span data-ttu-id="6d216-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d216-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d216-136">-WhatIf</span></span>
<span data-ttu-id="6d216-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d216-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d216-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d216-139">CommonParameters</span></span>
<span data-ttu-id="6d216-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d216-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d216-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d216-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d216-142">입력</span><span class="sxs-lookup"><span data-stu-id="6d216-142">INPUTS</span></span>

### <span data-ttu-id="6d216-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="6d216-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="6d216-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6d216-144">System.String</span></span>

## <span data-ttu-id="6d216-145">출력</span><span class="sxs-lookup"><span data-stu-id="6d216-145">OUTPUTS</span></span>

### <span data-ttu-id="6d216-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d216-146">System.Boolean</span></span>

## <span data-ttu-id="6d216-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d216-147">NOTES</span></span>

## <span data-ttu-id="6d216-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d216-148">RELATED LINKS</span></span>
