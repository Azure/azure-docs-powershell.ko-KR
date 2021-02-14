---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197308"
---
# <span data-ttu-id="205a5-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="205a5-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="205a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205a5-102">SYNOPSIS</span></span>
<span data-ttu-id="205a5-103">작업 영역의 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="205a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="205a5-104">SYNTAX</span></span>

### <span data-ttu-id="205a5-105">StopByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="205a5-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205a5-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="205a5-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="205a5-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="205a5-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205a5-108">설명</span><span class="sxs-lookup"><span data-stu-id="205a5-108">DESCRIPTION</span></span>
<span data-ttu-id="205a5-109">**Stop-AzSynapseTrigger** cmdlet은 작업 영역의 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="205a5-110">트리거가 '시작' 상태인 경우 cmdlet은 트리거를 중지하고 더 이상 파이프라인을 호출하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="205a5-111">트리거가 이미 '중지됨' 상태인 경우 이 cmdlet은 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="205a5-112">예제</span><span class="sxs-lookup"><span data-stu-id="205a5-112">EXAMPLES</span></span>

### <span data-ttu-id="205a5-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="205a5-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="205a5-114">작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="205a5-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="205a5-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="205a5-116">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="205a5-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="205a5-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="205a5-118">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="205a5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="205a5-119">PARAMETERS</span></span>

### <span data-ttu-id="205a5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="205a5-120">-AsJob</span></span>
<span data-ttu-id="205a5-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="205a5-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="205a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205a5-122">-DefaultProfile</span></span>
<span data-ttu-id="205a5-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205a5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="205a5-124">-InputObject</span></span>
<span data-ttu-id="205a5-125">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205a5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="205a5-126">-Name</span></span>
<span data-ttu-id="205a5-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205a5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="205a5-128">-PassThru</span></span>
<span data-ttu-id="205a5-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="205a5-130">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="205a5-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="205a5-131">-WorkspaceName</span></span>
<span data-ttu-id="205a5-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205a5-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="205a5-133">-WorkspaceObject</span></span>
<span data-ttu-id="205a5-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205a5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="205a5-135">-Confirm</span></span>
<span data-ttu-id="205a5-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205a5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205a5-137">-WhatIf</span></span>
<span data-ttu-id="205a5-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="205a5-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="205a5-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205a5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205a5-140">CommonParameters</span></span>
<span data-ttu-id="205a5-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="205a5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205a5-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="205a5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205a5-143">입력</span><span class="sxs-lookup"><span data-stu-id="205a5-143">INPUTS</span></span>

### <span data-ttu-id="205a5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="205a5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="205a5-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="205a5-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="205a5-146">출력</span><span class="sxs-lookup"><span data-stu-id="205a5-146">OUTPUTS</span></span>

### <span data-ttu-id="205a5-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="205a5-147">System.Boolean</span></span>

## <span data-ttu-id="205a5-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="205a5-148">NOTES</span></span>

## <span data-ttu-id="205a5-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="205a5-149">RELATED LINKS</span></span>
