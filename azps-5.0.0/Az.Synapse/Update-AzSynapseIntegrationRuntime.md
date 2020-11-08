---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215146"
---
# <span data-ttu-id="060b6-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="060b6-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="060b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="060b6-102">SYNOPSIS</span></span>
<span data-ttu-id="060b6-103">통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="060b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="060b6-104">SYNTAX</span></span>

### <span data-ttu-id="060b6-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="060b6-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="060b6-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="060b6-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="060b6-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="060b6-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="060b6-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="060b6-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="060b6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="060b6-109">DESCRIPTION</span></span>
<span data-ttu-id="060b6-110">**업데이트 AzSynapseIntegrationRuntime** cmdlet은 통합 런타임 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="060b6-111">현재 cmdlet은 자체 호스팅 통합 런타임으로 ' 자동 업데이트 ' 및 ' AutoUpdateDelayOffset ' 업데이트가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="060b6-112">예제의</span><span class="sxs-lookup"><span data-stu-id="060b6-112">EXAMPLES</span></span>

### <span data-ttu-id="060b6-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="060b6-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="060b6-114">Cmdlet은 ' selfhost-ir ' 이라는 이름의 자체 호스팅된 통합 런타임을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="060b6-115">변수</span><span class="sxs-lookup"><span data-stu-id="060b6-115">PARAMETERS</span></span>

### <span data-ttu-id="060b6-116">-자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="060b6-116">-AutoUpdate</span></span>
<span data-ttu-id="060b6-117">자체 호스팅 통합 런타임 자동 업데이트를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="060b6-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="060b6-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="060b6-119">자체 호스팅 통합 런타임 자동 업데이트에 대 한 일 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="060b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060b6-120">-DefaultProfile</span></span>
<span data-ttu-id="060b6-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="060b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="060b6-122">-InputObject</span></span>
<span data-ttu-id="060b6-123">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="060b6-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="060b6-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="060b6-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="060b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="060b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="060b6-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-127">Resource group name.</span></span>

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

### <span data-ttu-id="060b6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="060b6-128">-ResourceId</span></span>
<span data-ttu-id="060b6-129">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="060b6-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="060b6-130">-WorkspaceName</span></span>
<span data-ttu-id="060b6-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="060b6-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="060b6-132">-WorkspaceObject</span></span>
<span data-ttu-id="060b6-133">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="060b6-134">-확인</span><span class="sxs-lookup"><span data-stu-id="060b6-134">-Confirm</span></span>
<span data-ttu-id="060b6-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="060b6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="060b6-136">-WhatIf</span></span>
<span data-ttu-id="060b6-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="060b6-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="060b6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060b6-139">CommonParameters</span></span>
<span data-ttu-id="060b6-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="060b6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060b6-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="060b6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060b6-142">입력</span><span class="sxs-lookup"><span data-stu-id="060b6-142">INPUTS</span></span>

### <span data-ttu-id="060b6-143">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="060b6-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="060b6-144">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="060b6-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="060b6-145">출력</span><span class="sxs-lookup"><span data-stu-id="060b6-145">OUTPUTS</span></span>

### <span data-ttu-id="060b6-146">Synapse. PSSelfHostedIntegrationRuntimeStatus/.</span><span class="sxs-lookup"><span data-stu-id="060b6-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="060b6-147">상속자</span><span class="sxs-lookup"><span data-stu-id="060b6-147">NOTES</span></span>

## <span data-ttu-id="060b6-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="060b6-148">RELATED LINKS</span></span>
