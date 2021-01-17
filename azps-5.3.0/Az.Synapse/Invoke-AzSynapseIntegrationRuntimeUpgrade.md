---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383685"
---
# <span data-ttu-id="08142-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="08142-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="08142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08142-102">SYNOPSIS</span></span>
<span data-ttu-id="08142-103">자체 호스팅 통합 런타임 업그레이드</span><span class="sxs-lookup"><span data-stu-id="08142-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="08142-104">구문</span><span class="sxs-lookup"><span data-stu-id="08142-104">SYNTAX</span></span>

### <span data-ttu-id="08142-105">InvokeByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="08142-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08142-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08142-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08142-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08142-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08142-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08142-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08142-109">설명</span><span class="sxs-lookup"><span data-stu-id="08142-109">DESCRIPTION</span></span>
<span data-ttu-id="08142-110">**Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet은 새 버전을 사용할 수 있는 경우 자체 호스팅 통합 런타임으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="08142-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="08142-111">예제</span><span class="sxs-lookup"><span data-stu-id="08142-111">EXAMPLES</span></span>

### <span data-ttu-id="08142-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="08142-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="08142-113">cmdlet은 작업 영역 ContosoWorkspace에서 'test-selfhost-ir'이라는 자체 호스팅 통합 런타임이 업그레이드됩니다.</span><span class="sxs-lookup"><span data-stu-id="08142-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="08142-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08142-114">PARAMETERS</span></span>

### <span data-ttu-id="08142-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08142-115">-DefaultProfile</span></span>
<span data-ttu-id="08142-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08142-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08142-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08142-117">-InputObject</span></span>
<span data-ttu-id="08142-118">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="08142-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08142-119">-Name</span><span class="sxs-lookup"><span data-stu-id="08142-119">-Name</span></span>
<span data-ttu-id="08142-120">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08142-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08142-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08142-121">-ResourceGroupName</span></span>
<span data-ttu-id="08142-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08142-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08142-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08142-123">-ResourceId</span></span>
<span data-ttu-id="08142-124">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="08142-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08142-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08142-125">-WorkspaceName</span></span>
<span data-ttu-id="08142-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08142-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08142-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="08142-127">-WorkspaceObject</span></span>
<span data-ttu-id="08142-128">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="08142-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08142-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08142-129">-Confirm</span></span>
<span data-ttu-id="08142-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="08142-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08142-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08142-131">-WhatIf</span></span>
<span data-ttu-id="08142-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="08142-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08142-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08142-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08142-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08142-134">CommonParameters</span></span>
<span data-ttu-id="08142-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08142-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08142-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08142-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08142-137">입력</span><span class="sxs-lookup"><span data-stu-id="08142-137">INPUTS</span></span>

### <span data-ttu-id="08142-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="08142-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="08142-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="08142-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="08142-140">출력</span><span class="sxs-lookup"><span data-stu-id="08142-140">OUTPUTS</span></span>

### <span data-ttu-id="08142-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="08142-141">System.Void</span></span>

## <span data-ttu-id="08142-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08142-142">NOTES</span></span>

## <span data-ttu-id="08142-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08142-143">RELATED LINKS</span></span>
