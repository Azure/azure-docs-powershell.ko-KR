---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190553"
---
# <span data-ttu-id="6ad80-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ad80-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="6ad80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad80-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad80-103">통합 런타임 업데이트</span><span class="sxs-lookup"><span data-stu-id="6ad80-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="6ad80-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ad80-104">SYNTAX</span></span>

### <span data-ttu-id="6ad80-105">UpdateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ad80-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad80-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad80-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad80-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad80-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ad80-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad80-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad80-109">설명</span><span class="sxs-lookup"><span data-stu-id="6ad80-109">DESCRIPTION</span></span>
<span data-ttu-id="6ad80-110">**Update-AzSynapseIntegrationRuntime** cmdlet은 통합 런타임 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="6ad80-111">현재 cmdlet은 자체 호스팅 통합 런타임에 대해 'AutoUpdate' 및 'AutoUpdateDelayOffset' 업데이트만 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="6ad80-112">예제</span><span class="sxs-lookup"><span data-stu-id="6ad80-112">EXAMPLES</span></span>

### <span data-ttu-id="6ad80-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ad80-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="6ad80-114">cmdlet은 'test-selfhost-ir'이라는 자체 호스팅 통합 런타임을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6ad80-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ad80-115">PARAMETERS</span></span>

### <span data-ttu-id="6ad80-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="6ad80-116">-AutoUpdate</span></span>
<span data-ttu-id="6ad80-117">자체 호스팅 통합 런타임 자동 업데이트를 사용 또는 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="6ad80-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="6ad80-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="6ad80-119">자체 호스팅 통합 런타임 자동 업데이트에 대한 하루의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="6ad80-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad80-120">-DefaultProfile</span></span>
<span data-ttu-id="6ad80-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad80-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ad80-122">-InputObject</span></span>
<span data-ttu-id="6ad80-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="6ad80-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6ad80-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6ad80-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="6ad80-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad80-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ad80-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-127">Resource group name.</span></span>

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

### <span data-ttu-id="6ad80-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad80-128">-ResourceId</span></span>
<span data-ttu-id="6ad80-129">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6ad80-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6ad80-130">-WorkspaceName</span></span>
<span data-ttu-id="6ad80-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6ad80-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6ad80-132">-WorkspaceObject</span></span>
<span data-ttu-id="6ad80-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6ad80-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ad80-134">-Confirm</span></span>
<span data-ttu-id="6ad80-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad80-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad80-136">-WhatIf</span></span>
<span data-ttu-id="6ad80-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6ad80-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad80-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad80-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad80-139">CommonParameters</span></span>
<span data-ttu-id="6ad80-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad80-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad80-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ad80-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad80-142">입력</span><span class="sxs-lookup"><span data-stu-id="6ad80-142">INPUTS</span></span>

### <span data-ttu-id="6ad80-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6ad80-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6ad80-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ad80-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6ad80-145">출력</span><span class="sxs-lookup"><span data-stu-id="6ad80-145">OUTPUTS</span></span>

### <span data-ttu-id="6ad80-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="6ad80-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="6ad80-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ad80-147">NOTES</span></span>

## <span data-ttu-id="6ad80-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ad80-148">RELATED LINKS</span></span>
