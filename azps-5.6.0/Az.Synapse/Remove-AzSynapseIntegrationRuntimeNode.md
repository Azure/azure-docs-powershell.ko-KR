---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 07b1b36222f0d1a31d4a4a7374957336246f0073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011307"
---
# <span data-ttu-id="ff3a9-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ff3a9-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="ff3a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff3a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3a9-103">통합 런타임에 지정한 이름으로 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="ff3a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff3a9-104">SYNTAX</span></span>

### <span data-ttu-id="ff3a9-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff3a9-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff3a9-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff3a9-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff3a9-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff3a9-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff3a9-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff3a9-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff3a9-109">설명</span><span class="sxs-lookup"><span data-stu-id="ff3a9-109">DESCRIPTION</span></span>
<span data-ttu-id="ff3a9-110">**Remove-AzSynapseIntegrationRuntimeNode** cmdlet은 통합 런타임의 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="ff3a9-111">예제</span><span class="sxs-lookup"><span data-stu-id="ff3a9-111">EXAMPLES</span></span>

### <span data-ttu-id="ff3a9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff3a9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="ff3a9-113">통합 런타임에 지정한 이름으로 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="ff3a9-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff3a9-114">PARAMETERS</span></span>

### <span data-ttu-id="ff3a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3a9-115">-DefaultProfile</span></span>
<span data-ttu-id="ff3a9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff3a9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ff3a9-117">-Force</span></span>
<span data-ttu-id="ff3a9-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ff3a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff3a9-119">-InputObject</span></span>
<span data-ttu-id="ff3a9-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a9-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ff3a9-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ff3a9-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a9-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="ff3a9-123">-NodeName</span></span>
<span data-ttu-id="ff3a9-124">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff3a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff3a9-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff3a9-127">-ResourceId</span></span>
<span data-ttu-id="ff3a9-128">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a9-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff3a9-129">-WorkspaceName</span></span>
<span data-ttu-id="ff3a9-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a9-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ff3a9-131">-WorkspaceObject</span></span>
<span data-ttu-id="ff3a9-132">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a9-133">-확인</span><span class="sxs-lookup"><span data-stu-id="ff3a9-133">-Confirm</span></span>
<span data-ttu-id="ff3a9-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff3a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3a9-135">-WhatIf</span></span>
<span data-ttu-id="ff3a9-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff3a9-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff3a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3a9-138">CommonParameters</span></span>
<span data-ttu-id="ff3a9-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff3a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3a9-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff3a9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3a9-141">입력</span><span class="sxs-lookup"><span data-stu-id="ff3a9-141">INPUTS</span></span>

### <span data-ttu-id="ff3a9-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff3a9-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ff3a9-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ff3a9-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="ff3a9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ff3a9-144">System.String</span></span>

## <span data-ttu-id="ff3a9-145">출력</span><span class="sxs-lookup"><span data-stu-id="ff3a9-145">OUTPUTS</span></span>

### <span data-ttu-id="ff3a9-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="ff3a9-146">System.Void</span></span>

## <span data-ttu-id="ff3a9-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff3a9-147">NOTES</span></span>

## <span data-ttu-id="ff3a9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff3a9-148">RELATED LINKS</span></span>
