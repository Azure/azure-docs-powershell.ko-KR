---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216599"
---
# <span data-ttu-id="7302e-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="7302e-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="7302e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7302e-102">SYNOPSIS</span></span>
<span data-ttu-id="7302e-103">작업 영역에서 트리거를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="7302e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7302e-104">SYNTAX</span></span>

### <span data-ttu-id="7302e-105">StopByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7302e-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7302e-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="7302e-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7302e-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="7302e-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7302e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7302e-108">DESCRIPTION</span></span>
<span data-ttu-id="7302e-109">**AzSynapseTrigger** cmdlet은 작업 영역에서 트리거를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="7302e-110">트리거가 ' 시작 됨 ' 상태인 경우 cmdlet은 트리거를 중지 하 고 더 이상 파이프라인을 호출 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="7302e-111">트리거가 이미 ' 중지 됨 ' 상태인 경우에는이 cmdlet이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="7302e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7302e-112">EXAMPLES</span></span>

### <span data-ttu-id="7302e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7302e-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="7302e-114">Workspace ContosoWorkspace에서 ContosoTrigger 이라는 트리거를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7302e-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="7302e-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="7302e-116">Workspace ContosoWorkspace에서 파이프라인을 통해 ContosoTrigger 라는 트리거를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7302e-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="7302e-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="7302e-118">Workspace ContosoWorkspace to 파이프라인에서 ContosoTrigger 이라는 트리거를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7302e-119">변수</span><span class="sxs-lookup"><span data-stu-id="7302e-119">PARAMETERS</span></span>

### <span data-ttu-id="7302e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7302e-120">-AsJob</span></span>
<span data-ttu-id="7302e-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7302e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7302e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7302e-122">-DefaultProfile</span></span>
<span data-ttu-id="7302e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7302e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7302e-124">-InputObject</span></span>
<span data-ttu-id="7302e-125">트리거 개체</span><span class="sxs-lookup"><span data-stu-id="7302e-125">The trigger object.</span></span>

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

### <span data-ttu-id="7302e-126">-이름</span><span class="sxs-lookup"><span data-stu-id="7302e-126">-Name</span></span>
<span data-ttu-id="7302e-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-127">The trigger name.</span></span>

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

### <span data-ttu-id="7302e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7302e-128">-PassThru</span></span>
<span data-ttu-id="7302e-129">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7302e-130">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7302e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7302e-131">-WorkspaceName</span></span>
<span data-ttu-id="7302e-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7302e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7302e-133">-WorkspaceObject</span></span>
<span data-ttu-id="7302e-134">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7302e-135">-확인</span><span class="sxs-lookup"><span data-stu-id="7302e-135">-Confirm</span></span>
<span data-ttu-id="7302e-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7302e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7302e-137">-WhatIf</span></span>
<span data-ttu-id="7302e-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7302e-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7302e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7302e-140">CommonParameters</span></span>
<span data-ttu-id="7302e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7302e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7302e-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7302e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7302e-143">입력</span><span class="sxs-lookup"><span data-stu-id="7302e-143">INPUTS</span></span>

### <span data-ttu-id="7302e-144">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="7302e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7302e-145">Synapse. PSTriggerResource/.</span><span class="sxs-lookup"><span data-stu-id="7302e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="7302e-146">출력</span><span class="sxs-lookup"><span data-stu-id="7302e-146">OUTPUTS</span></span>

### <span data-ttu-id="7302e-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7302e-147">System.Boolean</span></span>

## <span data-ttu-id="7302e-148">상속자</span><span class="sxs-lookup"><span data-stu-id="7302e-148">NOTES</span></span>

## <span data-ttu-id="7302e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7302e-149">RELATED LINKS</span></span>
