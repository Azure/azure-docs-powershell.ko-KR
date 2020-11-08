---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217106"
---
# <span data-ttu-id="5faa2-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="5faa2-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="5faa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5faa2-102">SYNOPSIS</span></span>
<span data-ttu-id="5faa2-103">관리 되는 클러스터에서 노드 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="5faa2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5faa2-104">SYNTAX</span></span>

### <span data-ttu-id="5faa2-105">GroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5faa2-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5faa2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5faa2-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5faa2-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5faa2-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5faa2-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5faa2-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5faa2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5faa2-109">DESCRIPTION</span></span>
<span data-ttu-id="5faa2-110">관리 되는 클러스터에서 노드 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="5faa2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5faa2-111">EXAMPLES</span></span>

### <span data-ttu-id="5faa2-112">지정 된 노드 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="5faa2-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="5faa2-113">변수</span><span class="sxs-lookup"><span data-stu-id="5faa2-113">PARAMETERS</span></span>

### <span data-ttu-id="5faa2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5faa2-114">-AsJob</span></span>
<span data-ttu-id="5faa2-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5faa2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5faa2-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5faa2-116">-ClusterName</span></span>
<span data-ttu-id="5faa2-117">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="5faa2-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5faa2-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="5faa2-118">-ClusterObject</span></span>
<span data-ttu-id="5faa2-119">클러스터 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-119">The cluster object.</span></span>

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

### <span data-ttu-id="5faa2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5faa2-120">-DefaultProfile</span></span>
<span data-ttu-id="5faa2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5faa2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5faa2-122">-Force</span></span>
<span data-ttu-id="5faa2-123">메시지를 표시 하지 않고 노드 풀 제거</span><span class="sxs-lookup"><span data-stu-id="5faa2-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="5faa2-124">-Id</span><span class="sxs-lookup"><span data-stu-id="5faa2-124">-Id</span></span>
<span data-ttu-id="5faa2-125">관리 되는 Kubernetes 클러스터의 노드 풀 Id</span><span class="sxs-lookup"><span data-stu-id="5faa2-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5faa2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5faa2-126">-InputObject</span></span>
<span data-ttu-id="5faa2-127">일반적으로 파이프라인을 통해 전달 되는 PSAgentPool 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5faa2-128">-이름</span><span class="sxs-lookup"><span data-stu-id="5faa2-128">-Name</span></span>
<span data-ttu-id="5faa2-129">노드 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="5faa2-129">Name of your node pool</span></span>

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

### <span data-ttu-id="5faa2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5faa2-130">-PassThru</span></span>
<span data-ttu-id="5faa2-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="5faa2-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="5faa2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5faa2-132">-ResourceGroupName</span></span>
<span data-ttu-id="5faa2-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5faa2-133">Resource group name</span></span>

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

### <span data-ttu-id="5faa2-134">-확인</span><span class="sxs-lookup"><span data-stu-id="5faa2-134">-Confirm</span></span>
<span data-ttu-id="5faa2-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5faa2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5faa2-136">-WhatIf</span></span>
<span data-ttu-id="5faa2-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5faa2-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5faa2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5faa2-139">CommonParameters</span></span>
<span data-ttu-id="5faa2-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5faa2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5faa2-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5faa2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5faa2-142">입력</span><span class="sxs-lookup"><span data-stu-id="5faa2-142">INPUTS</span></span>

### <span data-ttu-id="5faa2-143">Aks. PSNodePool 풀</span><span class="sxs-lookup"><span data-stu-id="5faa2-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="5faa2-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5faa2-144">System.String</span></span>

## <span data-ttu-id="5faa2-145">출력</span><span class="sxs-lookup"><span data-stu-id="5faa2-145">OUTPUTS</span></span>

### <span data-ttu-id="5faa2-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5faa2-146">System.Boolean</span></span>

## <span data-ttu-id="5faa2-147">상속자</span><span class="sxs-lookup"><span data-stu-id="5faa2-147">NOTES</span></span>

## <span data-ttu-id="5faa2-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5faa2-148">RELATED LINKS</span></span>
