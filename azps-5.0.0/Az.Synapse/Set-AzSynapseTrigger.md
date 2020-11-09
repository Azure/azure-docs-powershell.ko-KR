---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310439"
---
# <span data-ttu-id="4ed6b-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="4ed6b-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="4ed6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed6b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed6b-103">작업 영역에 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="4ed6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ed6b-104">SYNTAX</span></span>

### <span data-ttu-id="4ed6b-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ed6b-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ed6b-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="4ed6b-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ed6b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4ed6b-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed6b-108">**Set-AzSynapseTrigger** cmdlet은 작업 영역에서 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="4ed6b-109">트리거는 ' 중지 됨 ' 상태에서 만들어지고,이는 자신이 참조 하는 파이프라인 호출을 즉시 시작 하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="4ed6b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4ed6b-110">EXAMPLES</span></span>

### <span data-ttu-id="4ed6b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ed6b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="4ed6b-112">작업 영역 ContosoWorkspace에서 ContosoTrigger 이라는 새 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="4ed6b-113">트리거가 ' 중지 됨 ' 상태에 만들어지고,이는 즉시 시작 되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="4ed6b-114">트리거는 cmdlet을 사용 하 여 시작할 수 있습니다 `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="4ed6b-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="4ed6b-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="4ed6b-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="4ed6b-116">Workspace ContosoWorkspace to 파이프라인에서 ContosoTrigger 이라는 새 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="4ed6b-117">트리거가 ' 중지 됨 ' 상태에 만들어지고,이는 즉시 시작 되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="4ed6b-118">트리거는 cmdlet을 사용 하 여 시작할 수 있습니다 `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="4ed6b-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="4ed6b-119">변수</span><span class="sxs-lookup"><span data-stu-id="4ed6b-119">PARAMETERS</span></span>

### <span data-ttu-id="4ed6b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ed6b-120">-AsJob</span></span>
<span data-ttu-id="4ed6b-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4ed6b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ed6b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed6b-122">-DefaultProfile</span></span>
<span data-ttu-id="4ed6b-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ed6b-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4ed6b-124">-DefinitionFile</span></span>
<span data-ttu-id="4ed6b-125">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-125">The JSON file path.</span></span>

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

### <span data-ttu-id="4ed6b-126">-이름</span><span class="sxs-lookup"><span data-stu-id="4ed6b-126">-Name</span></span>
<span data-ttu-id="4ed6b-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-127">The trigger name.</span></span>

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

### <span data-ttu-id="4ed6b-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ed6b-128">-WorkspaceName</span></span>
<span data-ttu-id="4ed6b-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4ed6b-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4ed6b-130">-WorkspaceObject</span></span>
<span data-ttu-id="4ed6b-131">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4ed6b-132">-확인</span><span class="sxs-lookup"><span data-stu-id="4ed6b-132">-Confirm</span></span>
<span data-ttu-id="4ed6b-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ed6b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ed6b-134">-WhatIf</span></span>
<span data-ttu-id="4ed6b-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ed6b-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ed6b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed6b-137">CommonParameters</span></span>
<span data-ttu-id="4ed6b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed6b-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed6b-140">입력</span><span class="sxs-lookup"><span data-stu-id="4ed6b-140">INPUTS</span></span>

### <span data-ttu-id="4ed6b-141">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4ed6b-142">출력</span><span class="sxs-lookup"><span data-stu-id="4ed6b-142">OUTPUTS</span></span>

### <span data-ttu-id="4ed6b-143">Synapse. PSTriggerResource/.</span><span class="sxs-lookup"><span data-stu-id="4ed6b-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="4ed6b-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4ed6b-144">NOTES</span></span>

## <span data-ttu-id="4ed6b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ed6b-145">RELATED LINKS</span></span>
