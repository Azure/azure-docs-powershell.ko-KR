---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192652"
---
# <span data-ttu-id="38b61-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="38b61-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="38b61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38b61-102">SYNOPSIS</span></span>
<span data-ttu-id="38b61-103">관리되는 클러스터에서 노드 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="38b61-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="38b61-104">구문</span><span class="sxs-lookup"><span data-stu-id="38b61-104">SYNTAX</span></span>

### <span data-ttu-id="38b61-105">GroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="38b61-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b61-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38b61-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b61-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38b61-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b61-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38b61-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38b61-109">설명</span><span class="sxs-lookup"><span data-stu-id="38b61-109">DESCRIPTION</span></span>
<span data-ttu-id="38b61-110">관리되는 클러스터에서 노드 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="38b61-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="38b61-111">예제</span><span class="sxs-lookup"><span data-stu-id="38b61-111">EXAMPLES</span></span>

### <span data-ttu-id="38b61-112">지정된 노드 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="38b61-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="38b61-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38b61-113">PARAMETERS</span></span>

### <span data-ttu-id="38b61-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38b61-114">-AsJob</span></span>
<span data-ttu-id="38b61-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="38b61-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38b61-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="38b61-116">-ClusterName</span></span>
<span data-ttu-id="38b61-117">관리되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="38b61-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="38b61-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="38b61-118">-ClusterObject</span></span>
<span data-ttu-id="38b61-119">클러스터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="38b61-119">The cluster object.</span></span>

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

### <span data-ttu-id="38b61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b61-120">-DefaultProfile</span></span>
<span data-ttu-id="38b61-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38b61-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b61-122">-Force</span><span class="sxs-lookup"><span data-stu-id="38b61-122">-Force</span></span>
<span data-ttu-id="38b61-123">프롬프트 없이 노드 풀 제거</span><span class="sxs-lookup"><span data-stu-id="38b61-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="38b61-124">-Id</span><span class="sxs-lookup"><span data-stu-id="38b61-124">-Id</span></span>
<span data-ttu-id="38b61-125">관리되는 Kubernetes 클러스터의 노드 풀 ID</span><span class="sxs-lookup"><span data-stu-id="38b61-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="38b61-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38b61-126">-InputObject</span></span>
<span data-ttu-id="38b61-127">일반적으로 파이프라인을 통해 전달되는 PSAgentPool 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="38b61-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="38b61-128">-Name</span><span class="sxs-lookup"><span data-stu-id="38b61-128">-Name</span></span>
<span data-ttu-id="38b61-129">노드 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="38b61-129">Name of your node pool</span></span>

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

### <span data-ttu-id="38b61-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38b61-130">-PassThru</span></span>
<span data-ttu-id="38b61-131">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="38b61-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="38b61-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b61-132">-ResourceGroupName</span></span>
<span data-ttu-id="38b61-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="38b61-133">Resource group name</span></span>

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

### <span data-ttu-id="38b61-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38b61-134">-Confirm</span></span>
<span data-ttu-id="38b61-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38b61-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b61-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b61-136">-WhatIf</span></span>
<span data-ttu-id="38b61-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="38b61-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b61-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38b61-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b61-139">CommonParameters</span></span>
<span data-ttu-id="38b61-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38b61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b61-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38b61-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b61-142">입력</span><span class="sxs-lookup"><span data-stu-id="38b61-142">INPUTS</span></span>

### <span data-ttu-id="38b61-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="38b61-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="38b61-144">System.String</span><span class="sxs-lookup"><span data-stu-id="38b61-144">System.String</span></span>

## <span data-ttu-id="38b61-145">출력</span><span class="sxs-lookup"><span data-stu-id="38b61-145">OUTPUTS</span></span>

### <span data-ttu-id="38b61-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38b61-146">System.Boolean</span></span>

## <span data-ttu-id="38b61-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38b61-147">NOTES</span></span>

## <span data-ttu-id="38b61-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38b61-148">RELATED LINKS</span></span>
