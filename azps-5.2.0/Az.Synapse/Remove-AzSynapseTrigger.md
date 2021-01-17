---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 648d215066fb7bd827d43ec9d063a7994ada82f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337298"
---
# <span data-ttu-id="c5acb-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="c5acb-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="c5acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5acb-102">SYNOPSIS</span></span>
<span data-ttu-id="c5acb-103">작업 영역의 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="c5acb-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5acb-104">SYNTAX</span></span>

### <span data-ttu-id="c5acb-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c5acb-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5acb-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="c5acb-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5acb-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c5acb-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5acb-108">설명</span><span class="sxs-lookup"><span data-stu-id="c5acb-108">DESCRIPTION</span></span>
<span data-ttu-id="c5acb-109">**Remove-AzSynapseTrigger** cmdlet은 작업 영역의 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="c5acb-110">예제</span><span class="sxs-lookup"><span data-stu-id="c5acb-110">EXAMPLES</span></span>

### <span data-ttu-id="c5acb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5acb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="c5acb-112">작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c5acb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c5acb-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="c5acb-114">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="c5acb-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="c5acb-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="c5acb-116">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c5acb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5acb-117">PARAMETERS</span></span>

### <span data-ttu-id="c5acb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5acb-118">-AsJob</span></span>
<span data-ttu-id="c5acb-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c5acb-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5acb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5acb-120">-DefaultProfile</span></span>
<span data-ttu-id="c5acb-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5acb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c5acb-122">-Force</span></span>
<span data-ttu-id="c5acb-123">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c5acb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5acb-124">-InputObject</span></span>
<span data-ttu-id="c5acb-125">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5acb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c5acb-126">-Name</span></span>
<span data-ttu-id="c5acb-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5acb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5acb-128">-PassThru</span></span>
<span data-ttu-id="c5acb-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c5acb-130">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c5acb-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5acb-131">-WorkspaceName</span></span>
<span data-ttu-id="c5acb-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5acb-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c5acb-133">-WorkspaceObject</span></span>
<span data-ttu-id="c5acb-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5acb-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5acb-135">-Confirm</span></span>
<span data-ttu-id="c5acb-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5acb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5acb-137">-WhatIf</span></span>
<span data-ttu-id="c5acb-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c5acb-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5acb-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5acb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5acb-140">CommonParameters</span></span>
<span data-ttu-id="c5acb-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5acb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5acb-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5acb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5acb-143">입력</span><span class="sxs-lookup"><span data-stu-id="c5acb-143">INPUTS</span></span>

### <span data-ttu-id="c5acb-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5acb-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c5acb-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="c5acb-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="c5acb-146">출력</span><span class="sxs-lookup"><span data-stu-id="c5acb-146">OUTPUTS</span></span>

### <span data-ttu-id="c5acb-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5acb-147">System.Boolean</span></span>

## <span data-ttu-id="c5acb-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5acb-148">NOTES</span></span>

## <span data-ttu-id="c5acb-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5acb-149">RELATED LINKS</span></span>
