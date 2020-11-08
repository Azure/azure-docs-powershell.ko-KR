---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217143"
---
# <span data-ttu-id="3284f-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="3284f-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="3284f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3284f-102">SYNOPSIS</span></span>
<span data-ttu-id="3284f-103">통합 런타임에서 지정 된 이름의 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="3284f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3284f-104">SYNTAX</span></span>

### <span data-ttu-id="3284f-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3284f-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3284f-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3284f-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3284f-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3284f-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3284f-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3284f-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3284f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="3284f-109">DESCRIPTION</span></span>
<span data-ttu-id="3284f-110">**AzSynapseIntegrationRuntimeNode** cmdlet은 통합 런타임에서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="3284f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3284f-111">EXAMPLES</span></span>

### <span data-ttu-id="3284f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3284f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="3284f-113">통합 런타임에서 지정 된 이름의 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="3284f-114">변수</span><span class="sxs-lookup"><span data-stu-id="3284f-114">PARAMETERS</span></span>

### <span data-ttu-id="3284f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3284f-115">-DefaultProfile</span></span>
<span data-ttu-id="3284f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3284f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3284f-117">-Force</span></span>
<span data-ttu-id="3284f-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3284f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3284f-119">-InputObject</span></span>
<span data-ttu-id="3284f-120">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="3284f-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3284f-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="3284f-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="3284f-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="3284f-123">-NodeName</span></span>
<span data-ttu-id="3284f-124">통합 런타임 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="3284f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3284f-125">-ResourceGroupName</span></span>
<span data-ttu-id="3284f-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-126">Resource group name.</span></span>

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

### <span data-ttu-id="3284f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3284f-127">-ResourceId</span></span>
<span data-ttu-id="3284f-128">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="3284f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3284f-129">-WorkspaceName</span></span>
<span data-ttu-id="3284f-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3284f-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3284f-131">-WorkspaceObject</span></span>
<span data-ttu-id="3284f-132">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3284f-133">-확인</span><span class="sxs-lookup"><span data-stu-id="3284f-133">-Confirm</span></span>
<span data-ttu-id="3284f-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3284f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3284f-135">-WhatIf</span></span>
<span data-ttu-id="3284f-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3284f-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3284f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3284f-138">CommonParameters</span></span>
<span data-ttu-id="3284f-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3284f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3284f-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3284f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3284f-141">입력</span><span class="sxs-lookup"><span data-stu-id="3284f-141">INPUTS</span></span>

### <span data-ttu-id="3284f-142">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="3284f-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3284f-143">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="3284f-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="3284f-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3284f-144">System.String</span></span>

## <span data-ttu-id="3284f-145">출력</span><span class="sxs-lookup"><span data-stu-id="3284f-145">OUTPUTS</span></span>

### <span data-ttu-id="3284f-146">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="3284f-146">System.Void</span></span>

## <span data-ttu-id="3284f-147">상속자</span><span class="sxs-lookup"><span data-stu-id="3284f-147">NOTES</span></span>

## <span data-ttu-id="3284f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3284f-148">RELATED LINKS</span></span>
