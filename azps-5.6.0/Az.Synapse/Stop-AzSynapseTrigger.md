---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 94773a882a4bb2d29712fff6796d34cff6254df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991956"
---
# <span data-ttu-id="f361f-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="f361f-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="f361f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f361f-102">SYNOPSIS</span></span>
<span data-ttu-id="f361f-103">작업 영역의 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="f361f-104">구문</span><span class="sxs-lookup"><span data-stu-id="f361f-104">SYNTAX</span></span>

### <span data-ttu-id="f361f-105">StopByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f361f-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f361f-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="f361f-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f361f-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="f361f-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f361f-108">설명</span><span class="sxs-lookup"><span data-stu-id="f361f-108">DESCRIPTION</span></span>
<span data-ttu-id="f361f-109">**Stop-AzSynapseTrigger** cmdlet은 작업 영역의 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="f361f-110">트리거가 '시작' 상태인 경우 cmdlet은 트리거를 중지하고 더 이상 파이프라인을 호출하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="f361f-111">트리거가 이미 '중지됨' 상태인 경우 이 cmdlet은 영향을주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="f361f-112">예제</span><span class="sxs-lookup"><span data-stu-id="f361f-112">EXAMPLES</span></span>

### <span data-ttu-id="f361f-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f361f-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="f361f-114">작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f361f-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="f361f-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="f361f-116">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="f361f-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="f361f-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="f361f-118">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f361f-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f361f-119">PARAMETERS</span></span>

### <span data-ttu-id="f361f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f361f-120">-AsJob</span></span>
<span data-ttu-id="f361f-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f361f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f361f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f361f-122">-DefaultProfile</span></span>
<span data-ttu-id="f361f-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f361f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f361f-124">-InputObject</span></span>
<span data-ttu-id="f361f-125">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-125">The trigger object.</span></span>

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

### <span data-ttu-id="f361f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f361f-126">-Name</span></span>
<span data-ttu-id="f361f-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-127">The trigger name.</span></span>

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

### <span data-ttu-id="f361f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f361f-128">-PassThru</span></span>
<span data-ttu-id="f361f-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f361f-130">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f361f-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f361f-131">-WorkspaceName</span></span>
<span data-ttu-id="f361f-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f361f-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f361f-133">-WorkspaceObject</span></span>
<span data-ttu-id="f361f-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f361f-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f361f-135">-Confirm</span></span>
<span data-ttu-id="f361f-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f361f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f361f-137">-WhatIf</span></span>
<span data-ttu-id="f361f-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f361f-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f361f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f361f-140">CommonParameters</span></span>
<span data-ttu-id="f361f-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f361f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f361f-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f361f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f361f-143">입력</span><span class="sxs-lookup"><span data-stu-id="f361f-143">INPUTS</span></span>

### <span data-ttu-id="f361f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f361f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f361f-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="f361f-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="f361f-146">출력</span><span class="sxs-lookup"><span data-stu-id="f361f-146">OUTPUTS</span></span>

### <span data-ttu-id="f361f-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f361f-147">System.Boolean</span></span>

## <span data-ttu-id="f361f-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f361f-148">NOTES</span></span>

## <span data-ttu-id="f361f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f361f-149">RELATED LINKS</span></span>
