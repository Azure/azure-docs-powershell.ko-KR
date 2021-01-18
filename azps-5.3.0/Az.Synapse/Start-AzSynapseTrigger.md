---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493252"
---
# <span data-ttu-id="42245-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="42245-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="42245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42245-102">SYNOPSIS</span></span>
<span data-ttu-id="42245-103">작업 영역의 트리거를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="42245-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="42245-104">구문</span><span class="sxs-lookup"><span data-stu-id="42245-104">SYNTAX</span></span>

### <span data-ttu-id="42245-105">StartByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="42245-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42245-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="42245-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42245-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="42245-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42245-108">설명</span><span class="sxs-lookup"><span data-stu-id="42245-108">DESCRIPTION</span></span>
<span data-ttu-id="42245-109">**Start-AzSynapseTrigger** cmdlet은 작업 영역의 트리거를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="42245-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="42245-110">트리거가 '중지됨' 상태인 경우 cmdlet은 트리거를 시작하고 결국 정의에 따라 파이프라인을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="42245-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="42245-111">트리거가 이미 '시작' 상태인 경우 이 cmdlet은 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42245-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="42245-112">예제</span><span class="sxs-lookup"><span data-stu-id="42245-112">EXAMPLES</span></span>

### <span data-ttu-id="42245-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="42245-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="42245-114">작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="42245-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="42245-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="42245-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="42245-116">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="42245-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="42245-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="42245-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="42245-118">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="42245-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="42245-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42245-119">PARAMETERS</span></span>

### <span data-ttu-id="42245-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42245-120">-AsJob</span></span>
<span data-ttu-id="42245-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="42245-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42245-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42245-122">-DefaultProfile</span></span>
<span data-ttu-id="42245-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42245-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42245-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42245-124">-InputObject</span></span>
<span data-ttu-id="42245-125">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42245-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42245-126">-Name</span><span class="sxs-lookup"><span data-stu-id="42245-126">-Name</span></span>
<span data-ttu-id="42245-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42245-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42245-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42245-128">-PassThru</span></span>
<span data-ttu-id="42245-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42245-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="42245-130">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="42245-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="42245-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="42245-131">-WorkspaceName</span></span>
<span data-ttu-id="42245-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42245-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42245-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="42245-133">-WorkspaceObject</span></span>
<span data-ttu-id="42245-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42245-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42245-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42245-135">-Confirm</span></span>
<span data-ttu-id="42245-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42245-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42245-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42245-137">-WhatIf</span></span>
<span data-ttu-id="42245-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="42245-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42245-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42245-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42245-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42245-140">CommonParameters</span></span>
<span data-ttu-id="42245-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42245-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42245-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42245-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42245-143">입력</span><span class="sxs-lookup"><span data-stu-id="42245-143">INPUTS</span></span>

### <span data-ttu-id="42245-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="42245-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="42245-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="42245-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="42245-146">출력</span><span class="sxs-lookup"><span data-stu-id="42245-146">OUTPUTS</span></span>

### <span data-ttu-id="42245-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42245-147">System.Boolean</span></span>

## <span data-ttu-id="42245-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42245-148">NOTES</span></span>

## <span data-ttu-id="42245-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42245-149">RELATED LINKS</span></span>
