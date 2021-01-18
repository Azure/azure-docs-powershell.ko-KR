---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492734"
---
# <span data-ttu-id="a3de5-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a3de5-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a3de5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3de5-102">SYNOPSIS</span></span>
<span data-ttu-id="a3de5-103">자체 호스팅 통합 런타임 노드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="a3de5-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3de5-104">SYNTAX</span></span>

### <span data-ttu-id="a3de5-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a3de5-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3de5-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3de5-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3de5-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3de5-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3de5-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3de5-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3de5-109">설명</span><span class="sxs-lookup"><span data-stu-id="a3de5-109">DESCRIPTION</span></span>
<span data-ttu-id="a3de5-110">**Update-AzSynapseIntegrationRuntimeNode** cmdlet은 작업 영역의 자체 호스팅 통합 런타임 노드 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="a3de5-111">현재는 'ConcurrentJobsLimit' 업데이트만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="a3de5-112">예제</span><span class="sxs-lookup"><span data-stu-id="a3de5-112">EXAMPLES</span></span>

### <span data-ttu-id="a3de5-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3de5-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="a3de5-114">cmdlet은 자체 호스팅 통합 런타임 'test-selfhost-ir'에서 'Node_1' 노드에 대해 'ConcurrentJobsLimit'를 3으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="a3de5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3de5-115">PARAMETERS</span></span>

### <span data-ttu-id="a3de5-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="a3de5-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="a3de5-117">통합 런타임 노드에서 실행될 수 있는 동시 작업 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="a3de5-118">1과 maxConcurrentJobs 사이의 값은 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="a3de5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3de5-119">-DefaultProfile</span></span>
<span data-ttu-id="a3de5-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3de5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3de5-121">-InputObject</span></span>
<span data-ttu-id="a3de5-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3de5-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a3de5-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a3de5-124">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3de5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a3de5-125">-Name</span></span>
<span data-ttu-id="a3de5-126">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="a3de5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3de5-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3de5-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3de5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3de5-129">-ResourceId</span></span>
<span data-ttu-id="a3de5-130">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3de5-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a3de5-131">-WorkspaceName</span></span>
<span data-ttu-id="a3de5-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3de5-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a3de5-133">-WorkspaceObject</span></span>
<span data-ttu-id="a3de5-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3de5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3de5-135">-Confirm</span></span>
<span data-ttu-id="a3de5-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3de5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3de5-137">-WhatIf</span></span>
<span data-ttu-id="a3de5-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a3de5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3de5-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3de5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3de5-140">CommonParameters</span></span>
<span data-ttu-id="a3de5-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3de5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3de5-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3de5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3de5-143">입력</span><span class="sxs-lookup"><span data-stu-id="a3de5-143">INPUTS</span></span>

### <span data-ttu-id="a3de5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a3de5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a3de5-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a3de5-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a3de5-146">출력</span><span class="sxs-lookup"><span data-stu-id="a3de5-146">OUTPUTS</span></span>

### <span data-ttu-id="a3de5-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="a3de5-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="a3de5-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3de5-148">NOTES</span></span>

## <span data-ttu-id="a3de5-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3de5-149">RELATED LINKS</span></span>
