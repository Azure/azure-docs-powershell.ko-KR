---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358457"
---
# <span data-ttu-id="b1871-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="b1871-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="b1871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1871-102">SYNOPSIS</span></span>
<span data-ttu-id="b1871-103">작업 영역의 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="b1871-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1871-104">SYNTAX</span></span>

### <span data-ttu-id="b1871-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b1871-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1871-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="b1871-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1871-107">설명</span><span class="sxs-lookup"><span data-stu-id="b1871-107">DESCRIPTION</span></span>
<span data-ttu-id="b1871-108">**Set-AzSynapseTrigger** cmdlet은 작업 영역의 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="b1871-109">트리거는 '중지됨' 상태로 생성됩니다. 즉, 트리거가 참조하는 파이프라인 호출을 즉시 시작하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="b1871-110">예제</span><span class="sxs-lookup"><span data-stu-id="b1871-110">EXAMPLES</span></span>

### <span data-ttu-id="b1871-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b1871-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="b1871-112">작업 영역 ContosoWorkspace에서 ContosoTrigger라는 새 트리거를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="b1871-113">트리거는 '중지됨' 상태로 생성됩니다. 즉, 즉시 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="b1871-114">cmdlet을 사용하여 트리거를 `Start-AzDataFactoryV2Trigger` 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="b1871-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="b1871-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="b1871-116">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 새 트리거를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="b1871-117">트리거는 '중지됨' 상태로 생성됩니다. 즉, 즉시 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="b1871-118">cmdlet을 사용하여 트리거를 `Start-AzDataFactoryV2Trigger` 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="b1871-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1871-119">PARAMETERS</span></span>

### <span data-ttu-id="b1871-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1871-120">-AsJob</span></span>
<span data-ttu-id="b1871-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b1871-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1871-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1871-122">-DefaultProfile</span></span>
<span data-ttu-id="b1871-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1871-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b1871-124">-DefinitionFile</span></span>
<span data-ttu-id="b1871-125">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-125">The JSON file path.</span></span>

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

### <span data-ttu-id="b1871-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b1871-126">-Name</span></span>
<span data-ttu-id="b1871-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-127">The trigger name.</span></span>

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

### <span data-ttu-id="b1871-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1871-128">-WorkspaceName</span></span>
<span data-ttu-id="b1871-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b1871-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b1871-130">-WorkspaceObject</span></span>
<span data-ttu-id="b1871-131">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b1871-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1871-132">-Confirm</span></span>
<span data-ttu-id="b1871-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1871-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1871-134">-WhatIf</span></span>
<span data-ttu-id="b1871-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1871-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1871-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1871-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1871-137">CommonParameters</span></span>
<span data-ttu-id="b1871-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1871-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1871-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1871-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1871-140">입력</span><span class="sxs-lookup"><span data-stu-id="b1871-140">INPUTS</span></span>

### <span data-ttu-id="b1871-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b1871-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b1871-142">출력</span><span class="sxs-lookup"><span data-stu-id="b1871-142">OUTPUTS</span></span>

### <span data-ttu-id="b1871-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b1871-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b1871-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1871-144">NOTES</span></span>

## <span data-ttu-id="b1871-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1871-145">RELATED LINKS</span></span>
