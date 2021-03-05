---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 0852cbbce26e1f95bfb75975418fae30038316ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992049"
---
# <span data-ttu-id="03200-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="03200-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="03200-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03200-102">SYNOPSIS</span></span>
<span data-ttu-id="03200-103">작업 영역에서 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03200-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="03200-104">구문</span><span class="sxs-lookup"><span data-stu-id="03200-104">SYNTAX</span></span>

### <span data-ttu-id="03200-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="03200-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03200-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="03200-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03200-107">설명</span><span class="sxs-lookup"><span data-stu-id="03200-107">DESCRIPTION</span></span>
<span data-ttu-id="03200-108">**Set-AzSynapseTrigger** cmdlet은 작업 영역의 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03200-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="03200-109">트리거는 '중지됨' 상태로 생성됩니다. 즉, 트리거가 참조하는 파이프라인을 즉시 호출하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03200-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="03200-110">예제</span><span class="sxs-lookup"><span data-stu-id="03200-110">EXAMPLES</span></span>

### <span data-ttu-id="03200-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="03200-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="03200-112">작업 영역 ContosoWorkspace에서 ContosoTrigger라는 새 트리거를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="03200-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="03200-113">트리거는 '중지됨' 상태로 생성됩니다. 즉, 즉시 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03200-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="03200-114">cmdlet을 사용하여 트리거를 `Start-AzDataFactoryV2Trigger` 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03200-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="03200-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="03200-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="03200-116">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 새 트리거를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="03200-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="03200-117">트리거는 '중지됨' 상태로 생성됩니다. 즉, 즉시 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03200-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="03200-118">cmdlet을 사용하여 트리거를 `Start-AzDataFactoryV2Trigger` 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03200-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="03200-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03200-119">PARAMETERS</span></span>

### <span data-ttu-id="03200-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03200-120">-AsJob</span></span>
<span data-ttu-id="03200-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03200-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03200-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03200-122">-DefaultProfile</span></span>
<span data-ttu-id="03200-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03200-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03200-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="03200-124">-DefinitionFile</span></span>
<span data-ttu-id="03200-125">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="03200-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03200-126">-Name</span><span class="sxs-lookup"><span data-stu-id="03200-126">-Name</span></span>
<span data-ttu-id="03200-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03200-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03200-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="03200-128">-WorkspaceName</span></span>
<span data-ttu-id="03200-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03200-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03200-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="03200-130">-WorkspaceObject</span></span>
<span data-ttu-id="03200-131">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="03200-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03200-132">-확인</span><span class="sxs-lookup"><span data-stu-id="03200-132">-Confirm</span></span>
<span data-ttu-id="03200-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03200-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03200-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03200-134">-WhatIf</span></span>
<span data-ttu-id="03200-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03200-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03200-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03200-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03200-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03200-137">CommonParameters</span></span>
<span data-ttu-id="03200-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03200-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03200-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03200-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03200-140">입력</span><span class="sxs-lookup"><span data-stu-id="03200-140">INPUTS</span></span>

### <span data-ttu-id="03200-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="03200-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="03200-142">출력</span><span class="sxs-lookup"><span data-stu-id="03200-142">OUTPUTS</span></span>

### <span data-ttu-id="03200-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="03200-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="03200-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03200-144">NOTES</span></span>

## <span data-ttu-id="03200-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03200-145">RELATED LINKS</span></span>
