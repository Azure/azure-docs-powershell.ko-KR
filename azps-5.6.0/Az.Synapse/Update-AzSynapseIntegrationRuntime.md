---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 004cfc8e0bd22be1f57a320cf10aa7d7f53cbb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990710"
---
# <span data-ttu-id="ade4e-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ade4e-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="ade4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade4e-102">SYNOPSIS</span></span>
<span data-ttu-id="ade4e-103">통합 런타임을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="ade4e-104">구문</span><span class="sxs-lookup"><span data-stu-id="ade4e-104">SYNTAX</span></span>

### <span data-ttu-id="ade4e-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ade4e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade4e-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade4e-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade4e-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade4e-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ade4e-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ade4e-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ade4e-109">설명</span><span class="sxs-lookup"><span data-stu-id="ade4e-109">DESCRIPTION</span></span>
<span data-ttu-id="ade4e-110">**Update-AzSynapseIntegrationRuntime** cmdlet은 통합 런타임 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="ade4e-111">현재 cmdlet은 자체 호스팅 통합 런타임에 대해 'AutoUpdate' 및 'AutoUpdateDelayOffset' 업데이트만 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="ade4e-112">예제</span><span class="sxs-lookup"><span data-stu-id="ade4e-112">EXAMPLES</span></span>

### <span data-ttu-id="ade4e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ade4e-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="ade4e-114">cmdlet은 'test-selfhost-ir'이라는 자체 호스팅 통합 런타임을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ade4e-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ade4e-115">PARAMETERS</span></span>

### <span data-ttu-id="ade4e-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="ade4e-116">-AutoUpdate</span></span>
<span data-ttu-id="ade4e-117">자체 호스팅 통합 런타임 자동 업데이트를 사용하도록 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4e-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="ade4e-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="ade4e-119">자체 호스팅 통합 런타임 자동 업데이트의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade4e-120">-DefaultProfile</span></span>
<span data-ttu-id="ade4e-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade4e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ade4e-122">-InputObject</span></span>
<span data-ttu-id="ade4e-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="ade4e-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ade4e-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ade4e-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="ade4e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade4e-126">-ResourceGroupName</span></span>
<span data-ttu-id="ade4e-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-127">Resource group name.</span></span>

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

### <span data-ttu-id="ade4e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ade4e-128">-ResourceId</span></span>
<span data-ttu-id="ade4e-129">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="ade4e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ade4e-130">-WorkspaceName</span></span>
<span data-ttu-id="ade4e-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ade4e-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ade4e-132">-WorkspaceObject</span></span>
<span data-ttu-id="ade4e-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ade4e-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ade4e-134">-Confirm</span></span>
<span data-ttu-id="ade4e-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade4e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade4e-136">-WhatIf</span></span>
<span data-ttu-id="ade4e-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade4e-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade4e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade4e-139">CommonParameters</span></span>
<span data-ttu-id="ade4e-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ade4e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade4e-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ade4e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade4e-142">입력</span><span class="sxs-lookup"><span data-stu-id="ade4e-142">INPUTS</span></span>

### <span data-ttu-id="ade4e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ade4e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ade4e-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ade4e-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ade4e-145">출력</span><span class="sxs-lookup"><span data-stu-id="ade4e-145">OUTPUTS</span></span>

### <span data-ttu-id="ade4e-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="ade4e-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="ade4e-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ade4e-147">NOTES</span></span>

## <span data-ttu-id="ade4e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ade4e-148">RELATED LINKS</span></span>
