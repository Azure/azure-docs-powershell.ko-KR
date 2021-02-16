---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209024"
---
# <span data-ttu-id="3f4cf-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f4cf-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="3f4cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4cf-103">통합 런타임이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="3f4cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f4cf-104">SYNTAX</span></span>

### <span data-ttu-id="3f4cf-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3f4cf-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4cf-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4cf-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4cf-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4cf-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4cf-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4cf-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4cf-109">설명</span><span class="sxs-lookup"><span data-stu-id="3f4cf-109">DESCRIPTION</span></span>
<span data-ttu-id="3f4cf-110">**Remove-AzSynapseIntegrationRuntime** cmdlet은 통합 런타임을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="3f4cf-111">예제</span><span class="sxs-lookup"><span data-stu-id="3f4cf-111">EXAMPLES</span></span>

### <span data-ttu-id="3f4cf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3f4cf-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="3f4cf-113">이 명령은 ContosoWorkspace라는 작업 영역에서 'test-reserved-ir'이라는 통합 런타임을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="3f4cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f4cf-114">PARAMETERS</span></span>

### <span data-ttu-id="3f4cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4cf-115">-DefaultProfile</span></span>
<span data-ttu-id="3f4cf-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f4cf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3f4cf-117">-Force</span></span>
<span data-ttu-id="3f4cf-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3f4cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f4cf-119">-InputObject</span></span>
<span data-ttu-id="3f4cf-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="3f4cf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3f4cf-121">-Name</span></span>
<span data-ttu-id="3f4cf-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="3f4cf-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-124">Resource group name.</span></span>

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

### <span data-ttu-id="3f4cf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f4cf-125">-ResourceId</span></span>
<span data-ttu-id="3f4cf-126">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="3f4cf-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f4cf-127">-WorkspaceName</span></span>
<span data-ttu-id="3f4cf-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3f4cf-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f4cf-129">-WorkspaceObject</span></span>
<span data-ttu-id="3f4cf-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3f4cf-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f4cf-131">-Confirm</span></span>
<span data-ttu-id="3f4cf-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4cf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4cf-133">-WhatIf</span></span>
<span data-ttu-id="3f4cf-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3f4cf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4cf-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4cf-136">CommonParameters</span></span>
<span data-ttu-id="3f4cf-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4cf-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3f4cf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4cf-139">입력</span><span class="sxs-lookup"><span data-stu-id="3f4cf-139">INPUTS</span></span>

### <span data-ttu-id="3f4cf-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f4cf-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3f4cf-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f4cf-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3f4cf-142">출력</span><span class="sxs-lookup"><span data-stu-id="3f4cf-142">OUTPUTS</span></span>

### <span data-ttu-id="3f4cf-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="3f4cf-143">System.Void</span></span>

## <span data-ttu-id="3f4cf-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f4cf-144">NOTES</span></span>

## <span data-ttu-id="3f4cf-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f4cf-145">RELATED LINKS</span></span>
