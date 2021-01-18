---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493244"
---
# <span data-ttu-id="22cd2-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="22cd2-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="22cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="22cd2-103">통합 런타임 노드 간 자격 증명을 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="22cd2-104">구문</span><span class="sxs-lookup"><span data-stu-id="22cd2-104">SYNTAX</span></span>

### <span data-ttu-id="22cd2-105">StopByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="22cd2-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22cd2-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22cd2-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22cd2-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22cd2-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22cd2-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22cd2-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22cd2-109">설명</span><span class="sxs-lookup"><span data-stu-id="22cd2-109">DESCRIPTION</span></span>
<span data-ttu-id="22cd2-110">**Sync-AzSynapseIntegrationRuntimeCredential** cmdlet은 통합 런타임 노드 간에서 모든 프레미스 자격 증명을 동기화합니다. 이 경우 모든 노드에서 자격 증명이 동일하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="22cd2-111">예제</span><span class="sxs-lookup"><span data-stu-id="22cd2-111">EXAMPLES</span></span>

### <span data-ttu-id="22cd2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="22cd2-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="22cd2-113">통합 런타임 노드 간 자격 증명을 동기화합니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="22cd2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22cd2-114">PARAMETERS</span></span>

### <span data-ttu-id="22cd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cd2-115">-DefaultProfile</span></span>
<span data-ttu-id="22cd2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cd2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="22cd2-117">-Force</span></span>
<span data-ttu-id="22cd2-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="22cd2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22cd2-119">-InputObject</span></span>
<span data-ttu-id="22cd2-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22cd2-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="22cd2-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="22cd2-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cd2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cd2-123">-ResourceGroupName</span></span>
<span data-ttu-id="22cd2-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cd2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22cd2-125">-ResourceId</span></span>
<span data-ttu-id="22cd2-126">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cd2-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="22cd2-127">-WorkspaceName</span></span>
<span data-ttu-id="22cd2-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cd2-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="22cd2-129">-WorkspaceObject</span></span>
<span data-ttu-id="22cd2-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22cd2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22cd2-131">-Confirm</span></span>
<span data-ttu-id="22cd2-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22cd2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22cd2-133">-WhatIf</span></span>
<span data-ttu-id="22cd2-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="22cd2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22cd2-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22cd2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cd2-136">CommonParameters</span></span>
<span data-ttu-id="22cd2-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22cd2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cd2-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22cd2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cd2-139">입력</span><span class="sxs-lookup"><span data-stu-id="22cd2-139">INPUTS</span></span>

### <span data-ttu-id="22cd2-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="22cd2-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="22cd2-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="22cd2-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="22cd2-142">출력</span><span class="sxs-lookup"><span data-stu-id="22cd2-142">OUTPUTS</span></span>

### <span data-ttu-id="22cd2-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="22cd2-143">System.Void</span></span>

## <span data-ttu-id="22cd2-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22cd2-144">NOTES</span></span>

## <span data-ttu-id="22cd2-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22cd2-145">RELATED LINKS</span></span>
